---
description: I gestori dei menu di scelta rapida sono noti anche come gestori di menu di scelta rapida o gestori di verbi. Un gestore di menu di scelta rapida è un tipo di gestore di tipi di file.
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: Personalizzazione di un menu di scelta rapida tramite verbi dinamici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980183"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a>Personalizzazione di un menu di scelta rapida tramite verbi dinamici

I gestori dei menu di scelta rapida sono noti anche come gestori di menu di scelta rapida o gestori di verbi. Un gestore di menu di scelta rapida è un tipo di gestore di tipi di file.

Questo argomento è organizzato nel modo seguente:

-   [Informazioni sui verbi statici e dinamici](#about-static-and-dynamic-verbs)
-   [Funzionamento dei gestori dei menu di scelta rapida con verbi dinamici](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [Evitare collisioni a causa di nomi di verbi non qualificati](#avoiding-collisions-due-to-unqualified-verb-names)
-   [Registrazione di un gestore di menu di scelta rapida con un verbo dinamico](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [Implementazione dell'interfaccia IContextMenu](#implementing-the-icontextmenu-interface)
    -   [Metodo IContextMenu:: GetCommandString](#icontextmenugetcommandstring-method)
    -   [Metodo IContextMenu:: InvokeCommand](#icontextmenuinvokecommand-method)
    -   [Metodo IContextMenu:: QueryContextMenu](#icontextmenuquerycontextmenu-method)
-   [Argomenti correlati](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a>Informazioni sui verbi statici e dinamici

Si consiglia di implementare un menu di scelta rapida usando uno dei metodi del verbo statico. È consigliabile seguire le istruzioni fornite nella sezione "personalizzazione di un menu di scelta rapida con verbi statici" di creazione di [gestori di menu di scelta rapida](context-menu-handlers.md). Per ottenere il comportamento dinamico per i verbi statici in Windows 7 e versioni successive, vedere la sezione relativa all'acquisizione del comportamento dinamico per i verbi statici in [creazione di gestori di menu di scelta rapida](context-menu-handlers.md). Per informazioni dettagliate sull'implementazione del verbo statico e sui verbi dinamici da evitare, vedere [scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md).

Se è necessario estendere il menu di scelta rapida per un tipo di file registrando un verbo dinamico per il tipo di file, seguire le istruzioni fornite più avanti in questo argomento.

> [!Note]  
> Quando si registrano i gestori che operano nel contesto di applicazioni a 32 bit, è necessario tenere presenti alcune considerazioni speciali per Windows a 64 bit: quando i verbi della shell vengono richiamati nel contesto di un'applicazione a 32 bit, il sottosistema WOW64 reindirizza file system accesso ad alcuni percorsi. Se il gestore. exe viene archiviato in uno di questi percorsi, non è accessibile in questo contesto. Pertanto, come soluzione alternativa, archiviare il file con estensione exe in un percorso che non viene reindirizzato oppure archiviare una versione stub del file exe che avvia la versione reale.

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a>Funzionamento dei gestori dei menu di scelta rapida con verbi dinamici

Oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), i gestori dei menu di scelta rapida esportano le seguenti interfacce aggiuntive per gestire la messaggistica necessaria per implementare voci di menu create dal proprietario:

-   [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (obbligatorio)
-   [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (obbligatorio)
-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (facoltativo)
-   [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (facoltativo)

Per ulteriori informazioni sulle voci di menu create dal proprietario, vedere la sezione *creazione di Owner-Drawn voci di menu* in [utilizzo di menu](../menurc/using-menus.md).

Shell usa l'interfaccia [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) per inizializzare il gestore. Quando la shell chiama [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), passa un oggetto dati con il nome dell'oggetto e un puntatore a un elenco di identificatori di elemento (PIDL) della cartella che contiene il file. Il parametro *hkeyProgID* è il percorso del registro di sistema in cui è registrato il punto di controllo del menu di scelta rapida. Il metodo **IShellExtInit:: Initialize** deve estrarre il nome del file dall'oggetto dati e archiviare il nome e il puntatore della cartella in un elenco di identificatori di elemento (PIDL) per un uso successivo. Per ulteriori informazioni sull'inizializzazione del gestore, vedere [implementazione di IShellExtInit](handlers.md).

Quando i verbi vengono presentati in un menu di scelta rapida, vengono prima individuati, quindi presentati all'utente e infine richiamati. Nell'elenco seguente vengono descritti in modo più dettagliato questi tre passaggi:

1.  La shell chiama [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), che restituisce un set di verbi che possono essere basati sullo stato degli elementi o del sistema.
2.  Il sistema passa un handle **HMENU** che il metodo può usare per aggiungere elementi al menu di scelta rapida.
3.  Se l'utente fa clic su uno degli elementi del gestore, la shell chiama [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand). Il gestore può quindi eseguire il comando appropriato.

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a>Evitare collisioni a causa di nomi di verbi non qualificati

Poiché i verbi sono registrati per tipo, è possibile usare lo stesso nome di verbo per i verbi su elementi diversi. In questo modo, le applicazioni fanno riferimento a verbi comuni indipendenti dal tipo di elemento. Sebbene questa funzionalità sia utile, l'utilizzo di nomi non qualificati può comportare conflitti con più fornitori di software indipendenti (ISV) che scelgono lo stesso nome del verbo. Per evitare questo problema, anteporre sempre i verbi al nome ISV come indicato di seguito:

`ISV_Name.verb`

Usare sempre un ProgID specifico dell'applicazione. L'adozione della convenzione di mapping dell'estensione di file a un ProgID fornito da ISV evita potenziali collisioni. Tuttavia, poiché alcuni tipi di elemento non utilizzano questo mapping, è necessario disporre di nomi univoci del fornitore. Quando si aggiunge un verbo a un ProgID esistente che potrebbe avere già registrato il verbo, è necessario prima rimuovere la chiave del registro di sistema per il verbo precedente prima di aggiungere il proprio verbo. È necessario eseguire questa operazione per evitare di unire le informazioni sui verbi dai due verbi. In caso contrario, viene restituito un comportamento imprevedibile.

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a>Registrazione di un gestore di menu di scelta rapida con un verbo dinamico

I gestori dei menu di scelta rapida sono associati a un tipo di file o a una cartella. Per i tipi di file, il gestore viene registrato nella sottochiave seguente.

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

Per associare un gestore di menu di scelta rapida a un tipo di file o a una cartella, creare prima una sottochiave nella sottochiave **ContextMenuHandlers** . Assegnare un nome alla sottochiave per il gestore, quindi impostare il valore predefinito della sottochiave sul formato stringa del GUID dell'identificatore di classe del gestore (CLSID).

Quindi, per associare un gestore di menu di scelta rapida con diversi tipi di cartelle, registrare il gestore nello stesso modo in cui si farebbe per un tipo di file, ma sotto la sottochiave *FolderType* , come illustrato nell'esempio seguente.

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

Per ulteriori informazioni sui tipi di cartelle per i quali è possibile registrare i gestori, vedere la pagina relativa alla [registrazione dei gestori di estensioni della shell](handlers.md).

Se a un tipo di file è associato un menu di scelta rapida, facendo doppio clic su un oggetto viene normalmente avviato il comando predefinito e il metodo [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) del gestore non viene chiamato. Per specificare che il metodo **IContextMenu:: QueryContextMenu** del gestore deve essere chiamato quando si fa doppio clic su un oggetto, creare una sottochiave sotto la sottochiave **CLSID** del gestore, come illustrato di seguito.

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

Quando si fa doppio clic su un oggetto associato al gestore, [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) viene chiamato con il flag **CMF \_ DEFAULTONLY** impostato nel parametro *uFlags* .

I gestori dei menu di scelta rapida devono impostare la sottochiave **MayChangeDefaultMenu** solo se potrebbero dover modificare il verbo predefinito del menu di scelta rapida. L'impostazione di questa sottochiave impone al sistema di caricare la DLL del gestore quando si fa doppio clic su un elemento associato. Se il gestore non modifica il verbo predefinito, è consigliabile non impostare questa sottochiave perché in questo modo il sistema carica la DLL inutilmente.

Nell'esempio seguente vengono illustrate le voci del registro di sistema che consentono un gestore di menu di scelta rapida per un tipo di file con estensione MYP. La sottochiave **CLSID** del gestore include una sottochiave **MayChangeDefaultMenu** per garantire che il gestore venga chiamato quando l'utente fa doppio clic su un oggetto correlato.

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

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) è il metodo più potente ma anche il più complesso da implementare. Si consiglia di implementare un verbo utilizzando uno dei metodi del verbo statico. Per ulteriori informazioni, vedere [scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md). [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) dispone di tre metodi, **GetCommandString**, **InvokeCommand** e **QueryContextMenu**, descritti in dettaglio.

### <a name="icontextmenugetcommandstring-method"></a>Metodo IContextMenu:: GetCommandString

Il metodo [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) del gestore viene usato per restituire il nome canonico per un verbo. È facoltativo. In Windows XP e nelle versioni precedenti di Windows, quando Esplora risorse dispone di una barra di stato, questo metodo viene utilizzato per recuperare il testo della Guida visualizzato nella barra di stato per una voce di menu.

Il parametro *idCmd* include l'offset dell'identificatore del comando definito al momento della chiamata a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) . Se viene richiesta una stringa della guida, *uFlags* verrà impostato su **cataloghi globali \_ HELPTEXTW**. Copiare la stringa della guida nel buffer *pszName* , eseguendone il cast in un **PWSTR**. La stringa del verbo viene richiesta impostando *uFlags* su **cataloghi globali \_ VERBW**. Copiare la stringa appropriata in *pszName*, proprio come con la stringa della guida. I flag **GC \_ validatea** e **GC \_ VALIDATEW** non vengono utilizzati dai gestori dei menu di scelta rapida.

Nell'esempio seguente viene illustrata un'implementazione semplice di [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) che corrisponde all'esempio [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) fornito nella sezione [metodo IContextMenu:: QueryContextMenu](#icontextmenuquerycontextmenu-method) di questo argomento. Poiché il gestore aggiunge solo una voce di menu, è possibile restituire un solo set di stringhe. Il metodo verifica se *idCmd* è valido e, in caso contrario, restituisce la stringa richiesta.

La funzione [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) viene usata per copiare la stringa richiesta in *pszName* per assicurarsi che la stringa copiata non superi le dimensioni del buffer specificato da *cchName*. Questo esempio implementa solo il supporto per i valori Unicode di *uFlags*, in quanto solo quelli sono stati usati in Esplora risorse da Windows 2000.


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



### <a name="icontextmenuinvokecommand-method"></a>Metodo IContextMenu:: InvokeCommand

Questo metodo viene chiamato quando un utente fa clic su una voce di menu per indicare al gestore di eseguire il comando associato. Il parametro *pici* punta a una struttura che contiene le informazioni necessarie.

Sebbene *pici* sia dichiarato in Shlobj. h come struttura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , in pratica spesso punta a una struttura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) . Questa struttura è una versione estesa di **CMINVOKECOMMANDINFO** e include diversi membri aggiuntivi che rendono possibile il passaggio di stringhe Unicode.

Verificare il membro **cbSize** di *pici* per determinare la struttura passata. Se si tratta di una struttura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) e per il membro **fmask** è impostato il flag **\_ \_ Unicode CMIC mask** , eseguire il cast di *pici* a **CMINVOKECOMMANDINFOEX**. Ciò consente all'applicazione di utilizzare le informazioni Unicode contenute negli ultimi cinque membri della struttura.

Il membro **lpVerb** o **lpVerbW** della struttura viene usato per identificare il comando da eseguire. I comandi sono identificati in uno dei due modi seguenti:

-   Dalla stringa del verbo del comando
-   In base all'offset dell'identificatore del comando

Per distinguere tra questi due casi, controllare la parola più ordinata di **lpVerb** per il caso ANSI o **lpVerbW** per il caso Unicode. Se la parola più ordinata è diversa da zero, **lpVerb** o **lpVerbW** include una stringa verbo. Se la parola più ordinata è pari a zero, l'offset del comando è nella parola più bassa dell'ordine di **lpVerb**.

Nell'esempio seguente viene illustrata un'implementazione semplice di [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) che corrisponde agli esempi [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) e [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) forniti prima e dopo questa sezione. Il metodo determina prima di tutto la struttura che viene passata. Quindi determina se il comando viene identificato in base al relativo offset o al relativo verbo. Se **lpVerb** o **lpVerbW** contiene un verbo o un offset valido, il metodo Visualizza una finestra di messaggio.


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



### <a name="icontextmenuquerycontextmenu-method"></a>Metodo IContextMenu:: QueryContextMenu

La shell chiama [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) per abilitare il gestore del menu di scelta rapida per aggiungere le voci di menu al menu. Passa l'handle **HMENU** nel parametro *HMENU* . Il parametro *indexMenu* è impostato sull'indice da utilizzare per la prima voce di menu da aggiungere.

Tutte le voci di menu aggiunte dal gestore devono contenere identificatori che rientrano tra i valori nei parametri *idCmdFirst* e *idCmdLast* . In genere, il primo identificatore del comando è impostato su *idCmdFirst*, che viene incrementato di uno (1) per ogni comando aggiuntivo. Questa procedura consente di evitare il superamento di *idCmdLast* e massimizza il numero di identificatori disponibili nel caso in cui la shell chiami più di un gestore.

L' *offset del comando* di un identificatore di elemento è la differenza tra l'identificatore e il valore in *idCmdFirst*. Archiviare l'offset di ogni elemento aggiunto dal gestore al menu di scelta rapida perché può essere utilizzato dalla Shell per identificare l'elemento se successivamente viene chiamato [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).

È inoltre consigliabile assegnare un [verbo](launch.md) a ogni comando aggiunto. Un verbo è una stringa che può essere utilizzata al posto dell'offset per identificare il comando quando viene chiamato [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) . Viene anche usato da funzioni come [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per eseguire i comandi del menu di scelta rapida.

Sono disponibili tre flag che possono essere passati tramite il parametro *uFlags* rilevanti per i gestori dei menu di scelta rapida. descritti nella tabella seguente.



| Flag             | Descrizione                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DEFAULTONLY di CMF \_ | L'utente ha selezionato il comando predefinito, in genere facendo doppio clic sull'oggetto. [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deve restituire il controllo alla shell senza modificare il menu. |
| CMF \_ NOdefault   | Nessun elemento nel menu deve essere l'elemento predefinito. Il metodo deve aggiungere i comandi al menu.                                                                                                                          |
| \_normale CMF      | Il menu di scelta rapida verrà visualizzato normalmente. Il metodo deve aggiungere i comandi al menu.                                                                                                                            |



 

Usare [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) o [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) per aggiungere voci di menu all'elenco. Restituire quindi un valore **HRESULT** con gravità impostato su **gravità \_ riuscita**. Impostare il valore del codice sull'offset dell'identificatore di comando più grande assegnato, più uno (1). Si supponga, ad esempio, che *idCmdFirst* sia impostato su 5 e che vengano aggiunti tre elementi al menu con gli identificatori dei comandi 5, 7 e 8. Il valore restituito deve essere `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` .

Nell'esempio seguente viene illustrata un'implementazione semplice di [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) che inserisce un singolo comando. L'offset dell'identificatore per il comando è IDM \_ display, che è impostato su zero. Le variabili **m \_ pszVerb** e **m \_ pwszVerb** sono variabili private usate per archiviare la stringa del verbo indipendente dal linguaggio associata nei formati ANSI e Unicode.


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



Per altre attività di implementazione di verbi, vedere [creazione di gestori di menu di scelta rapida](context-menu-handlers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Menu di scelta rapida (contesto) e gestori di menu di scelta rapida](context-menu.md)
</dt> <dt>

[Verbi e associazioni di file](fa-verbs.md)
</dt> <dt>

[Scelta di un verbo statico o dinamico per il menu di scelta rapida](shortcut-choose-method.md)
</dt> <dt>

[Procedure consigliate per i gestori di menu di scelta rapida e più verbi di selezione](verbs-best-practices.md)
</dt> <dt>

[Creazione di gestori di menu di scelta rapida](context-menu-handlers.md)
</dt> <dt>

[Riferimento al menu di scelta rapida](context-menu-reference.md)
</dt> </dl>

 

 
