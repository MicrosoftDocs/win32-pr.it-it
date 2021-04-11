---
description: Il gestore del filtro deve essere registrato. È anche possibile individuare un gestore di filtri esistente per una determinata estensione di file tramite il registro di sistema o tramite l'interfaccia ILoadFilter.
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: Registrazione di gestori di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f39688bbea3bb0dd73ef28a0ba6e8b0dcf7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128566"
---
# <a name="registering-filter-handlers"></a>Registrazione di gestori di filtro

Il gestore del filtro deve essere registrato. È anche possibile individuare un gestore di filtri esistente per una determinata estensione di file tramite il registro di sistema o tramite l'interfaccia [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) .

Questo argomento è organizzato nel modo seguente:

- [Registrazione dei gestori di filtri per la ricerca di Windows](#registering-filter-handlers)
  - [Approccio obsoleto per la registrazione dei gestori di filtri](#obsolete-approach-for-registering-filters-handlers)
- [Sostituzione di gestori di filtro esistenti](#replacing-existing-filter-handlers)
- [Ricerca di un gestore di filtro per un'estensione di file specificata](#finding-a-filter-handler-for-a-given-file-extension)
- [Risorse aggiuntive](#additional-resources)
- [Argomenti correlati](#related-topics)

> [!NOTE]  
> Un gestore di filtro è un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

## <a name="registering-filters-handlers-for-windows-search"></a>Registrazione dei gestori di filtri per la ricerca di Windows

Nella tabella seguente sono elencati i GUID necessari per la registrazione di un nuovo gestore di protocollo o per trovare un gestore di protocollo esistente.

| GUID                                     | Definito dall'utente o dall'applicazione | Descrizione                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| **89BCB740-6119-101A-BCB7-00DD010655AF** | Applicazione                 | Il GUID dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è una costante della chiave del registro di sistema per tutti i gestori di filtro. |
| **{PersistentHandlerGUID}**              | User                        | Si tratta del GUID per il gestore permanente.                                                              |
| **{FilterHandlerCLSID}**                 | User                        | Si tratta dell'identificatore di classe (CLSID) per il gestore di filtro.                                              |
| **{ApplicationGUID}**                    | User                        | Si tratta di un GUID intermedio (aggregato).                                                                |

I gestori di filtro devono essere registrati nel \_ computer locale HKEY \_ perché SearchFilterHost.exe è in esecuzione con l'account di sistema e pertanto non possono accedere alle chiavi del registro di sistema per l'utente corrente di HKEY \_ \_ per l'utente connesso. Inoltre, il gruppo Users deve disporre dell'accesso in lettura ed esecuzione al gestore di filtro. dll, perché SearchFilterHost.exe rimuove tutti i diritti di amministratore e consente solo diritti non di amministratore. Poiché il percorso predefinito del progetto di Visual Studio si trova nella directory dell'utente corrente e pertanto non concede le autorizzazioni di lettura al gruppo Users, è necessario spostare il file con estensione dll o modificare gli ACL per consentire l'accesso SearchFilterHost.exe.

Quando si registra un nuovo gestore di filtro, si consiglia di utilizzare un nome descrittivo, ad esempio IFilter HTML.

**Per registrare il nuovo gestore di filtri:**

1. Specificare l'estensione e il GUID del gestore permanente che utilizzeranno il gestore di filtro:

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                PersistentHandler
                   (Default) = {PersistentHandlerGUID}
```

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {PersistentHandlerGUID}
                      PersistentAddinsRegistered
                         {89BCB740-6119-101A-BCB7-00DD010655AF}l
                            (Default) = {FilterHandlerCLSID}
```

2. Registrare il gestore di filtri con le chiavi e i valori seguenti:

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {FilterHandlerCLSID}
                      (Default) = {DescriptiveFilterHandlerName}
                      InprocServer32
                         (Default) = DLL Install Path
                         ThreadingModel = Both
```

### <a name="obsolete-approach-for-registering-filters-handlers"></a>Approccio obsoleto per la registrazione dei gestori di filtri

Questo approccio non è consigliato per l'uso. I filtri possono essere registrati per un CLSID che rappresenta una classe Component Object Model (COM) e/o per un'estensione del nome di file. È possibile registrare entrambi i filtri se è necessario registrare un gestore di filtri per una classe e un gestore di filtro diverso per un'estensione di file all'interno della classe. Si noti che un gestore di filtri registrato per un'estensione di file ha la precedenza su un gestore di filtro per un CLSID.

Queste voci sono voci del registro di sistema OLE standard fino alla voce **CLSID \\ {ApplicationGUID}** inclusa. La DLL sample.dll implementa il comportamento degli oggetti in esecuzione per la classe. txt. Si noti la voce aggiuntiva, PersistentHandler. Questa voce specifica la classe responsabile del broker delle richieste agli oggetti permanenti della classe di esempio. La voce in **PersistentAddinsRegistered** identifica l'implementazione responsabile dell'interfaccia denominata **89BCB740-6119-101A-BCB7-00DD010655AF**(IID \_ IFilter). La classe che implementa l' **\_ IFilter di IID** include voci del registro di sistema OLE standard. La DLL InprocServer32 viene caricata tramite il meccanismo OLE standard.

Windows Search osserva il modello di threading specificato per il gestore di filtro. Quando il modello di threading è impostato su **entrambi**, il gestore di filtro deve essere thread-safe. in caso contrario, se non è thread-safe, specificare **Apartment**. Si noti che i gestori di filtro devono essere sempre thread-safe.

Le voci del registro di sistema di esempio seguenti sono relative a un gestore di filtro registrato per una classe e un'estensione di file. **{PersistentHandlerGUID}** e **{FilterHandlerCLSID}** vengono usati come variabili che indicano i valori che devono essere specificati dall'autore del gestore di filtro. I valori sono di tipo REG \_ SZ.

```
HKEY_LOCAL_MACHINE
   Software
      Classes
         .txt
            (Default) = SampleFile
         SampleFile
            (Default) = Class for Sample Files
            CLSID
               (Default) = {ApplicationGUID}
         CLSID
            {ApplicationGUID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sample.dll
               PersistentHandler
                  (Default) = {PersistentHandlerGUID}
            {PersistentHandlerGUID}
               (Default) = Sample file persistent handler
               PersistentAddinsRegistered
                  {89BCB740-6119-101A-BCB7-00DD010655AF}l
                     (Default) = {FilterHandlerCLSID}
            {FilterHandlerCLSID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sampfilt.dll
                  ThreadingModel = Both
```

## <a name="replacing-existing-filter-handlers"></a>Sostituzione di gestori di filtro esistenti

Si consiglia di non sostituire i gestori di filtri incorporati per i tipi di file comuni, ad esempio txt, doc, HTML, URL e così via, perché questa operazione può avere effetti indesiderati su altri componenti di sistema. L'indicizzazione di corpi dei messaggi di posta elettronica dipende, ad esempio, dai gestori di filtri txt, HTML e RTF.

Se è in corso l'installazione di un nuovo gestore di filtro per un tipo di file in sostituzione di una registrazione filtro esistente, il programma di installazione deve salvare la registrazione corrente e ripristinarla se il nuovo gestore di filtro viene disinstallato. Non esiste alcun meccanismo per concatenare i filtri. Di conseguenza, il nuovo gestore di filtro è responsabile della replica di tutte le funzionalità necessarie del filtro precedente.

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a>Ricerca di un gestore di filtro per un'estensione di file specificata

È possibile usare l'interfaccia [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) per trovare un gestore di filtro per una determinata estensione di file. Le voci del registro di sistema di esempio seguenti illustrano come eseguire questa operazione per i file HTML. In questo esempio, il gestore del filtro per i documenti HTML è nlhtml.dll. I valori sono di tipo REG \_ SZ.

**Per trovare il gestore di filtro per una determinata estensione di file:**

1. Controllare se l'estensione per il tipo di file filtrato ha un gestore permanente registrato nella voce del registro di sistema \\ HKEY \_ Local \_ Machine \\ software \\ Classes. Extension. In tal caso, lasciare che la chiave sia {PersistentHandlerGUID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. Se non è presente un gestore permanente registrato per l'estensione, trovare il CLSID associato al tipo di documento nella voce del registro di sistema \\ HKEY \_ Local \_ Machine \\ software \\ Classes. Lasciare che la chiave sia {ApplicationGUID}. Determinare quindi se un gestore persistente è registrato per il CLSID: usando {ApplicationGUID} individuare il gestore permanente per \\ la \_ voce HKEY delle \_ classi software del computer locale \\ \\ \\ CLSID \\ {ApplicationGUID}. Lasciare che la chiave sia {PersistentHandlerGUID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                (Default) = Class for WWW HTML files
                CLSID
                   (Default) = {25336920-03F9-11CF-8FD0-00AA00686F13}
             CLSID
                {25336920-03F9-11CF-8FD0-00AA00686F13}
                   PersistentHandler
                      (Default) = {PersistentHandlerGUID}
```

3. Determinare il GUID del gestore permanente: usando {PersistentHandlerGUID} trovare il GUID del gestore permanente per il tipo di documento. Il valore nella voce del registro di sistema HKEY \_ Local \_ Machine \\ software \\ Classes \\ CLSID \\ {PERSISTENTHANDLERGUID} \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF restituisce il GUID del gestore persistente per questo tipo di documento. Lasciare che la chiave sia {FilterHandlerCLSID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Determinare il gestore di filtro: usando {FilterHandlerCLSID} che è stato determinato nel passaggio precedente, individuare il gestore di filtro sotto la voce \\ HKEY \_ Local \_ Machine \\ software \\ Classes \\ CLSID \\ {FilterHandlerCLSID} \\ InprocServer32. In questo esempio il nome del gestore del filtro descrittivo usato è IFilter HTML.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             CLSID
                {EEC97550-47A9-11CF-B952-00AA0051FE20}
                   (Default) = HTML IFilter
                    Data type  REG_SZ
                    InprocServer32
                    nlhtml.dll
```

## <a name="additional-resources"></a>Risorse aggiuntive

- Nell'esempio di codice [IFilterSample](-search-sample-ifiltersample.md) , disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), viene illustrato come creare una classe di base [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) per implementare l'interfaccia **IFilter** .
- Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).
- Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).
- Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

[Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)

[Informazioni sui gestori di filtro in Windows Search](-search-ifilter-about.md)

[Procedure consigliate per la creazione di gestori di filtro in Windows Search](-search-3x-wds-extidx-filters.md)

[Restituzione di proprietà da un gestore di filtro](-search-ifilter-property-filtering.md)

[Gestori di filtri forniti con Windows](-search-ifilter-implementations.md)

[Implementazione di gestori di filtro in Windows Search](-search-ifilter-constructing-filters.md)

[Test di gestori filtro](-search-ifilter-testing-filters.md)
