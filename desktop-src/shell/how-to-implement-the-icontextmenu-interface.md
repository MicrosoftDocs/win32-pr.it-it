---
description: IContextMenu è l'interfaccia più potente ma anche più complessa da implementare.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Come implementare l'interfaccia IContextMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44ec65d95a4f6d67a9f15e10f5720be21c3b6c57fba5d0cf920bd12be54f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223468"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a>Come implementare l'interfaccia IContextMenu

[**IContextMenu è**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) l'interfaccia più potente ma anche più complessa da implementare. È consigliabile implementare un verbo usando uno dei metodi verbi statici. Per altre informazioni, vedere Scelta di un metodo statico o dinamico del [menu di scelta rapida.](shortcut-choose-method.md) [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) include tre metodi, [**GetCommandString,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)e [**QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)descritti in dettaglio qui.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   C++

### <a name="prerequisites"></a>Prerequisiti

-   Verbo statico
-   Menu di scelta rapida

## <a name="instructions"></a>Istruzioni

### <a name="icontextmenugetcommandstring-method"></a>Metodo IContextMenu::GetCommandString

Il metodo [**IContextMenu::GetCommandString del**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) gestore viene usato per restituire il nome canonico per un verbo. È facoltativo. In Windows XP e versioni precedenti di Windows, quando Windows Explorer ha una barra di stato, questo metodo viene usato per recuperare il testo della Guida visualizzato nella barra di stato per una voce di menu.

Il *parametro idCmd* contiene l'offset dell'identificatore del comando definito quando è stato chiamato [**IContextMenu::QueryContextMenu.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) Se viene richiesta una stringa della Guida, *uFlags* verrà impostato su **GCS \_ HELPTEXTW**. Copiare la stringa della Guida nel buffer *pszName,* eseguendo il cast a **un PWSTR.** La stringa verbo viene richiesta impostando *uFlags* su **GCS \_ VERBW.** Copiare la stringa appropriata in *pszName*, come con la stringa della Guida. I **flag \_ GCS VALIDATEA** e **GCS \_ VALIDATEW** non vengono usati dai gestori del menu di scelta rapida.

L'esempio seguente illustra una semplice implementazione di [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) che corrisponde all'esempio [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) fornito nella sezione [Metodo IContextMenu::QueryContextMenu](shortcut-menu-using-dynamic-verbs.md) di questo argomento. Poiché il gestore aggiunge una sola voce di menu, è possibile restituire un solo set di stringhe. Il metodo verifica se *idCmd* è valido e, in caso contrario, restituisce la stringa richiesta.

La [**funzione StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) viene usata per copiare la stringa richiesta in *pszName* per assicurarsi che la stringa copiata non superi le dimensioni del buffer specificato da *cchName*. In questo esempio viene implementato il supporto solo per i valori Unicode di *uFlags*, perché solo quelli sono stati usati in Windows Explorer Windows 2000.


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



### <a name="icontextmenuinvokecommand-method"></a>Metodo IContextMenu::InvokeCommand

Questo metodo viene chiamato quando un utente fa clic su una voce di menu per indicare al gestore di eseguire il comando associato. Il *parametro pici* punta a una struttura che contiene le informazioni necessarie per eseguire il comando.

Anche *se il file pici* viene dichiarato in Shlobj.h come struttura [**CMINVOKECOMMANDINFO,**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) in pratica punta spesso a una [**struttura CMINVOKECOMMANDINFOEX.**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) Questa struttura è una versione estesa di **CMINVOKECOMMANDINFO** e include diversi membri aggiuntivi che rendono possibile passare stringhe Unicode.

Controllare il **membro cbSize** di *pici* per determinare la struttura passata. Se si tratta di una struttura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) e per il membro **fMask** è impostato il flag **UNICODE CMIC \_ MASK, \_** eseguire il cast *di pici* a **CMINVOKECOMMANDINFOEX.** In questo modo l'applicazione può usare le informazioni Unicode contenute negli ultimi cinque membri della struttura .

Il membro **lpVerb** o **lpVerbW della** struttura viene usato per identificare il comando da eseguire. I comandi vengono identificati in uno dei due modi seguenti:

