---
description: IContextMenu è l'interfaccia più potente ma anche più complessa da implementare.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Come implementare l'interfaccia IContextMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f251b9a64c3f401239eeb7c88286c016f399cc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967443"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a>Come implementare l'interfaccia IContextMenu

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) è l'interfaccia più potente ma anche più complessa da implementare. Si consiglia di implementare un verbo utilizzando uno dei metodi del verbo statico. Per ulteriori informazioni, vedere [scelta di un metodo di menu di scelta rapida statico o dinamico](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) dispone di tre metodi, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)e [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), descritti in dettaglio.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   C++

### <a name="prerequisites"></a>Prerequisiti

-   Verbo statico
-   Menu di scelta rapida

## <a name="instructions"></a>Istruzioni

### <a name="icontextmenugetcommandstring-method"></a>Metodo IContextMenu:: GetCommandString

Il metodo [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) del gestore viene usato per restituire il nome canonico per un verbo. È facoltativo. In Windows XP e nelle versioni precedenti di Windows, quando Esplora risorse dispone di una barra di stato, questo metodo viene utilizzato per recuperare il testo della Guida visualizzato nella barra di stato per una voce di menu.

Il parametro *idCmd* include l'offset dell'identificatore del comando definito al momento della chiamata a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) . Se viene richiesta una stringa della guida, *uFlags* verrà impostato su **cataloghi globali \_ HELPTEXTW**. Copiare la stringa della guida nel buffer *pszName* , eseguendone il cast in un **PWSTR**. La stringa del verbo viene richiesta impostando *uFlags* su **cataloghi globali \_ VERBW**. Copiare la stringa appropriata in *pszName*, proprio come con la stringa della guida. I flag **GC \_ validatea** e **GC \_ VALIDATEW** non vengono utilizzati dai gestori dei menu di scelta rapida.

Nell'esempio seguente viene illustrata un'implementazione semplice di [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) che corrisponde all'esempio di [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) fornito nella sezione relativa al [metodo IContextMenu:: QueryContextMenu](shortcut-menu-using-dynamic-verbs.md) di questo argomento. Poiché il gestore aggiunge solo una voce di menu, è possibile restituire un solo set di stringhe. Il metodo verifica se *idCmd* è valido e, in caso contrario, restituisce la stringa richiesta.

La funzione [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) viene usata per copiare la stringa richiesta in *pszName* per assicurarsi che la stringa copiata non superi le dimensioni del buffer specificato da *cchName*. Questo esempio implementa il supporto solo per i valori Unicode di *uFlags*, in quanto solo quelli sono stati usati in Esplora risorse da Windows 2000.


```
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb that is passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a>Metodo IContextMenu:: InvokeCommand

Questo metodo viene chiamato quando un utente fa clic su una voce di menu per indicare al gestore di eseguire il comando associato. Il parametro *pici* punta a una struttura che contiene le informazioni necessarie per eseguire il comando.

Sebbene *pici* sia dichiarato in Shlobj. h come struttura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , in pratica spesso punta a una struttura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) . Questa struttura è una versione estesa di **CMINVOKECOMMANDINFO** e include diversi membri aggiuntivi che rendono possibile il passaggio di stringhe Unicode.

Verificare il membro **cbSize** di *pici* per determinare la struttura passata. Se si tratta di una struttura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) e per il membro **fmask** è impostato il flag **\_ \_ Unicode CMIC mask** , eseguire il cast di *pici* a **CMINVOKECOMMANDINFOEX**. Ciò consente all'applicazione di utilizzare le informazioni Unicode contenute negli ultimi cinque membri della struttura.

Il membro **lpVerb** o **lpVerbW** della struttura viene usato per identificare il comando da eseguire. I comandi sono identificati in uno dei due modi seguenti:

-   Dalla stringa del verbo del comando
-   In base all'offset dell'identificatore del comando

Per distinguere tra questi due casi, controllare la parola più ordinata di **lpVerb** per il caso ANSI o **lpVerbW** per il caso Unicode. Se la parola più ordinata è diversa da zero, **lpVerb** o **lpVerbW** include una stringa verbo. Se la parola più ordinata è pari a zero, l'offset del comando è nella parola più bassa dell'ordine di **lpVerb**.

Nell'esempio seguente viene illustrata un'implementazione semplice di [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) che corrisponde agli esempi [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) e [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) forniti prima e dopo questa sezione. Il metodo determina prima di tutto la struttura che viene passata. Quindi determina se il comando viene identificato in base al relativo offset o al relativo verbo. Se **lpVerb** o **lpVerbW** contiene un verbo o un offset valido, il metodo Visualizza una finestra di messaggio.


```
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a>Metodo IContextMenu:: QueryContextMenu

