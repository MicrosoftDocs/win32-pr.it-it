---
title: Enumerazione di file e directory
description: Viene descritto il modo in cui un provider ProjFS partecipa all'enumerazione di directory.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: e0712ceb927388b090a84a89f80f0e2d3a1befbb
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2020
ms.locfileid: "103723991"
---
# <a name="enumerating-files-and-directories"></a><span data-ttu-id="42ac4-103">Enumerazione di file e directory</span><span class="sxs-lookup"><span data-stu-id="42ac4-103">Enumerating Files and Directories</span></span>

<span data-ttu-id="42ac4-104">Quando un provider crea innanzitutto una radice di virtualizzazione, è vuota nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="42ac4-104">When a provider first creates a virtualization root it is empty on the local system.</span></span>  <span data-ttu-id="42ac4-105">Ovvero, nessuno degli elementi nell'archivio dati di supporto è ancora stato memorizzato nella cache su disco.</span><span class="sxs-lookup"><span data-stu-id="42ac4-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span>  <span data-ttu-id="42ac4-106">Poiché ogni elemento viene aperto, viene memorizzato nella cache, ma fino a quando non viene aperto un elemento esiste solo nell'archivio dati di supporto.</span><span class="sxs-lookup"><span data-stu-id="42ac4-106">As each item is opened it is cached, but until an item is opened it only exists in the backing data store.</span></span>

<span data-ttu-id="42ac4-107">Poiché gli elementi non aperti non hanno una presenza locale, l'enumerazione di directory normale non rivelerà l'esistenza dell'utente.</span><span class="sxs-lookup"><span data-stu-id="42ac4-107">Since unopened items have no local presence, normal directory enumeration would not reveal their existence to the user.</span></span>  <span data-ttu-id="42ac4-108">Pertanto, il provider deve partecipare all'enumerazione di directory restituendo le informazioni a ProjFS sugli elementi nell'archivio dati di supporto.</span><span class="sxs-lookup"><span data-stu-id="42ac4-108">Therefore the provider must participate in directory enumeration by returning information to ProjFS about items in its backing data store.</span></span>  <span data-ttu-id="42ac4-109">ProjFS unisce le informazioni del provider con le informazioni sul file system locale per presentare all'utente un elenco unificato del contenuto di una directory.</span><span class="sxs-lookup"><span data-stu-id="42ac4-109">ProjFS merges the information from the provider with what is on the local file system to present to the user a unified list of the contents of a directory.</span></span>

## <a name="directory-enumeration-callbacks"></a><span data-ttu-id="42ac4-110">Callback di enumerazione directory</span><span class="sxs-lookup"><span data-stu-id="42ac4-110">Directory Enumeration Callbacks</span></span>

<span data-ttu-id="42ac4-111">Per partecipare all'enumerazione di directory, il provider deve implementare i callback **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** e **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** .</span><span class="sxs-lookup"><span data-stu-id="42ac4-111">To participate in directory enumeration the provider must implement the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)**, and **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** callbacks.</span></span>  <span data-ttu-id="42ac4-112">Quando viene enumerata una directory sotto la radice di virtualizzazione del provider, ProjFS esegue le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="42ac4-112">When a directory under the provider's virtualization root gets enumerated, ProjFS performs the following actions:</span></span>

