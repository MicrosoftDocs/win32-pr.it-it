---
title: Creazione di gestori di ricerca
description: La shell supporta diverse utilità di ricerca che consentono agli utenti di individuare oggetti dello spazio dei nomi, ad esempio file o stampanti. È possibile creare un motore di ricerca personalizzato e renderlo disponibile agli utenti implementando e registrando un gestore di ricerca.
ms.assetid: ffd023bb-16ab-43ce-b00b-5e32656c8013
keywords:
- gestori di ricerca
- register,search handlers
- gestori di ricerca statici
- register, gestori di ricerca statici
- gestori di ricerca dinamica
- register, gestori di ricerca dinamica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be891247c36687b0305e7e9c60711a233fb9b1d4f7f8554d0103be4cc0dc5a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975781"
---
# <a name="creating-search-handlers"></a>Creazione di gestori di ricerca

\[Questa funzionalità è supportata solo in Windows XP o versioni precedenti. Usare Windows ricerca.\]

La shell supporta diverse utilità di ricerca che consentono agli utenti di individuare oggetti dello spazio dei nomi, ad esempio file o stampanti. È possibile creare un motore di ricerca personalizzato e renderlo disponibile agli utenti implementando e registrando un gestore *di ricerca*.

Le procedure generali per l'implementazione e la registrazione di un gestore estensioni della shell sono descritte in [Creazione di gestori di estensioni della shell.](/windows/desktop/shell/handlers) Questo documento è in particolare sugli aspetti dell'implementazione specifici dei gestori di ricerca.