La shell chiama [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) per abilitare il gestore del menu di scelta rapida per aggiungere le voci di menu al menu. Passa l'handle **HMENU** nel parametro *HMENU* . Il parametro *indexMenu* è impostato sull'indice da utilizzare per la prima voce di menu da aggiungere.

Tutte le voci di menu aggiunte dal gestore devono contenere identificatori che rientrano tra i valori nei parametri *idCmdFirst* e *idCmdLast* . In genere, il primo identificatore del comando è impostato su *idCmdFirst*, che viene incrementato di uno (1) per ogni comando aggiuntivo. Questa procedura consente di evitare il superamento di *idCmdLast* e massimizza il numero di identificatori disponibili nel caso in cui la shell chiami più di un gestore.

L' *offset del comando* di un identificatore di elemento è la differenza tra l'identificatore e il valore in *idCmdFirst*. Archiviare l'offset di ogni elemento aggiunto dal gestore al menu di scelta rapida, perché la shell potrebbe utilizzare l'offset per identificare l'elemento se successivamente chiama [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

È inoltre consigliabile assegnare un [verbo](launch.md) a ogni comando aggiunto. Un verbo è una stringa che può essere utilizzata al posto dell'offset per identificare il comando quando viene chiamato [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) . Viene anche usato da funzioni come [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per eseguire i comandi del menu di scelta rapida.

Sono disponibili tre flag che possono essere passati tramite il parametro *uFlags* rilevanti per i gestori dei menu di scelta rapida. descritti nella tabella seguente.



| Flag             | Descrizione                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DEFAULTONLY di CMF \_ | L'utente ha selezionato il comando predefinito, in genere facendo doppio clic sull'oggetto. [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deve restituire il controllo alla shell senza modificare il menu. |
| CMF \_ NOdefault   | Nessun elemento nel menu deve essere l'elemento predefinito. Il metodo deve aggiungere i comandi al menu.                                                                                                                          |
| \_normale CMF      | Il menu di scelta rapida verrà visualizzato normalmente. Il metodo deve aggiungere i comandi al menu.                                                                                                                            |



 

Usare [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) o [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) per aggiungere voci di menu all'elenco. Restituire quindi un valore **HRESULT** con gravità impostato su gravità \_ riuscita. Impostare il valore del codice sull'offset dell'identificatore di comando più grande assegnato, più uno (1). Si supponga, ad esempio, che *idCmdFirst* sia impostato su 5 e che vengano aggiunti tre elementi al menu con gli identificatori dei comandi 5, 7 e 8. Il valore restituito deve essere \_ HRESULT (gravità \_ riuscita, 0, 8 + 1).

Nell'esempio seguente viene illustrata un'implementazione semplice di [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) che inserisce un singolo comando. L'offset dell'identificatore per il comando è IDM \_ display, che è impostato su zero. Le variabili **m \_ pszVerb** e **m \_ pwszVerb** sono variabili private utilizzate per archiviare la stringa del verbo indipendente dal linguaggio associata nei formati ANSI e Unicode.


```
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a>Commenti

Per altre attività di implementazione di verbi, vedere [creazione di gestori di menu di scelta rapida](context-menu-handlers.md).

 

 