1. <span data-ttu-id="42ac4-113">ProjFS chiama il callback **PRJ_START_DIRECTORY_ENUMERATION_CB** del provider per avviare una sessione di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="42ac4-113">ProjFS calls the provider's **PRJ_START_DIRECTORY_ENUMERATION_CB** callback to start an enumeration session.</span></span>

    <span data-ttu-id="42ac4-114">Come parte dell'elaborazione di questo callback, il provider deve prepararsi a eseguire l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="42ac4-114">As part of processing this callback the provider should prepare to perform the enumeration.</span></span>  <span data-ttu-id="42ac4-115">Ad esempio, deve allocare la memoria necessaria per tenere traccia dello stato di avanzamento dell'enumerazione nell'archivio dati di supporto.</span><span class="sxs-lookup"><span data-stu-id="42ac4-115">For example, it should allocate any memory it may need to track the progress of the enumeration in its backing data store.</span></span>

    <span data-ttu-id="42ac4-116">ProjFS identifica la directory enumerata nel membro **FilePathName** del parametro _callBackData_ del callback.</span><span class="sxs-lookup"><span data-stu-id="42ac4-116">ProjFS identifies the directory being enumerated in the **FilePathName** member of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="42ac4-117">Viene specificato come percorso relativo alla radice di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="42ac4-117">This is specified as a path relative to the virtualization root.</span></span>  <span data-ttu-id="42ac4-118">Se ad esempio la radice di virtualizzazione si trova in `C:\virtRoot` e la directory enumerata è `C:\virtRoot\dir1\dir2` , il membro **FilePathName** conterrà `dir1\dir2` .</span><span class="sxs-lookup"><span data-stu-id="42ac4-118">For example, if the virtualization root is located at `C:\virtRoot`, and the directory being enumerated is `C:\virtRoot\dir1\dir2`, the **FilePathName** member will contain `dir1\dir2`.</span></span>  <span data-ttu-id="42ac4-119">Il provider si prepara a enumerare il percorso nell'archivio dati di supporto.</span><span class="sxs-lookup"><span data-stu-id="42ac4-119">The provider will prepare to enumerate that path in its backing data store.</span></span>  <span data-ttu-id="42ac4-120">A seconda delle funzionalità dell'archivio di backup di un provider, può essere utile eseguire l'enumerazione dell'archivio di backup nel callback **PRJ_START_DIRECTORY_ENUMERATION_CB** .</span><span class="sxs-lookup"><span data-stu-id="42ac4-120">Depending on the capabilities of a provider's backing store it may make sense to perform the backing store enumeration in the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback.</span></span>

    <span data-ttu-id="42ac4-121">Poiché più enumerazioni possono essere eseguite in parallelo nella stessa directory, ogni callback di enumerazione ha un argomento _enumerationId_ per consentire al provider di associare le chiamate di callback in una singola sessione di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="42ac4-121">Because multiple enumerations may occur in parallel in the same directory, each enumeration callback has an _enumerationId_ argument to enable the provider to associate the callback invocations into a single enumeration session.</span></span>

    <span data-ttu-id="42ac4-122">Se il provider restituisce S_OK dal callback **PRJ_START_DIRECTORY_ENUMERATION_CB** , deve gestire tutte le informazioni sulla sessione di enumerazione che possiede fino a quando ProjFS richiama il callback **PRJ_END_DIRECTORY_ENUMERATION_CB** con lo stesso valore per _enumerationId_.</span><span class="sxs-lookup"><span data-stu-id="42ac4-122">If the provider returns S_OK from the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback, it must maintain any enumeration session information it has until ProjFS invokes the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback with the same value for _enumerationId_.</span></span>  <span data-ttu-id="42ac4-123">Se il provider restituisce un errore da **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS non richiama il callback **PRJ_END_DIRECTORY_ENUMERATION_CB** per tale _enumerationId_.</span><span class="sxs-lookup"><span data-stu-id="42ac4-123">If the provider returns an error from **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS will not invoke the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback for that _enumerationId_.</span></span>

