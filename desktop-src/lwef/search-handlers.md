---
title: Creazione di gestori di ricerca
description: La Shell supporta diverse utilità di ricerca che consentono agli utenti di individuare gli oggetti dello spazio dei nomi, ad esempio file o stampanti. È possibile creare un motore di ricerca personalizzato e renderlo disponibile agli utenti implementando e registrando un gestore di ricerca.
ms.assetid: ffd023bb-16ab-43ce-b00b-5e32656c8013
keywords:
- gestori di ricerca
- Register, Cerca gestori
- gestori di ricerca statici
- Register, gestori di ricerca statici
- gestori di ricerca dinamici
- registri, gestori di ricerca dinamici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6476109302a176822137747353b2762b0caea8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337342"
---
# <a name="creating-search-handlers"></a>Creazione di gestori di ricerca

\[Questa funzionalità è supportata solo in Windows XP o versioni precedenti. Usare invece Windows Search.\]

La Shell supporta diverse utilità di ricerca che consentono agli utenti di individuare gli oggetti dello spazio dei nomi, ad esempio file o stampanti. È possibile creare un motore di ricerca personalizzato e renderlo disponibile agli utenti implementando e registrando un *gestore di ricerca*.

Le procedure generali per l'implementazione e la registrazione di un gestore di estensione della shell sono descritte in [creazione di gestori di estensioni della shell](/windows/desktop/shell/handlers). Questo documento è incentrato sugli aspetti dell'implementazione specifici dei gestori di ricerca.