-   In base alla stringa verbo del comando
-   In base all'offset dell'identificatore del comando

Per distinguere tra questi due casi, controllare la parola di ordine superiore **di lpVerb** per la distinzione tra maiuscole e minuscole ANSI o **lpVerbW** per la distinzione Unicode. Se la parola più importante è diversa da zero, **lpVerb** o **lpVerbW** contiene una stringa verbo. Se la parola più alta è zero, l'offset del comando si trova nella parola di ordine più basso **di lpVerb**.

L'esempio seguente illustra una semplice implementazione di [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) che corrisponde agli esempi [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) [**e IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) forniti prima e dopo questa sezione. Il metodo determina innanzitutto la struttura passata. Determina quindi se il comando è identificato dall'offset o dal verbo. Se **lpVerb o** **lpVerbW contiene** un verbo o un offset valido, il metodo visualizza una finestra di messaggio.


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



### <a name="icontextmenuquerycontextmenu-method"></a>Metodo IContextMenu::QueryContextMenu

La shell chiama [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) per consentire al gestore del menu di scelta rapida di aggiungere le voci di menu al menu. Passa l'handle **HMENU** nel *parametro hmenu.* Il *parametro indexMenu* è impostato sull'indice da usare per la prima voce di menu da aggiungere.

Le voci di menu aggiunte dal gestore devono avere identificatori compresi tra i valori nei parametri *idCmdFirst* *e idCmdLast.* In genere, il primo identificatore di comando è impostato su *idCmdFirst*, che viene incrementato di uno (1) per ogni comando aggiuntivo. Questa procedura consente di evitare il superamento di *idCmdLast* e ottimizza il numero di identificatori disponibili nel caso in cui la shell chiami più di un gestore.

L'offset dei comandi di *un identificatore* di elemento è la differenza tra l'identificatore e il valore in *idCmdFirst.* Archiviare l'offset di ogni elemento aggiunto dal gestore al menu di scelta rapida, perché la shell potrebbe usare l'offset per identificare l'elemento se successivamente chiama [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

È anche necessario assegnare [un verbo](launch.md) a ogni comando aggiunto. Un verbo è una stringa che può essere usata al posto dell'offset per identificare il comando quando [**viene chiamato InvokeCommand.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) Viene usato anche da funzioni come [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per eseguire i comandi del menu di scelta rapida.

Esistono tre flag che possono essere passati tramite il *parametro uFlags* rilevanti per i gestori del menu di scelta rapida. descritti nella tabella seguente.



| Flag             | Descrizione                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | L'utente ha selezionato il comando predefinito, in genere facendo doppio clic sull'oggetto. [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deve restituire il controllo alla shell senza modificare il menu. |
| CMF \_ NODEFAULT   | Nessuna voce nel menu deve essere l'elemento predefinito. Il metodo deve aggiungere i relativi comandi al menu.                                                                                                                          |
| CMF \_ NORMAL      | Il menu di scelta rapida verrà visualizzato normalmente. Il metodo deve aggiungere i relativi comandi al menu.                                                                                                                            |



 

Usare [**InsertMenu o**](/windows/win32/api/winuser/nf-winuser-insertmenua) [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) per aggiungere voci di menu all'elenco. Restituire quindi un **valore HRESULT** con la gravità impostata su SEVERITY \_ SUCCESS. Impostare il valore del codice sull'offset dell'identificatore di comando più grande assegnato, più uno (1). Si supponga, ad esempio, che *idCmdFirst* sia impostato su 5 e che siano stati aggiunti tre elementi al menu con identificatori di comando 5, 7 e 8. Il valore restituito deve essere MAKE \_ HRESULT(SEVERITY \_ SUCCESS, 0, 8 + 1).

L'esempio seguente illustra una semplice implementazione di [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) che inserisce un singolo comando. L'offset dell'identificatore per il comando è IDM \_ DISPLAY, che è impostato su zero. Le **variabili m \_ pszVerb** e **m \_ pwszVerb** sono variabili private usate per archiviare la stringa verbo indipendente dalla lingua associata nei formati ANSI e Unicode.


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

Per altre attività di implementazione dei verbi, vedere [Creazione di gestori del menu di scelta rapida.](context-menu-handlers.md)

 

 