1. <span data-ttu-id="42ac4-124">ProjFS chiama il callback **PRJ_GET_DIRECTORY_ENUMERATION_CB** del provider una o più volte per ottenere il contenuto della directory dal provider.</span><span class="sxs-lookup"><span data-stu-id="42ac4-124">ProjFS calls the provider's **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback one or more times to get the directory contents from the provider.</span></span>

    <span data-ttu-id="42ac4-125">In risposta a questo callback, il provider restituisce un elenco ordinato di elementi dall'archivio dati di supporto.</span><span class="sxs-lookup"><span data-stu-id="42ac4-125">In response to this callback the provider returns a sorted list of items from its backing data store.</span></span>

    <span data-ttu-id="42ac4-126">Il callback può fornire un'espressione di ricerca nel parametro _searchExpression_ che il provider USA per definire l'ambito dei risultati dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="42ac4-126">The callback may provide a search expression in its _searchExpression_ parameter that the provider uses to scope the results of the enumeration.</span></span>  <span data-ttu-id="42ac4-127">Se _searchExpression_ è null, il provider restituisce tutte le voci della directory enumerata.</span><span class="sxs-lookup"><span data-stu-id="42ac4-127">If _searchExpression_ is NULL, the provider returns all the entries in the directory being enumerated.</span></span>  <span data-ttu-id="42ac4-128">Se è diverso da NULL, il provider può utilizzare **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** per determinare se sono presenti caratteri jolly nell'espressione.</span><span class="sxs-lookup"><span data-stu-id="42ac4-128">If it is non-NULL, the provider can use **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** to determine whether there are wildcards in the expression.</span></span>  <span data-ttu-id="42ac4-129">In tal caso, il provider utilizza **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** per determinare se una voce nella directory corrisponde all'espressione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="42ac4-129">If there are, the provider uses **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** to determine whether an entry in the directory matches the search expression.</span></span>

    <span data-ttu-id="42ac4-130">Il provider deve acquisire il valore di _searchExpression_ alla prima chiamata di questo callback.</span><span class="sxs-lookup"><span data-stu-id="42ac4-130">The provider should capture the value of _searchExpression_ on the first invocation of this callback.</span></span>  <span data-ttu-id="42ac4-131">Usa il valore acquisito per qualsiasi chiamata successiva del callback nella stessa sessione di enumerazione, a meno che PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN non sia impostato nel campo dei **flag** del parametro _callBackData_ del callback.</span><span class="sxs-lookup"><span data-stu-id="42ac4-131">It uses the captured value on any subsequent invocation of the callback in the same enumeration session, unless PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN is set in the **Flags** field of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="42ac4-132">In tal caso, è necessario riacquisire il valore di _searchExpression_.</span><span class="sxs-lookup"><span data-stu-id="42ac4-132">In that case it should recapture the value of _searchExpression_.</span></span>

    <span data-ttu-id="42ac4-133">Se non sono presenti voci corrispondenti nell'archivio di backup, il provider restituisce semplicemente S_OK dal callback.</span><span class="sxs-lookup"><span data-stu-id="42ac4-133">If there are no matching entries in its backing store, the provider simply returns S_OK from the callback.</span></span>  <span data-ttu-id="42ac4-134">In caso contrario, il provider formatta ogni voce corrispondente dal relativo archivio di backup in una struttura **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** , quindi utilizza **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** per riempire il buffer fornito dal parametro _dirEntryBufferHandle_ del callback.</span><span class="sxs-lookup"><span data-stu-id="42ac4-134">Otherwise the provider formats each matching entry from its backing store into a **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** structure, and then uses **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="42ac4-135">Il provider continua ad aggiungere voci fino a quando non vengono aggiunte tutte o fino a quando **PrjFillDirEntryBuffer** non restituisce HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER).</span><span class="sxs-lookup"><span data-stu-id="42ac4-135">The provider keeps adding entries until it has added them all or until **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER).</span></span>  <span data-ttu-id="42ac4-136">Il provider restituisce quindi S_OK dal callback.</span><span class="sxs-lookup"><span data-stu-id="42ac4-136">Then the provider returns S_OK from the callback.</span></span>  <span data-ttu-id="42ac4-137">Si noti che il provider deve aggiungere le voci al buffer _dirEntryBufferHandle_ nell'ordinamento corretto.</span><span class="sxs-lookup"><span data-stu-id="42ac4-137">Note that the provider must add the entries to the _dirEntryBufferHandle_ buffer in the correct sort order.</span></span>  <span data-ttu-id="42ac4-138">Il provider deve usare **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** per determinare il tipo di ordinamento corretto.</span><span class="sxs-lookup"><span data-stu-id="42ac4-138">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** to determine the correct sort order.</span></span>

    > <span data-ttu-id="42ac4-139">Il provider deve fornire un valore per il membro della **directory** di **PRJ_FILE_BASIC_INFO**.</span><span class="sxs-lookup"><span data-stu-id="42ac4-139">The provider must supply a value for the **IsDirectory** member of **PRJ_FILE_BASIC_INFO**.</span></span>  <span data-ttu-id="42ac4-140">Se la **directory** è false, il provider deve fornire anche un valore per il membro **Filesize** .</span><span class="sxs-lookup"><span data-stu-id="42ac4-140">If **IsDirectory** is FALSE, the provider must also supply a value for the **FileSize** member.</span></span>
    >
    > <span data-ttu-id="42ac4-141">Se il provider non fornisce valori per i membri **creationTime**, **LastAccessTime**, **LastWriteTime** e **ChangeTime** , ProjFS utilizzerà l'ora di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="42ac4-141">If the provider does not supply values for the **CreationTime**, **LastAccessTime**, **LastWriteTime**, and **ChangeTime** members, ProjFS will use the current system time.</span></span>
    >
    > <span data-ttu-id="42ac4-142">ProjFS utilizzerà qualsiasi FILE_ATTRIBUTE flag che il provider imposta nel membro **FileAttributes** ad eccezione di FILE_ATTRIBUTE_DIRECTORY; il valore corretto per FILE_ATTRIBUTE_DIRECTORY nel membro **FileAttributes** verrà impostato in base al valore fornito del membro di **directory** .</span><span class="sxs-lookup"><span data-stu-id="42ac4-142">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileAttributes** member except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileAttributes** member according to the supplied value of the **IsDirectory** member.</span></span>

    <span data-ttu-id="42ac4-143">Se **PrjFillDirEntryBuffer** restituisce HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) prima che il provider esaurisca le voci da aggiungere, il provider deve tenere traccia della voce che stava tentando di aggiungere quando ha ricevuto l'errore.</span><span class="sxs-lookup"><span data-stu-id="42ac4-143">If **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) before the provider runs out of entries to add to it, the provider must keep track of the entry it was trying to add when it received the error.</span></span>  <span data-ttu-id="42ac4-144">La volta successiva che ProjFS chiama il callback **PRJ_GET_DIRECTORY_ENUMERATION_CB** per la stessa sessione di enumerazione, il provider deve riprendere l'aggiunta di voci al buffer _dirEntryBufferHandle_ con la voce che stava tentando di aggiungere.</span><span class="sxs-lookup"><span data-stu-id="42ac4-144">The next time ProjFS calls the **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback for the same enumeration session, the provider must resume adding entries to the _dirEntryBufferHandle_ buffer with the entry it was trying to add.</span></span>

    > <span data-ttu-id="42ac4-145">Se l'archivio di backup supporta i collegamenti simbolici, il provider deve usare **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** per riempire il buffer fornito dal parametro _dirEntryBufferHandle_ del callback.</span><span class="sxs-lookup"><span data-stu-id="42ac4-145">If the backing store supports symbolic links, the provider must use **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="42ac4-146">**PrjFillDirEntryBuffer2** supporta un input del buffer aggiuntivo che consente al provider di specificare che la voce di enumerazione è un collegamento simbolico e la relativa destinazione.</span><span class="sxs-lookup"><span data-stu-id="42ac4-146">**PrjFillDirEntryBuffer2** supports an extra buffer input that allows the provider to specify that the enumeration entry is a symbolic link and what its target is.</span></span>  <span data-ttu-id="42ac4-147">In caso contrario, si comporta come descritto in precedenza per **PrjFillDirEntryBuffer**.</span><span class="sxs-lookup"><span data-stu-id="42ac4-147">It otherwise behaves as described above for **PrjFillDirEntryBuffer**.</span></span>  <span data-ttu-id="42ac4-148">Nell'esempio seguente viene usato **PrjFillDirEntryBuffer2** per illustrare il supporto dei collegamenti simbolici.</span><span class="sxs-lookup"><span data-stu-id="42ac4-148">The following sample uses **PrjFillDirEntryBuffer2** to illustrate support for symbolic links.</span></span>
    >
    > <span data-ttu-id="42ac4-149">Si noti che **PrjFillDirEntryBuffer2** è supportato a partire da Windows 10, versione 2004.</span><span class="sxs-lookup"><span data-stu-id="42ac4-149">Note that **PrjFillDirEntryBuffer2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="42ac4-150">Un provider deve verificare l'esistenza di **PrjFillDirEntryBuffer2**, ad esempio usando **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span><span class="sxs-lookup"><span data-stu-id="42ac4-150">A provider should probe for the existence of **PrjFillDirEntryBuffer2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

    ```C++
    typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

    typedef struct MY_ENUM_ENTRY {
        MY_ENUM_ENTRY* Next;
        PWSTR Name;
        BOOLEAN IsDirectory;
        INT64 FileSize;
        BOOLEAN IsSymlink;
        PWSTR SymlinkTarget;
    } MY_ENUM_ENTRY;

    typedef struct MY_ENUM_SESSION {
        GUID EnumerationId;
        PWSTR SearchExpression;
        USHORT SearchExpressionMaxLen;
        BOOLEAN SearchExpressionCaptured;
        MY_ENUM_ENTRY* EnumHead;
        MY_ENUM_ENTRY* LastEnumEntry;
        BOOLEAN EnumCompleted;
    } MY_ENUM_SESSION;

    HRESULT
    MyGetEnumCallback(
        _In_ const PRJ_CALLBACK_DATA* callbackData,
        _In_ const GUID* enumerationId,
        _In_opt_z_ PCWSTR searchExpression,
        _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
        )
    {
        // MyGetEnumSession is a routine the provider might implement to find
        // information about the enumeration session that it first stored
        // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
        //
        // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
        // already retrieved a list of the items in the backing store located at
        // callbackData->FilePathName, sorted them using PrjFileNameCompare()
        // to determine collation order, and stored the list in session->EnumHead.
        MY_ENUM_SESSION* session = NULL;
        session = MyGetEnumSession(enumerationId);

        if (session == NULL)
        {
            return HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        }

        if (!session->SearchExpressionCaptured ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            if (searchExpression != NULL)
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              searchExpression,
                              wcslen(searchExpression)))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            else
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              "*",
                              1))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            session->SearchExpressionCaptured = TRUE;
        }

        MY_ENUM_ENTRY* enumHead = NULL;

        // We have to start the enumeration from the beginning if we aren't
        // continuing an existing session or if the caller is requesting a restart.
        if (((session->LastEnumEntry == NULL) &&
             !session->EnumCompleted) ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            // Ensure that if the caller is requesting a restart we reset our
            // bookmark of how far we got in the enumeration.
            session->LastEnumEntry = NULL;

            // In case we're restarting ensure we don't think we're done.
            session->EnumCompleted = FALSE;

            // We need to start considering items from the beginning of the list
            // retrieved from the backing store.
            enumHead = session->EnumHead;
        }
        else
        {
            // We are resuming an existing enumeration session.  Note that
            // session->LastEnumEntry may be NULL.  That is okay; it means
            // we got all the entries the last time this callback was invoked.
            // Returning S_OK without adding any new entries to the
            // dirEntryBufferHandle buffer signals ProjFS that the enumeration
            // has returned everything it can.
            enumHead = session->LastEnumEntry;
        }

        if (enumHead == NULL)
        {
            // There are no items to return.  Remember that we've returned everything
            // we can.
            session->EnumCompleted = TRUE;
        }
        else
        {
            MY_ENUM_ENTRY* thisEntry = enumHead;
            while (thisEntry != NULL)
            {
                // We'll insert the entry into the return buffer if it matches
                // the search expression captured for this enumeration session.
                if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
                {
                    PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                    fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                    fileBasicInfo.FileSize = thisEntry->FileSize;

                    // If our backing store says this is really a symbolic link,
                    // set up to tell ProjFS that it is a symlink and what its
                    // target is.
                    PRJ_EXTENDED_INFO extraInfo = {};
                    if (thisEntry->IsSymlink)
                    {
                        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
                        extraInfo.Symlink.TargetName = thisEntry->SymlinkTarget;
                    }

                    // Format the entry for return to ProjFS.
                    HRESULT fillResult = PrjFillDirEntryBuffer2(dirEntryBufferHandle,
                                                                thisEntry->Name,
                                                                &fileBasicInfo,
                                                                thisEntry->IsSymlink ? &extraInfo : NULL);

                    if (fillResult == HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER))
                    {
                        // We couldn't add this entry to the buffer; remember where we left
                        // off for the next time we're called for this enumeration session.
                        session->LastEnumEntry = thisEntry;
                        return S_OK;
                    }
                }

                thisEntry = thisEntry->Next;
            }

            // We reached the end of the list of entries; remember that we've returned
            // everything we can.
            session->EnumCompleted = TRUE;
        }

        return S_OK;
    }
    ```

1. <span data-ttu-id="42ac4-151">ProjFS chiama il callback **PRJ_END_DIRECTORY_ENUMERATION_CB** del provider per terminare la sessione di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="42ac4-151">ProjFS calls the provider's **PRJ_END_DIRECTORY_ENUMERATION_CB** callback to end the enumeration session.</span></span>

    <span data-ttu-id="42ac4-152">Il provider deve eseguire tutte le operazioni di pulizia necessarie per terminare la sessione di enumerazione, ad esempio deallocare la memoria allocata come parte dell'elaborazione **PRJ_START_DIRECTORY_ENUMERATION_CB**.</span><span class="sxs-lookup"><span data-stu-id="42ac4-152">The provider should perform any cleanup it needs to do to end the enumeration session, such as deallocate memory allocated as part of processing **PRJ_START_DIRECTORY_ENUMERATION_CB**.</span></span>