-   [Funzionamento del gestore di ricerca](#how-search-handlers-work)
-   [Registrazione di gestori di ricerca](#registering-search-handlers)
    -   [Registrazione di un gestore di ricerca statico](#registering-a-static-search-handler)
    -   [Registrazione di un gestore di ricerca dinamico](#registering-a-dynamic-search-handler)
-   [Implementazione di gestori di ricerca](#implementing-search-handlers)

## <a name="how-search-handlers-work"></a>Funzionamento del gestore di ricerca

Gli utenti hanno due modi per selezionare un motore di ricerca. Il primo consiste nel menu Start. Con i sistemi precedenti a Windows 2000, selezionare il comando **trova** nel menu **Start** per visualizzare un sottomenu dei motori di ricerca disponibili. Con Windows 2000 e versioni successive, **il comando di ricerca del** menu **St** Art è stato rinominato search. Nella figura seguente viene illustrato il pulsante **Cerca** in un sistema Windows XP.

![sottomenu di ricerca del menu Start](images/searchhandler1.jpg)

Gli utenti possono anche avviare una ricerca da Esplora risorse. Nei sistemi precedenti a Windows 2000, fare clic sul comando **trova** nel menu **strumenti** per visualizzare essenzialmente lo stesso menu associato al menu **Start** . Tuttavia, Esplora risorse di Windows 2000 gestisce i motori di ricerca in modo molto diverso. Anziché gestire i motori di ricerca come sottomenu del menu **strumenti** , è ora disponibile un pulsante **Cerca** sulla barra degli strumenti. Fare clic su questo pulsante per aprire il riquadro di **ricerca** della barra di Explorer. La figura seguente mostra il riquadro **di ricerca di file e cartelle** .

![riquadro di ricerca della barra di Esplora risorse](images/searchhandler2.jpg)

Esistono diverse differenze nel modo in cui Windows 2000 e i sistemi precedenti gestiscono i gestori di ricerca che interessano l'implementazione e la registrazione.



| Pre-Windows 2000                                                                                                                                                                                                       | Windows 2000 e versioni successive                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| I gestori di ricerca sono implementati come un tipo di [gestore di menu di scelta rapida](/windows/desktop/shell/context-menu-handlers).                                                                                                                     | I gestori di ricerca possono essere implementati come gestori di menu di scelta rapida o come documenti DHTML (Dynamic HTML).                                                                                                                                                                                                               |
| I gestori di ricerca possono essere statici o dinamici. I gestori statici vengono caricati solo quando vengono selezionati dall'utente. I gestori dinamici vengono caricati dalla shell all'avvio e non vengono terminati fino alla chiusura della shell. | I gestori implementati come gestori di menu di scelta rapida possono essere statici o dinamici. I gestori implementati come documenti DHTML devono essere statici.                                                                                                                                                                           |
| I gestori di ricerca vengono visualizzati nel sottomenu **trova** del menu **Start** e nel sottomenu **trova** del menu  **strumenti** di Esplora risorse.                                                                                  | I gestori di ricerca vengono visualizzati solo nel sottomenu di **ricerca** del menu **Start** . Per rendere disponibile un riquadro di ricerca personalizzato tramite la barra dei menu di Esplora risorse, è necessario implementarlo come [oggetto banda](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)). Viene quindi elencato nel sottomenu **barra di Explorer** del menu  **visualizzazione** di Esplora risorse. |



 

## <a name="registering-search-handlers"></a>Registrazione di gestori di ricerca

I gestori di ricerca sono registrati nella sottochiave **FindExtensions** dei tipi di file.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

Da questo punto, la procedura di registrazione dipende dal fatto che il gestore sia statico o dinamico. Per informazioni generali su come registrare i gestori di estensioni della shell, vedere [creazione di gestori di estensioni della shell](/windows/desktop/shell/handlers).

### <a name="registering-a-static-search-handler"></a>Registrazione di un gestore di ricerca statico

I gestori di ricerca statici vengono caricati solo quando vengono avviati dall'utente. Questo approccio funziona meglio per le DLL di piccole dimensioni che possono essere caricate rapidamente. Se si utilizza DHTML per implementare il gestore, è necessario che sia statico. Per registrare un gestore di estensioni statiche, creare una sottochiave denominata per il gestore sotto la sottochiave **statica** della sottochiave **FindExtensions** . Il nome non viene utilizzato dal sistema, ma non deve essere identico ad altri nomi di gestori di ricerca nella sottochiave **FindExtensions** .

### <a name="shortcut-menu-based-search-handlers"></a>Gestori di ricerca basati sul menu di scelta rapida

Se il gestore viene implementato come [gestore di menu di scelta rapida](/windows/desktop/shell/context-menu-handlers), impostare il valore predefinito della sottochiave del nome del gestore sul GUID dell'identificatore di classe (CLSID) dell'oggetto. Nella sottochiave nome del gestore creare una sottochiave denominata **0**   (zero) e impostarne il valore predefinito sulla stringa che verrà visualizzata nel sottomenu **Cerca** o **trova** . È possibile abilitare le scelte rapide da tastiera nel modo consueto, facendo precedere il carattere di collegamento con una e commerciale (&). È possibile avere un'icona piccola facoltativa visualizzata a destra del testo del menu creando una sottochiave **DefaultIcon** nella sottochiave **0** . Impostare il valore predefinito su una stringa contenente il percorso del file contenente l'icona, seguito da una virgola, seguita dall'indice in base zero dell'icona.

Nell'esempio seguente viene registrato il gestore di ricerca **MySearchEngine** . Il testo del menu è "motore di ricerca personale", con M specificato come tasto di scelta rapida. L'icona si trova in C: \\ MyDir \\MySearch.dll con indice 2.

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

Con Windows 2000, è anche possibile implementare un gestore di ricerca come documento DHTML. Il nome è elencato nel sottomenu di **ricerca** del menu **Start** . Quando l'utente le seleziona, avvia Esplora risorse con la barra di Explorer aperta nel documento di ricerca. È anche possibile specificare un documento DHTML da visualizzare a destra della barra di Explorer. Non è possibile avviare un gestore diverso dal riquadro di ricerca predefinito. I motori di ricerca possono essere avviati direttamente da Esplora risorse, ma solo se sono implementati come [oggetti band](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)).

Per registrare un gestore di ricerca basato su DHTML, impostare la sottochiave del nome del gestore sul formato stringa di CLSID \_ ShellSearchExt (attualmente {169A0691-8DF9-11D1-A1C4-00C04FD75D13}) e creare le sottochiavi seguenti.

1.  Creare una sottochiave **0**(zero) nella sottochiave del nome del gestore e impostarne il valore predefinito sul testo del menu.
2.  Per visualizzare un'icona accanto al testo del menu, creare una sottochiave **DefaultIcon** in **0** e impostarne il valore predefinito sul percorso e sull'indice dell'icona.
3.  Creare una sottochiave **SearchGUID** inferiore a **0**. Assegnare un GUID al documento DHTML e impostare il valore predefinito di **SearchGUID** sul formato stringa corrispondente. Non è necessario registrare questo GUID nel **\_ \_ \\ CLSID radice delle classi HKEY**.
4.  Creare una sottochiave **URL** in **SearchGUID**. Impostare il valore predefinito sul percorso del documento HTML che verrà visualizzato nella barra di Explorer.
5.  Creare una sottochiave **UrlNavNew** in **SearchGUID**. Impostare il valore predefinito sul percorso del documento HTML che verrà visualizzato a destra della barra di Explorer.

Nell'esempio seguente viene registrato il gestore di ricerca **MySearchEngine** implementato come documento DHTML. Il testo del menu è "motore di ricerca personale", con M specificato come tasto di scelta rapida. L'icona si trova in C: \\ MyDir \\MySearch.dll con indice 2. Il documento DHTML della barra di Explorer è C: \\ MyDir \\MySearch.htm e il documento che verrà visualizzato a destra della barra di Explorer è c: \\ mydir \\MySearchPage.htm.

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

### <a name="registering-a-dynamic-search-handler"></a>Registrazione di un gestore di ricerca dinamico

Se il gestore viene implementato come [gestore di menu di scelta rapida](/windows/desktop/shell/context-menu-handlers), è possibile registrarlo anche come gestore dinamico. In tal caso, verrà caricato con la shell e verrà terminato solo quando la shell viene chiusa. I gestori di ricerca dinamici rispondono molto più rapidamente rispetto ai gestori statici quando vengono avviati dall'utente. Questo approccio funziona meglio se la DLL del gestore potrebbe richiedere molto tempo per il caricamento o se è probabile che venga chiamata di frequente.

I gestori di ricerca dinamici sono registrati nella sottochiave **FindExtensions** .

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

Creare una sottochiave di **FindExtensions** denominata per il gestore e impostarne il valore predefinito sul GUID del gestore CLSID. Le icone dei menu non sono supportate per i gestori di ricerca dinamici. Nell'esempio seguente viene registrato MySearchEngine come gestore di ricerca dinamico.

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

A differenza dei gestori di ricerca statici, non è necessario specificare il testo del menu nel registro di sistema. Quando il gestore viene caricato, la shell chiamerà il metodo [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) del gestore per aggiungere elementi al sottomenu **trova** o **Cerca** .

## <a name="implementing-search-handlers"></a>Implementazione di gestori di ricerca

I gestori di ricerca possono essere implementati come gestori di menu di scelta rapida per tutte le versioni di Windows. Per Windows 2000, possono essere implementati anche come documenti DHTML.

Per informazioni generali su come implementare i gestori dei menu di scelta rapida, vedere [creazione di gestori di menu](/windows/desktop/shell/context-menu-handlers)di scelta rapida. I gestori di ricerca sono diversi dai gestori dei menu di scelta rapida standard in pochi modi.

Per i gestori di menu statici, il sottomenu **trova** o **Cerca** viene creato dalle informazioni nel registro di sistema. Non è necessario che il gestore aggiunga una voce di menu, come farebbe un normale gestore di menu di scelta rapida. La shell gestisce i gestori dei menu statici nel modo seguente.

-   Quando l'utente avvia la voce di menu del gestore, la Shell carica la DLL del gestore e chiama [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) per notificare al gestore di avviare il motore di ricerca. I metodi [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) e [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) non vengono chiamati.
-   Quando viene chiamato [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) , il membro **LpVerb** della struttura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) passata in identifica il comando. La parola di ordine inferiore di **lpVerb** è impostata sull'equivalente numerico del nome della sottochiave del comando. Poiché questa sottochiave è in genere denominata **0**, **lpVerb** è in genere impostato su zero. Il gestore deve quindi avviare il motore di ricerca.

I gestori di ricerca dinamici sono implementati in modo molto simile ai normali gestori dei menu di scelta rapida. L'eccezione principale è che quando viene chiamato [**IShellExtInit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) , gli argomenti *pidlFolder* e *lpdobj* sono impostati su **null**.

I gestori di ricerca basati su DHTML vengono implementati come un normale documento DHTML. Possono includere qualsiasi tecnologia HTML, DHTML o di scripting supportata da Windows Internet Explorer.

 

 