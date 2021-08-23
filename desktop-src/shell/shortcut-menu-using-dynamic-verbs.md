---
description: I gestori del menu di scelta rapida sono noti anche come gestori di menu di scelta rapida o gestori di verbi. Un gestore del menu di scelta rapida è un tipo di gestore del tipo di file.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Personalizzazione di un menu di scelta rapida tramite verbi dinamici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b33361be5a89480e05bb42bd760b63517bf0b06c9828cae36a36ecddce1e9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968310"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a>Personalizzazione di un menu di scelta rapida tramite verbi dinamici

I gestori del menu di scelta rapida sono noti anche come gestori di menu di scelta rapida o gestori di verbi. Un gestore del menu di scelta rapida è un tipo di gestore del tipo di file.

Questo argomento è organizzato come segue:

-   [Informazioni sui verbi statici e dinamici](#about-static-and-dynamic-verbs)
-   [Funzionamento dei gestori del menu di scelta rapida con i verbi dinamici](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [Evitare conflitti dovuti a nomi di verbi non qualificati](#avoiding-collisions-due-to-unqualified-verb-names)
-   [Registrazione di un gestore del menu di scelta rapida con un verbo dinamico](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [Implementazione dell'interfaccia IContextMenu](#implementing-the-icontextmenu-interface)
    -   [Metodo IContextMenu::GetCommandString](#icontextmenugetcommandstring-method)
    -   [Metodo IContextMenu::InvokeCommand](#icontextmenuinvokecommand-method)
    -   [Metodo IContextMenu::QueryContextMenu](#icontextmenuquerycontextmenu-method)
-   [Argomenti correlati](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a>Informazioni sui verbi statici e dinamici

È consigliabile implementare un menu di scelta rapida usando uno dei metodi verbi statici. È consigliabile seguire le istruzioni fornite nella sezione "Personalizzazione di un menu di scelta rapida tramite verbi statici" di Creazione di gestori [del menu di scelta rapida.](context-menu-handlers.md) Per ottenere il comportamento dinamico per i verbi statici in Windows 7 e versioni successive, vedere "Recupero del comportamento dinamico per i verbi statici" in Creazione di gestori [del menu di scelta rapida.](context-menu-handlers.md) Per informazioni dettagliate sull'implementazione di verbi statici e sui verbi dinamici da evitare, vedere Scelta di un verbo statico o dinamico [per il menu di scelta rapida.](shortcut-choose-method.md)

Se è necessario estendere il menu di scelta rapida per un tipo di file registrando un verbo dinamico per il tipo di file, seguire le istruzioni fornite più avanti in questo argomento.

> [!Note]  
> Esistono considerazioni speciali per il Windows a 64 bit quando si registrano gestori che funzionano nel contesto delle applicazioni a 32 bit: quando i verbi della shell vengono richiamati nel contesto di un'applicazione a 32 bit, il sottosistema WOW64 reindirizza file system l'accesso ad alcuni percorsi. Se il .exe è archiviato in uno di questi percorsi, non è accessibile in questo contesto. Di conseguenza, per risolvere il problema, archiviare il .exe in un percorso che non viene reindirizzato o archiviare una versione stub del .exe che avvia la versione reale.

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a>Funzionamento dei gestori del menu di scelta rapida con i verbi dinamici

Oltre a [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown)i gestori del menu di scelta rapida esportano le interfacce aggiuntive seguenti per gestire la messaggistica necessaria per implementare le voci di menu disegnate dal proprietario:

-   [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obbligatorio)
-   [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obbligatorio)
-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (facoltativo)
-   [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (facoltativo)

Per altre informazioni sulle voci di menu create dal proprietario, vedere la sezione *Creating Owner-Drawn Menu Items* in Using [Menus](../menurc/using-menus.md).

Shell usa [**l'interfaccia IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) per inizializzare il gestore. Quando la shell chiama [**IShellExtInit::Initialize,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)passa un oggetto dati con il nome dell'oggetto e un puntatore a un elenco di identificatori di elemento (PIDL) della cartella che contiene il file. Il *parametro hkeyProgID è il percorso* del Registro di sistema in cui viene registrato l'handle del menu di scelta rapida. Il **metodo IShellExtInit::Initialize** deve estrarre il nome file dall'oggetto dati e archiviare il nome e il puntatore della cartella a un elenco di identificatori di elemento (PIDL) per un uso successivo. Per altre informazioni sull'inizializzazione del gestore, vedere [Implementazione di IShellExtInit.](handlers.md)

Quando i verbi vengono presentati in un menu di scelta rapida, vengono prima individuati, quindi presentati all'utente e infine richiamati. L'elenco seguente descrive questi tre passaggi in modo più dettagliato:

1.  La shell chiama [**IContextMenu::QueryContextMenu,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)che restituisce un set di verbi che possono essere basati sullo stato degli elementi o del sistema.
2.  Il sistema passa un handle **HMENU** che il metodo può usare per aggiungere voci al menu di scelta rapida.
3.  Se l'utente fa clic su uno degli elementi del gestore, la shell chiama [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand). Il gestore può quindi eseguire il comando appropriato.

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a>Evitare conflitti dovuti a nomi di verbi non qualificati

Poiché i verbi vengono registrati per ogni tipo, è possibile usare lo stesso nome di verbo per i verbi su elementi diversi. In questo modo le applicazioni possono fare riferimento a verbi comuni indipendenti dal tipo di elemento. Sebbene questa funzionalità sia utile, l'uso di nomi non qualificati può causare conflitti con più fornitori di software indipendenti (ISV) che scelgono lo stesso nome di verbo. Per evitare questo problema, aggiungere sempre il prefisso ai verbi con il nome ISV come indicato di seguito:

`ISV_Name.verb`

Usare sempre un ProgID specifico dell'applicazione. L'adozione della convenzione di mapping dell'estensione di file a un ProgID fornito da ISV evita potenziali conflitti. Tuttavia, poiché alcuni tipi di elemento non usano questo mapping, è necessario usare nomi univoci del fornitore. Quando si aggiunge un verbo a un ProgID esistente che potrebbe già avere tale verbo registrato, è necessario rimuovere la chiave del Registro di sistema per il verbo precedente prima di aggiungere il proprio verbo. È necessario eseguire questa operazione per evitare di unire le informazioni sui verbi dai due verbi. In caso negativo, si verifica un comportamento imprevedibile.

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a>Registrazione di un gestore del menu di scelta rapida con un verbo dinamico

I gestori del menu di scelta rapida sono associati a un tipo di file o a una cartella. Per i tipi di file, il gestore viene registrato nella sottochiave seguente.

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

Per associare un gestore del menu di scelta rapida a un tipo di file o a una cartella, creare prima una sottochiave nella sottochiave **ContextMenuHandlers.** Assegnare un nome alla sottochiave per il gestore e impostare il valore predefinito della sottochiave sul formato stringa del GUID dell'identificatore di classe (CLSID) del gestore.

Quindi, per associare un gestore del menu di scelta rapida a diversi tipi di cartelle, registrare il gestore nello stesso modo in cui si farebbe per un tipo di file, ma nella sottochiave *FolderType,* come illustrato nell'esempio seguente.

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

Per altre informazioni sui tipi di cartella per cui è possibile registrare i gestori, vedere [Registrazione dei gestori delle estensioni della shell.](handlers.md)

Se a un tipo di file è associato un menu di scelta rapida, facendo doppio clic su un oggetto viene in genere avviato il comando predefinito e il metodo [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) del gestore non viene chiamato. Per specificare che il metodo **IContextMenu::QueryContextMenu** del gestore deve essere chiamato quando si fa doppio clic su un oggetto, creare una sottochiave sotto la sottochiave **CLSID** del gestore, come illustrato di seguito.

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

Quando si fa doppio clic su un oggetto associato al gestore, viene chiamato [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) con il flag **\_ DEFAULTONLY CMF** impostato nel *parametro uFlags.*

I gestori del menu di scelta rapida devono impostare la sottochiave **MayChangeDefaultMenu** solo se potrebbe essere necessario modificare il verbo predefinito del menu di scelta rapida. L'impostazione di questa sottochiave forza il sistema a caricare la DLL del gestore quando si fa doppio clic su un elemento associato. Se il gestore non modifica il verbo predefinito, è consigliabile non impostare questa sottochiave perché in questo modo il sistema carica inutilmente la DLL.

Nell'esempio seguente vengono illustrate le voci del Registro di sistema che abilitano un gestore del menu di scelta rapida per un tipo di file con estensione myp. La sottochiave **CLSID** del gestore include una sottochiave **MayChangeDefaultMenu** per garantire che il gestore venga chiamato quando l'utente fa doppio clic su un oggetto correlato.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a>Implementazione dell'interfaccia IContextMenu

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) è il metodo più potente ma anche il metodo più complesso da implementare. È consigliabile implementare un verbo usando uno dei metodi verbi statici. Per altre informazioni, vedere [Scelta di un verbo statico o dinamico per il menu di scelta rapida.](shortcut-choose-method.md) [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) include tre metodi, **GetCommandString,** **InvokeCommand** e **QueryContextMenu,** descritti in dettaglio qui.

### <a name="icontextmenugetcommandstring-method"></a>Metodo IContextMenu::GetCommandString

Il metodo [**IContextMenu::GetCommandString del**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) gestore viene usato per restituire il nome canonico per un verbo. È facoltativo. In Windows XP e versioni precedenti di Windows, quando Windows Explorer ha una barra di stato, questo metodo viene usato per recuperare il testo della Guida visualizzato nella barra di stato per una voce di menu.

Il *parametro idCmd* contiene l'offset dell'identificatore del comando definito quando è stato chiamato [**IContextMenu::QueryContextMenu.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) Se viene richiesta una stringa della Guida, *uFlags* verrà impostato su **GCS \_ HELPTEXTW**. Copiare la stringa della Guida nel buffer *pszName,* eseguendo il cast a **un PWSTR.** La stringa verbo viene richiesta impostando *uFlags* su **GCS \_ VERBW.** Copiare la stringa appropriata in *pszName*, come con la stringa della Guida. I **flag \_ GCS VALIDATEA** e **GCS \_ VALIDATEW** non vengono usati dai gestori del menu di scelta rapida.

L'esempio seguente illustra una semplice implementazione di [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) che corrisponde all'esempio [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) fornito nella sezione [Metodo IContextMenu::QueryContextMenu](#icontextmenuquerycontextmenu-method) di questo argomento. Poiché il gestore aggiunge una sola voce di menu, è possibile restituire un solo set di stringhe. Il metodo verifica se *idCmd* è valido e, in caso contrario, restituisce la stringa richiesta.

La [**funzione StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) viene usata per copiare la stringa richiesta in *pszName* per assicurarsi che la stringa copiata non superi le dimensioni del buffer specificato da *cchName*. In questo esempio viene implementato solo il supporto per i valori Unicode di *uFlags*, perché solo quelli sono stati usati in Windows Explorer Windows 2000.


```C++
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
                // to discover the canonical name for the verb passed in
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

Questo metodo viene chiamato quando un utente fa clic su una voce di menu per indicare al gestore di eseguire il comando associato. Il *parametro pici* punta a una struttura che contiene le informazioni necessarie.

Anche *se il file pici* viene dichiarato in Shlobj.h come struttura [**CMINVOKECOMMANDINFO,**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) in pratica punta spesso a una [**struttura CMINVOKECOMMANDINFOEX.**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) Questa struttura è una versione estesa di **CMINVOKECOMMANDINFO** e include diversi membri aggiuntivi che rendono possibile passare stringhe Unicode.

Controllare il **membro cbSize** di *pici* per determinare la struttura passata. Se si tratta di una struttura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) e per il membro **fMask** è impostato il flag **UNICODE CMIC \_ MASK, \_** eseguire il cast *di pici* a **CMINVOKECOMMANDINFOEX.** In questo modo l'applicazione può usare le informazioni Unicode contenute negli ultimi cinque membri della struttura .

Il membro **lpVerb** o **lpVerbW della** struttura viene usato per identificare il comando da eseguire. I comandi vengono identificati in uno dei due modi seguenti:

-   In base alla stringa verbo del comando
-   In base all'offset dell'identificatore del comando

Per distinguere tra questi due casi, controllare la parola di ordine superiore **di lpVerb** per il caso ANSI o **lpVerbW** per il caso Unicode. Se la parola più importante è diversa da zero, **lpVerb** o **lpVerbW** contiene una stringa verbo. Se la parola più alta è zero, l'offset del comando è nella parola di ordine più basso di **lpVerb**.

L'esempio seguente illustra una semplice implementazione di [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) che corrisponde agli esempi [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) e [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) forniti prima e dopo questa sezione. Il metodo determina prima quale struttura viene passata. Determina quindi se il comando è identificato dall'offset o dal verbo. Se **lpVerb o** **lpVerbW** contiene un verbo o un offset valido, il metodo visualizza una finestra di messaggio.


```C++
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

Shell chiama [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) per consentire al gestore del menu di scelta rapida di aggiungere le voci di menu al menu. Passa **l'handle HMENU** nel *parametro hmenu.* Il *parametro indexMenu* è impostato sull'indice da utilizzare per la prima voce di menu da aggiungere.

Tutte le voci di menu aggiunte dal gestore devono avere identificatori compresi tra i valori nei parametri *idCmdFirst* *e idCmdLast.* In genere, il primo identificatore di comando è impostato su *idCmdFirst*, che viene incrementato di uno (1) per ogni comando aggiuntivo. Questa procedura consente di evitare il superamento di *idCmdLast* e di ottimizzare il numero di identificatori disponibili nel caso in cui Shell chiami più di un gestore.

L'offset dei comandi *di un* identificatore di elemento è la differenza tra l'identificatore e il valore in *idCmdFirst*. Archiviare l'offset di ogni elemento aggiunto dal gestore al menu di scelta rapida perché shell potrebbe usarlo per identificare l'elemento se successivamente chiama [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

È anche necessario assegnare un [verbo](launch.md) a ogni comando aggiunto. Un verbo è una stringa che può essere usata al posto dell'offset per identificare il comando quando viene chiamato [**IContextMenu::InvokeCommand.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) Viene usato anche da funzioni come [**ShellExecuteEx per**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) eseguire i comandi del menu di scelta rapida.

Esistono tre flag che possono essere passati tramite il *parametro uFlags* rilevanti per i gestori del menu di scelta rapida. descritti nella tabella seguente.



| Flag             | Descrizione                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CMF \_ DEFAULTONLY | L'utente ha selezionato il comando predefinito, in genere facendo doppio clic sull'oggetto. [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deve restituire il controllo alla shell senza modificare il menu. |
| CMF \_ NODEFAULT   | Nessuna voce del menu deve essere l'elemento predefinito. Il metodo deve aggiungere i comandi al menu.                                                                                                                          |
| NORMALE \_ CMF      | Il menu di scelta rapida verrà visualizzato normalmente. Il metodo deve aggiungere i comandi al menu.                                                                                                                            |



 

Usare [**InsertMenu o**](/windows/win32/api/winuser/nf-winuser-insertmenua) [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) per aggiungere voci di menu all'elenco. Restituire quindi un **valore HRESULT** con la gravità impostata su **SEVERITY \_ SUCCESS**. Impostare il valore del codice sull'offset dell'identificatore di comando più grande assegnato, più uno (1). Si supponga, ad esempio, che *idCmdFirst* sia impostato su 5 e che siano stati aggiunti tre elementi al menu con identificatori di comando 5, 7 e 8. Il valore restituito deve essere `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .

L'esempio seguente illustra una semplice implementazione di [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) che inserisce un singolo comando. L'offset dell'identificatore per il comando è IDM \_ DISPLAY, che è impostato su zero. Le **variabili m \_ pszVerb** e **m \_ pwszVerb** sono variabili private usate per archiviare la stringa del verbo indipendente dalla lingua associata nei formati ANSI e Unicode.


```C++
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

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



Per altre attività di implementazione dei verbi, vedere [Creazione di gestori del menu di scelta rapida](context-menu-handlers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Menu di scelta rapida e gestori di menu di scelta rapida](context-menu.md)
</dt> <dt>

[Verbi e associazioni di file](fa-verbs.md)
</dt> <dt>

[Scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md)
</dt> <dt>

[Procedure consigliate per i gestori del menu di scelta rapida e più verbi di selezione](verbs-best-practices.md)
</dt> <dt>

[Creazione di gestori di menu di scelta rapida](context-menu-handlers.md)
</dt> <dt>

[Informazioni di riferimento sul menu di scelta rapida](context-menu-reference.md)
</dt> </dl>

 

 