-   [Funzionamento dei gestori di ricerca](#how-search-handlers-work)
-   [Registrazione dei gestori di ricerca](#registering-search-handlers)
    -   [Registrazione di un gestore di ricerca statico](#registering-a-static-search-handler)
    -   [Registrazione di un gestore di ricerca dinamica](#registering-a-dynamic-search-handler)
-   [Implementazione di gestori di ricerca](#implementing-search-handlers)

## <a name="how-search-handlers-work"></a>Funzionamento dei gestori di ricerca

Gli utenti possono selezionare un motore di ricerca in due modi. Il primo modo è dal menu Start. Con sistemi precedenti a Windows 2000, selezionando il comando Trova nel menu **Start** viene visualizzato un sottomenu dei motori di ricerca disponibili.  Con Windows 2000 e versioni successive, il  comando Trova del menu **St** art è stato rinominato Cerca. La figura seguente mostra il **pulsante** Cerca in un sistema Windows XP.

![Sottomenu di ricerca del menu Start](images/searchhandler1.jpg)

Gli utenti possono anche avviare una ricerca Windows Explorer. Nei sistemi precedenti Windows 2000, fanno  clic sul comando Trova nel **menu** Strumenti per visualizzare essenzialmente lo stesso menu associato al menu **Start.** Tuttavia, Windows Explorer per Windows 2000 gestisce i motori di ricerca in modo molto diverso. Invece di gestire i motori di ricerca come sottomenu del **menu** Strumenti, è ora disponibile un **pulsante** Cerca sulla barra degli strumenti. Facendo clic su questo pulsante si apre il riquadro **Cerca della barra di** Explorer. La figura seguente mostra il **riquadro di ricerca Cerca file** e cartelle.

![Riquadro di ricerca della barra di Esplora risorse](images/searchhandler2.jpg)

Esistono alcune differenze nel modo in cui i Windows 2000 e precedenti gestiscono i gestori di ricerca che influiscono sia sull'implementazione che sulla registrazione.



| Pre-Windows 2000                                                                                                                                                                                                       | Windows 2000 e versioni successive                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| I gestori di ricerca vengono implementati come tipo di gestore [del menu di scelta rapida](/windows/desktop/shell/context-menu-handlers).                                                                                                                     | I gestori di ricerca possono essere implementati come gestori del menu di scelta rapida o come documenti HTML dinamici (DHTML).                                                                                                                                                                                                               |
| I gestori di ricerca possono essere statici o dinamici. I gestori statici vengono caricati solo quando vengono selezionati dall'utente. I gestori dinamici vengono caricati dalla shell all'avvio e non vengono terminati fino alla chiusura della shell. | I gestori implementati come gestori del menu di scelta rapida possono essere statici o dinamici. I gestori implementati come documenti DHTML devono essere statici.                                                                                                                                                                           |
| I gestori di ricerca vengono **visualizzati** nel sottomenu Trova del menu  **Start** e nel sottomenu Trova del menu strumenti Windows Explorer.                                                                                   | I gestori di ricerca vengono visualizzati **solo** nel sottomenu Cerca del menu **Start.** Per rendere disponibile un riquadro di ricerca personalizzato tramite la barra dei menu Windows Explorer, è necessario implementarlo come oggetto [banda](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)). Viene quindi elencato nel sottomenu **Barra di Explorer** del menu Windows Visualizzazione **Esplora** risorse. |



 

## <a name="registering-search-handlers"></a>Registrazione dei gestori di ricerca

I gestori di ricerca vengono registrati nella sottochiave **FindExtensions dei tipi** di file.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

Da questo punto, la procedura di registrazione dipende dal fatto che il gestore sia statico o dinamico. Per una descrizione generale di come registrare i gestori di estensioni della shell, vedere [Creazione di gestori di estensioni della shell.](/windows/desktop/shell/handlers)

### <a name="registering-a-static-search-handler"></a>Registrazione di un gestore di ricerca statico

I gestori di ricerca statici vengono caricati solo quando vengono avviati dall'utente. Questo approccio funziona meglio per le DLL di piccole dimensioni che possono essere caricate rapidamente. Se si usa DHTML per implementare il gestore, deve essere statico. Per registrare un gestore di estensione statico, creare una sottochiave denominata per il gestore nella **sottochiave Static** della **sottochiave FindExtensions.** Il nome non viene usato dal sistema, ma non deve essere identico ad altri nomi di gestori di ricerca nella sottochiave **FindExtensions.**

### <a name="shortcut-menu-based-search-handlers"></a>Gestori di ricerca basati su menu di scelta rapida

Se il gestore viene implementato come gestore [del menu](/windows/desktop/shell/context-menu-handlers)di scelta rapida, impostare il valore predefinito della sottochiave del nome del gestore sul GUID dell'identificatore di classe (CLSID) dell'oggetto. Nella sottochiave name del gestore creare una sottochiave denominata **0** (zero) e impostarne il  valore predefinito sulla stringa che verrà visualizzata nel sottomenu Cerca **o** Trova. È possibile abilitare i tasti di scelta rapida nel modo consueto, facendo precedere il carattere di scelta rapida da una e commerciale (&). È possibile visualizzare un'icona piccola facoltativa a destra del testo del menu creando una sottochiave **DefaultIcon** nella sottochiave **0.** Impostarne il valore predefinito su una stringa contenente il percorso del file contenente l'icona, seguito da una virgola, seguita dall'indice in base zero dell'icona.

L'esempio seguente registra il **gestore di ricerca MySearchEngine.** Il testo del menu è "My Search Engine", con M specificato come tasto di scelta rapida. L'icona si trova in C: \\ MyDir \\MySearch.dll, con indice 2.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {MySearchEngine CLSID GUID}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
```

### <a name="dhtml-based-search-handlers"></a>Gestori di ricerca basati su DHTML

Con Windows 2000, è anche possibile implementare un gestore di ricerca come documento DHTML. Il nome è **elencato** nel sottomenu Cerca del menu **Start.** Quando l'utente lo seleziona, viene avviato Windows Explorer con la barra di Explorer aperta nel documento di ricerca. È anche possibile specificare un documento DHTML da visualizzare a destra della barra di Explorer. Non è possibile avviare un gestore diverso dal riquadro di ricerca predefinito. I motori di ricerca possono essere avviati direttamente da Windows Explorer, ma solo se vengono implementati come [oggetti banda.](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85))

Per registrare un gestore di ricerca basato su DHTML, impostare la sottochiave name del gestore sul formato stringa di CLSID \_ ShellSearchExt (attualmente {169A0691-8DF9-11d1-A1C4-00C04FD75D13}) e creare le sottochiavi seguenti.

1.  Creare una **sottochiave 0**(zero) sotto la sottochiave del nome del gestore e impostarne il valore predefinito sul testo del menu.
2.  Per visualizzare un'icona accanto al testo del menu, creare una sottochiave **DefaultIcon** in **0** e impostarne il valore predefinito sul percorso e sull'indice dell'icona.
3.  Creare una **sottochiave SearchGUID** in **0.** Assegnare un GUID al documento DHTML e impostare il valore predefinito **di SearchGUID** sul formato stringa. Non è necessario registrare questo GUID in **HKEY \_ CLASSES ROOT \_ \\ CLSID**.
4.  Creare una **sottochiave URL** in **SearchGUID**. Impostare il valore predefinito sul percorso del documento HTML che verrà visualizzato nella barra di Explorer.
5.  Creare una **sottochiave UrlNavNew** in **SearchGUID**. Impostare il valore predefinito sul percorso del documento HTML che verrà visualizzato a destra della barra di Explorer.

L'esempio seguente registra il **gestore di ricerca MySearchEngine** implementato come documento DHTML. Il testo del menu è "My Search Engine", con M specificato come tasto di scelta rapida. L'icona si trova in C: \\ MyDir \\MySearch.dll, con indice 2. Il documento DHTML della barra di Explorer è C: MyDirMySearch.htm e il documento che verrà visualizzato a destra della barra di Explorer è \\ \\ C: \\ MyDir \\MySearchPage.htm.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {169A0691-8DF9-11d1-A1C4-00C04FD75D13}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
                                 SearchGUID
                                    (Default) = {My Search GUID}
                                    Url
                                       (Default) = C:\MyDir\MySearch.htm
                                    UrlNavNew
                                       (Default) = C:\MyDir\MySearchPage.htm
```

### <a name="registering-a-dynamic-search-handler"></a>Registrazione di un gestore di ricerca dinamica

Se il gestore viene implementato come gestore [del menu di scelta rapida,](/windows/desktop/shell/context-menu-handlers)è anche possibile registrarlo come gestore dinamico. In tal caso, verrà caricato con la shell e terminerà solo quando la shell viene chiusa. I gestori di ricerca dinamica rispondono molto più rapidamente rispetto ai gestori statici quando vengono avviati dall'utente. Questo approccio funziona meglio se il caricamento della DLL del gestore potrebbe richiedere molto tempo o se è probabile che venga chiamato di frequente.

I gestori di ricerca dinamica vengono registrati nella **sottochiave FindExtensions.**

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

Creare una sottochiave di **FindExtensions** denominata per il gestore e impostarne il valore predefinito sul GUID CLSID del gestore. Le icone di menu non sono supportate per i gestori di ricerca dinamica. L'esempio seguente registra MySearchEngine come gestore di ricerca dinamico.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     MySearchEngine
                        (Default) = {MySearchEngine CLSID GUID}
                        0
                           (Default) = &My Search Engine
```

A differenza dei gestori di ricerca statici, non si specifica il testo del menu nel Registro di sistema. Quando il gestore viene caricato, la shell chiamerà il metodo [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) del gestore per aggiungere elementi al sottomenu **Trova o Cerca.** 

## <a name="implementing-search-handlers"></a>Implementazione di gestori di ricerca

I gestori di ricerca possono essere implementati come gestori del menu di scelta rapida per tutte le versioni di Windows. Ad Windows 2000, possono essere implementate anche come documenti DHTML.

Per una descrizione generale di come implementare i gestori del menu di scelta rapida, vedere [Creazione di gestori del menu di scelta rapida.](/windows/desktop/shell/context-menu-handlers) I gestori di ricerca differiscono dai gestori del menu di scelta rapida standard in pochi modi.

Per i gestori di menu **statici,** il sottomenu Trova **o** Cerca viene creato dalle informazioni nel Registro di sistema. Non è necessario che il gestore a cui viene aggiunta una voce di menu, come farebbe un normale gestore del menu di scelta rapida. Shell gestisce i gestori di menu statici nel modo seguente.

-   Quando l'utente avvia la voce di menu del gestore, Shell carica la DLL del gestore e chiama [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) per notificare al gestore di avviare il motore di ricerca. I [**metodi IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) e [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) non vengono chiamati.
-   Quando [**viene chiamato IContextMenu::InvokeCommand,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) il membro **lpVerb** della struttura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) passato in identifica il comando. La parola di basso livello **di lpVerb** è impostata sull'equivalente numerico del nome della sottochiave del comando. Poiché questa sottochiave è in genere denominata **0,** **lpVerb** è in genere impostato su zero. Il gestore deve quindi avviare il motore di ricerca.

I gestori di ricerca dinamica vengono implementati in modo molto identico ai normali gestori del menu di scelta rapida. L'eccezione principale è che quando viene chiamato [**IShellExtInit::Initialize,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) gli argomenti *pidlFolder* e *lpdobj* vengono impostati su **NULL.**

I gestori di ricerca basati su DHTML vengono implementati come normali documenti DHTML. Possono includere qualsiasi tecnologia HTML, DHTML o scripting supportata da Windows Internet Explorer.

 

 