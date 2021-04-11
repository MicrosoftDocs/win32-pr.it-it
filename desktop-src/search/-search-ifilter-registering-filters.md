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
# <a name="registering-filter-handlers"></a><span data-ttu-id="a84f3-104">Registrazione di gestori di filtro</span><span class="sxs-lookup"><span data-stu-id="a84f3-104">Registering Filter Handlers</span></span>

<span data-ttu-id="a84f3-105">Il gestore del filtro deve essere registrato.</span><span class="sxs-lookup"><span data-stu-id="a84f3-105">Your filter handler must be registered.</span></span> <span data-ttu-id="a84f3-106">È anche possibile individuare un gestore di filtri esistente per una determinata estensione di file tramite il registro di sistema o tramite l'interfaccia [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) .</span><span class="sxs-lookup"><span data-stu-id="a84f3-106">You can also locate an existing filter handler for a given file name extension either through the registry or by using the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface.</span></span>

<span data-ttu-id="a84f3-107">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="a84f3-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="a84f3-108">Registrazione dei gestori di filtri per la ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="a84f3-108">Registering Filters Handlers for Windows Search</span></span>](#registering-filter-handlers)
  - [<span data-ttu-id="a84f3-109">Approccio obsoleto per la registrazione dei gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="a84f3-109">Obsolete Approach for Registering Filters Handlers</span></span>](#obsolete-approach-for-registering-filters-handlers)
- [<span data-ttu-id="a84f3-110">Sostituzione di gestori di filtro esistenti</span><span class="sxs-lookup"><span data-stu-id="a84f3-110">Replacing Existing Filter Handlers</span></span>](#replacing-existing-filter-handlers)
- [<span data-ttu-id="a84f3-111">Ricerca di un gestore di filtro per un'estensione di file specificata</span><span class="sxs-lookup"><span data-stu-id="a84f3-111">Finding a Filter Handler for a Given File Extension</span></span>](#finding-a-filter-handler-for-a-given-file-extension)
- [<span data-ttu-id="a84f3-112">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a84f3-112">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="a84f3-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a84f3-113">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="a84f3-114">Un gestore di filtro è un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="a84f3-114">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

## <a name="registering-filters-handlers-for-windows-search"></a><span data-ttu-id="a84f3-115">Registrazione dei gestori di filtri per la ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="a84f3-115">Registering Filters Handlers for Windows Search</span></span>

<span data-ttu-id="a84f3-116">Nella tabella seguente sono elencati i GUID necessari per la registrazione di un nuovo gestore di protocollo o per trovare un gestore di protocollo esistente.</span><span class="sxs-lookup"><span data-stu-id="a84f3-116">The GUIDs you need for registering a new protocol handler or to find an existing protocol handler are listed in the following table.</span></span>

| <span data-ttu-id="a84f3-117">GUID</span><span class="sxs-lookup"><span data-stu-id="a84f3-117">GUID</span></span>                                     | <span data-ttu-id="a84f3-118">Definito dall'utente o dall'applicazione</span><span class="sxs-lookup"><span data-stu-id="a84f3-118">User or application defined</span></span> | <span data-ttu-id="a84f3-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a84f3-119">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a84f3-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span><span class="sxs-lookup"><span data-stu-id="a84f3-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span></span> | <span data-ttu-id="a84f3-121">Applicazione</span><span class="sxs-lookup"><span data-stu-id="a84f3-121">Application</span></span>                 | <span data-ttu-id="a84f3-122">Il GUID dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) è una costante della chiave del registro di sistema per tutti i gestori di filtro.</span><span class="sxs-lookup"><span data-stu-id="a84f3-122">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface GUID is a registry key constant for all filter handlers.</span></span> |
| <span data-ttu-id="a84f3-123">**{PersistentHandlerGUID}**</span><span class="sxs-lookup"><span data-stu-id="a84f3-123">**{PersistentHandlerGUID}**</span></span>              | <span data-ttu-id="a84f3-124">User</span><span class="sxs-lookup"><span data-stu-id="a84f3-124">User</span></span>                        | <span data-ttu-id="a84f3-125">Si tratta del GUID per il gestore permanente.</span><span class="sxs-lookup"><span data-stu-id="a84f3-125">This is the GUID for the persistent handler.</span></span>                                                              |
| <span data-ttu-id="a84f3-126">**{FilterHandlerCLSID}**</span><span class="sxs-lookup"><span data-stu-id="a84f3-126">**{FilterHandlerCLSID}**</span></span>                 | <span data-ttu-id="a84f3-127">User</span><span class="sxs-lookup"><span data-stu-id="a84f3-127">User</span></span>                        | <span data-ttu-id="a84f3-128">Si tratta dell'identificatore di classe (CLSID) per il gestore di filtro.</span><span class="sxs-lookup"><span data-stu-id="a84f3-128">This is the class identifier (CLSID) for the filter handler.</span></span>                                              |
| <span data-ttu-id="a84f3-129">**{ApplicationGUID}**</span><span class="sxs-lookup"><span data-stu-id="a84f3-129">**{ApplicationGUID}**</span></span>                    | <span data-ttu-id="a84f3-130">User</span><span class="sxs-lookup"><span data-stu-id="a84f3-130">User</span></span>                        | <span data-ttu-id="a84f3-131">Si tratta di un GUID intermedio (aggregato).</span><span class="sxs-lookup"><span data-stu-id="a84f3-131">This is an intermediate (aggregated) GUID.</span></span>                                                                |

<span data-ttu-id="a84f3-132">I gestori di filtro devono essere registrati nel \_ computer locale HKEY \_ perché SearchFilterHost.exe è in esecuzione con l'account di sistema e pertanto non possono accedere alle chiavi del registro di sistema per l'utente corrente di HKEY \_ \_ per l'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="a84f3-132">Filter handlers must be registered in HKEY\_LOCAL\_MACHINE because SearchFilterHost.exe is running under the SYSTEM account and therefore cannot access registry keys for HKEY\_CURRENT\_USER for the logged-on user.</span></span> <span data-ttu-id="a84f3-133">Inoltre, il gruppo Users deve disporre dell'accesso in lettura ed esecuzione al gestore di filtro. dll, perché SearchFilterHost.exe rimuove tutti i diritti di amministratore e consente solo diritti non di amministratore.</span><span class="sxs-lookup"><span data-stu-id="a84f3-133">In addition, the Users group must have read-and-execute access to the filter handler .dll itself because SearchFilterHost.exe removes all administrator rights and permits only non-administrator rights.</span></span> <span data-ttu-id="a84f3-134">Poiché il percorso predefinito del progetto di Visual Studio si trova nella directory dell'utente corrente e pertanto non concede le autorizzazioni di lettura al gruppo Users, è necessario spostare il file con estensione dll o modificare gli ACL per consentire l'accesso SearchFilterHost.exe.</span><span class="sxs-lookup"><span data-stu-id="a84f3-134">Because the default Visual Studio project location is in the current user's directory, and so does not give read permissions to the Users group, you must either move the .dll or change the ACLs to allow SearchFilterHost.exe access.</span></span>

<span data-ttu-id="a84f3-135">Quando si registra un nuovo gestore di filtro, si consiglia di utilizzare un nome descrittivo, ad esempio IFilter HTML.</span><span class="sxs-lookup"><span data-stu-id="a84f3-135">When you register a new filter handler, we recommend that you use a descriptive name, for example, HTML IFilter.</span></span>

<span data-ttu-id="a84f3-136">**Per registrare il nuovo gestore di filtri:**</span><span class="sxs-lookup"><span data-stu-id="a84f3-136">**To register your new filter handler:**</span></span>

1. <span data-ttu-id="a84f3-137">Specificare l'estensione e il GUID del gestore permanente che utilizzeranno il gestore di filtro:</span><span class="sxs-lookup"><span data-stu-id="a84f3-137">Specify the extension and persistent handler GUID that will use the filter handler:</span></span>

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

2. <span data-ttu-id="a84f3-138">Registrare il gestore di filtri con le chiavi e i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a84f3-138">Register your filter handler with the following keys and values:</span></span>

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

### <a name="obsolete-approach-for-registering-filters-handlers"></a><span data-ttu-id="a84f3-139">Approccio obsoleto per la registrazione dei gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="a84f3-139">Obsolete Approach for Registering Filters Handlers</span></span>

<span data-ttu-id="a84f3-140">Questo approccio non è consigliato per l'uso.</span><span class="sxs-lookup"><span data-stu-id="a84f3-140">This approach is not recommended for use.</span></span> <span data-ttu-id="a84f3-141">I filtri possono essere registrati per un CLSID che rappresenta una classe Component Object Model (COM) e/o per un'estensione del nome di file.</span><span class="sxs-lookup"><span data-stu-id="a84f3-141">Filters can be registered for a CLSID that represents a Component Object Model (COM) class, and/or for a file name extension.</span></span> <span data-ttu-id="a84f3-142">È possibile registrare entrambi i filtri se è necessario registrare un gestore di filtri per una classe e un gestore di filtro diverso per un'estensione di file all'interno della classe.</span><span class="sxs-lookup"><span data-stu-id="a84f3-142">You could register both filters if you need to register a filter handler for a class, and a different filter handler for a file name extension within the class.</span></span> <span data-ttu-id="a84f3-143">Si noti che un gestore di filtri registrato per un'estensione di file ha la precedenza su un gestore di filtro per un CLSID.</span><span class="sxs-lookup"><span data-stu-id="a84f3-143">Note that a filter handler registered for a file name extension takes precedence over a filter handler for a CLSID.</span></span>

<span data-ttu-id="a84f3-144">Queste voci sono voci del registro di sistema OLE standard fino alla voce **CLSID \\ {ApplicationGUID}** inclusa.</span><span class="sxs-lookup"><span data-stu-id="a84f3-144">These entries are standard OLE registry entries up to and including the entry for the class **CLSID\\{ApplicationGUID}**.</span></span> <span data-ttu-id="a84f3-145">La DLL sample.dll implementa il comportamento degli oggetti in esecuzione per la classe. txt.</span><span class="sxs-lookup"><span data-stu-id="a84f3-145">The DLL sample.dll implements running object behavior for the .txt class.</span></span> <span data-ttu-id="a84f3-146">Si noti la voce aggiuntiva, PersistentHandler.</span><span class="sxs-lookup"><span data-stu-id="a84f3-146">Note the extra entry, PersistentHandler.</span></span> <span data-ttu-id="a84f3-147">Questa voce specifica la classe responsabile del broker delle richieste agli oggetti permanenti della classe di esempio.</span><span class="sxs-lookup"><span data-stu-id="a84f3-147">This entry specifies the class that is responsible for brokering requests to the persistent objects of the sample class.</span></span> <span data-ttu-id="a84f3-148">La voce in **PersistentAddinsRegistered** identifica l'implementazione responsabile dell'interfaccia denominata **89BCB740-6119-101A-BCB7-00DD010655AF**(IID \_ IFilter).</span><span class="sxs-lookup"><span data-stu-id="a84f3-148">The entry under **PersistentAddinsRegistered** identifies the implementation responsible for the interface named **89BCB740-6119-101A-BCB7-00DD010655AF**(IID\_IFilter).</span></span> <span data-ttu-id="a84f3-149">La classe che implementa l' **\_ IFilter di IID** include voci del registro di sistema OLE standard.</span><span class="sxs-lookup"><span data-stu-id="a84f3-149">The class implementing **IID\_IFilter** has standard OLE registry entries.</span></span> <span data-ttu-id="a84f3-150">La DLL InprocServer32 viene caricata tramite il meccanismo OLE standard.</span><span class="sxs-lookup"><span data-stu-id="a84f3-150">The InprocServer32 DLL is loaded through the standard OLE mechanism.</span></span>

<span data-ttu-id="a84f3-151">Windows Search osserva il modello di threading specificato per il gestore di filtro.</span><span class="sxs-lookup"><span data-stu-id="a84f3-151">Windows Search observes the threading model specified for the filter handler.</span></span> <span data-ttu-id="a84f3-152">Quando il modello di threading è impostato su **entrambi**, il gestore di filtro deve essere thread-safe. in caso contrario, se non è thread-safe, specificare **Apartment**.</span><span class="sxs-lookup"><span data-stu-id="a84f3-152">When the threading model is set to **Both**, the filter handler must be thread safe; otherwise, if it is not thread safe, specify **Apartment**.</span></span> <span data-ttu-id="a84f3-153">Si noti che i gestori di filtro devono essere sempre thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a84f3-153">Note that filter handlers should always be thread safe.</span></span>

<span data-ttu-id="a84f3-154">Le voci del registro di sistema di esempio seguenti sono relative a un gestore di filtro registrato per una classe e un'estensione di file.</span><span class="sxs-lookup"><span data-stu-id="a84f3-154">The following example registry entries are for a filter handler registered for a class and file name extension.</span></span> <span data-ttu-id="a84f3-155">**{PersistentHandlerGUID}** e **{FilterHandlerCLSID}** vengono usati come variabili che indicano i valori che devono essere specificati dall'autore del gestore di filtro.</span><span class="sxs-lookup"><span data-stu-id="a84f3-155">**{PersistentHandlerGUID}** and **{FilterHandlerCLSID}** are used as variables indicating values that need to be specified by the creator of the filter handler.</span></span> <span data-ttu-id="a84f3-156">I valori sono di tipo REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a84f3-156">The values are of type REG\_SZ.</span></span>

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

## <a name="replacing-existing-filter-handlers"></a><span data-ttu-id="a84f3-157">Sostituzione di gestori di filtro esistenti</span><span class="sxs-lookup"><span data-stu-id="a84f3-157">Replacing Existing Filter Handlers</span></span>

<span data-ttu-id="a84f3-158">Si consiglia di non sostituire i gestori di filtri incorporati per i tipi di file comuni, ad esempio txt, doc, HTML, URL e così via, perché questa operazione può avere effetti indesiderati su altri componenti di sistema.</span><span class="sxs-lookup"><span data-stu-id="a84f3-158">We recommend that you do not replace the built-in filter handlers for common file types such as .txt, .doc, .html, .url, and so forth, because doing so can have undesired effects on other system components.</span></span> <span data-ttu-id="a84f3-159">L'indicizzazione di corpi dei messaggi di posta elettronica dipende, ad esempio, dai gestori di filtri txt, HTML e RTF.</span><span class="sxs-lookup"><span data-stu-id="a84f3-159">Indexing email message bodies depends on the .txt, .html, and .rtf filter handlers, for example.</span></span>

<span data-ttu-id="a84f3-160">Se è in corso l'installazione di un nuovo gestore di filtro per un tipo di file in sostituzione di una registrazione filtro esistente, il programma di installazione deve salvare la registrazione corrente e ripristinarla se il nuovo gestore di filtro viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="a84f3-160">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="a84f3-161">Non esiste alcun meccanismo per concatenare i filtri.</span><span class="sxs-lookup"><span data-stu-id="a84f3-161">There is no mechanism to chain filters.</span></span> <span data-ttu-id="a84f3-162">Di conseguenza, il nuovo gestore di filtro è responsabile della replica di tutte le funzionalità necessarie del filtro precedente.</span><span class="sxs-lookup"><span data-stu-id="a84f3-162">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a><span data-ttu-id="a84f3-163">Ricerca di un gestore di filtro per un'estensione di file specificata</span><span class="sxs-lookup"><span data-stu-id="a84f3-163">Finding a Filter Handler for a Given File Extension</span></span>

<span data-ttu-id="a84f3-164">È possibile usare l'interfaccia [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) per trovare un gestore di filtro per una determinata estensione di file.</span><span class="sxs-lookup"><span data-stu-id="a84f3-164">You can use the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface to find a filter handler for a given file name extension.</span></span> <span data-ttu-id="a84f3-165">Le voci del registro di sistema di esempio seguenti illustrano come eseguire questa operazione per i file HTML.</span><span class="sxs-lookup"><span data-stu-id="a84f3-165">The following example registry entries illustrate how to do so for HTML files.</span></span> <span data-ttu-id="a84f3-166">In questo esempio, il gestore del filtro per i documenti HTML è nlhtml.dll.</span><span class="sxs-lookup"><span data-stu-id="a84f3-166">In this example, the filter handler for HTML documents is nlhtml.dll.</span></span> <span data-ttu-id="a84f3-167">I valori sono di tipo REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a84f3-167">The values are of type REG\_SZ.</span></span>

<span data-ttu-id="a84f3-168">**Per trovare il gestore di filtro per una determinata estensione di file:**</span><span class="sxs-lookup"><span data-stu-id="a84f3-168">**To find the filter handler for a given file name extension:**</span></span>

1. <span data-ttu-id="a84f3-169">Controllare se l'estensione per il tipo di file filtrato ha un gestore permanente registrato nella voce del registro di sistema \\ HKEY \_ Local \_ Machine \\ software \\ Classes. Extension.</span><span class="sxs-lookup"><span data-stu-id="a84f3-169">Check whether the extension for the type of files that are filtered has a persistent handler registered under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.extension.</span></span> <span data-ttu-id="a84f3-170">In tal caso, lasciare che la chiave sia {PersistentHandlerGUID}.</span><span class="sxs-lookup"><span data-stu-id="a84f3-170">If so, let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. <span data-ttu-id="a84f3-171">Se non è presente un gestore permanente registrato per l'estensione, trovare il CLSID associato al tipo di documento nella voce del registro di sistema \\ HKEY \_ Local \_ Machine \\ software \\ Classes.</span><span class="sxs-lookup"><span data-stu-id="a84f3-171">If there is not a persistent handler registered for the extension, find the CLSID associated with the document type under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.</span></span> <span data-ttu-id="a84f3-172">Lasciare che la chiave sia {ApplicationGUID}.</span><span class="sxs-lookup"><span data-stu-id="a84f3-172">Let this key be {ApplicationGUID}.</span></span> <span data-ttu-id="a84f3-173">Determinare quindi se un gestore persistente è registrato per il CLSID: usando {ApplicationGUID} individuare il gestore permanente per \\ la \_ voce HKEY delle \_ classi software del computer locale \\ \\ \\ CLSID \\ {ApplicationGUID}.</span><span class="sxs-lookup"><span data-stu-id="a84f3-173">Then determine whether a persistent handler is registered for the CLSID: using {ApplicationGUID} locate the persistent handler for the \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{ApplicationGUID} entry.</span></span> <span data-ttu-id="a84f3-174">Lasciare che la chiave sia {PersistentHandlerGUID}.</span><span class="sxs-lookup"><span data-stu-id="a84f3-174">Let this key be {PersistentHandlerGUID}.</span></span>

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

3. <span data-ttu-id="a84f3-175">Determinare il GUID del gestore permanente: usando {PersistentHandlerGUID} trovare il GUID del gestore permanente per il tipo di documento.</span><span class="sxs-lookup"><span data-stu-id="a84f3-175">Determine the GUID of the persistent handler: using {PersistentHandlerGUID} find the persistent handler GUID for the document type.</span></span> <span data-ttu-id="a84f3-176">Il valore nella voce del registro di sistema HKEY \_ Local \_ Machine \\ software \\ Classes \\ CLSID \\ {PERSISTENTHANDLERGUID} \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF restituisce il GUID del gestore persistente per questo tipo di documento.</span><span class="sxs-lookup"><span data-stu-id="a84f3-176">The value under the registry entry HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{PersistentHandlerGUID}\\PersistentAddinsRegistered\\ 89BCB740-6119-101A-BCB7-00DD010655AF yields the persistent handler GUID for this document type.</span></span> <span data-ttu-id="a84f3-177">Lasciare che la chiave sia {FilterHandlerCLSID}.</span><span class="sxs-lookup"><span data-stu-id="a84f3-177">Let this key be {FilterHandlerCLSID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. <span data-ttu-id="a84f3-178">Determinare il gestore di filtro: usando {FilterHandlerCLSID} che è stato determinato nel passaggio precedente, individuare il gestore di filtro sotto la voce \\ HKEY \_ Local \_ Machine \\ software \\ Classes \\ CLSID \\ {FilterHandlerCLSID} \\ InprocServer32.</span><span class="sxs-lookup"><span data-stu-id="a84f3-178">Determine the filter handler: using {FilterHandlerCLSID} that was determined in the previous step locate the filter handler under the entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{FilterHandlerCLSID}\\InprocServer32.</span></span> <span data-ttu-id="a84f3-179">In questo esempio il nome del gestore del filtro descrittivo usato è IFilter HTML.</span><span class="sxs-lookup"><span data-stu-id="a84f3-179">In this example the descriptive filter handler name used is HTML IFilter.</span></span>

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

## <a name="additional-resources"></a><span data-ttu-id="a84f3-180">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="a84f3-180">Additional Resources</span></span>

- <span data-ttu-id="a84f3-181">Nell'esempio di codice [IFilterSample](-search-sample-ifiltersample.md) , disponibile in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), viene illustrato come creare una classe di base [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) per implementare l'interfaccia **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="a84f3-181">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) base class for implementing the **IFilter** interface.</span></span>
- <span data-ttu-id="a84f3-182">Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a84f3-182">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="a84f3-183">Per una panoramica dei tipi di file, vedere [tipi di file](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a84f3-183">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="a84f3-184">Per eseguire query sugli attributi di associazione file per un tipo di file, vedere [PerceivedTypes, SystemFileAssociations e registrazione dell'applicazione](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a84f3-184">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a84f3-185">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a84f3-185">Related topics</span></span>

[<span data-ttu-id="a84f3-186">Sviluppo di gestori di filtri</span><span class="sxs-lookup"><span data-stu-id="a84f3-186">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="a84f3-187">Informazioni sui gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="a84f3-187">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="a84f3-188">Procedure consigliate per la creazione di gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="a84f3-188">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="a84f3-189">Restituzione di proprietà da un gestore di filtro</span><span class="sxs-lookup"><span data-stu-id="a84f3-189">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="a84f3-190">Gestori di filtri forniti con Windows</span><span class="sxs-lookup"><span data-stu-id="a84f3-190">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="a84f3-191">Implementazione di gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="a84f3-191">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="a84f3-192">Test di gestori filtro</span><span class="sxs-lookup"><span data-stu-id="a84f3-192">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
