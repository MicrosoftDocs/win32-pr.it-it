---
title: Convenzione di processo di Windows Media Player BITS
description: Windows Media Player può scaricare e aggiungere automaticamente elementi multimediali digitali alla libreria se si usa Servizio trasferimento intelligente in background (BITS).
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Windows Media Player Online Stores, Servizio trasferimento intelligente in background (BITS)
- archivi online, Servizio trasferimento intelligente in background (BITS)
- digitare 2 archivi online, Servizio trasferimento intelligente in background (BITS)
- Servizio trasferimento intelligente in background (BITS)
- BITS (Servizio trasferimento intelligente in background)
- Windows Media Player Online Stores, convenzione del processo BITS
- negozi online, convenzione del processo BITS
- tipi 2 negozi online, convenzione del processo BITS
- Convenzione del processo BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223992"
---
# <a name="windows-media-player-bits-job-convention"></a><span data-ttu-id="55d6a-112">Convenzione di processo di Windows Media Player BITS</span><span class="sxs-lookup"><span data-stu-id="55d6a-112">Windows Media Player BITS Job Convention</span></span>

<span data-ttu-id="55d6a-113">Windows Media Player può scaricare e aggiungere automaticamente elementi multimediali digitali alla libreria se si usa [servizio trasferimento intelligente in background (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span><span class="sxs-lookup"><span data-stu-id="55d6a-113">Windows Media Player can automatically download and add digital media items to the library if you use [Background Intelligent Transfer Service (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span></span> <span data-ttu-id="55d6a-114">Per sfruttare i vantaggi di questa funzionalità, è necessario aggiungere il processo alla coda di trasferimento BITS e chiamare **Metodo ibackgroundcopyjob:: FileDescription**, specificando una stringa di descrizione che utilizza il formato corretto.</span><span class="sxs-lookup"><span data-stu-id="55d6a-114">To take advantage of this feature, you must add your job to the BITS transfer queue and call **IBackgroundCopyJob::SetDescription**, providing a description string that uses the correct format.</span></span>

> [!Note]  
> <span data-ttu-id="55d6a-115">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="55d6a-115">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="55d6a-116">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="55d6a-116">Use of this functionality outside the context of an online store is not supported.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="55d6a-117">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55d6a-117">Syntax</span></span>

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a><span data-ttu-id="55d6a-118">Parametri</span><span class="sxs-lookup"><span data-stu-id="55d6a-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55d6a-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span><span class="sxs-lookup"><span data-stu-id="55d6a-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span></span>
</dt> <dd>

<span data-ttu-id="55d6a-120">Valore a 32 bit generato in modo casuale che Windows Media Player utilizza per identificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="55d6a-120">A randomly generated 32-bit value that Windows Media Player uses to identify the service.</span></span>

</dd> <dt>

<span data-ttu-id="55d6a-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Provider*</span><span class="sxs-lookup"><span data-stu-id="55d6a-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Provider*</span></span>
</dt> <dd>

<span data-ttu-id="55d6a-122">Nome provider.</span><span class="sxs-lookup"><span data-stu-id="55d6a-122">The provider name.</span></span> <span data-ttu-id="55d6a-123">Questo valore deve corrispondere a un nome di chiave di archivio online valido.</span><span class="sxs-lookup"><span data-stu-id="55d6a-123">This value must match a valid online store key name.</span></span>

</dd> <dt>

<span data-ttu-id="55d6a-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span><span class="sxs-lookup"><span data-stu-id="55d6a-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span></span>
</dt> <dd>

<span data-ttu-id="55d6a-125">Nome dell'artista principale per l'album.</span><span class="sxs-lookup"><span data-stu-id="55d6a-125">The name of the primary artist for the album.</span></span>

</dd> <dt>

<span data-ttu-id="55d6a-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*</span><span class="sxs-lookup"><span data-stu-id="55d6a-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*</span></span>
</dt> <dd>

<span data-ttu-id="55d6a-127">Titolo dell'album.</span><span class="sxs-lookup"><span data-stu-id="55d6a-127">The title of the album.</span></span>

</dd> <dt>

<span data-ttu-id="55d6a-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*Numero*</span><span class="sxs-lookup"><span data-stu-id="55d6a-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*</span></span>
</dt> <dd>

<span data-ttu-id="55d6a-129">Numero di traccia del CD.</span><span class="sxs-lookup"><span data-stu-id="55d6a-129">The CD track number.</span></span>

</dd> <dt>

<span data-ttu-id="55d6a-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Titolo*</span><span class="sxs-lookup"><span data-stu-id="55d6a-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Title*</span></span>
</dt> <dd>

<span data-ttu-id="55d6a-131">Titolo del contenuto.</span><span class="sxs-lookup"><span data-stu-id="55d6a-131">The title of the content.</span></span>

</dd> <dt>

<span data-ttu-id="55d6a-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Durata*</span><span class="sxs-lookup"><span data-stu-id="55d6a-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Duration*</span></span>
</dt> <dd>

<span data-ttu-id="55d6a-133">Durata del contenuto.</span><span class="sxs-lookup"><span data-stu-id="55d6a-133">The duration of the content.</span></span>

</dd> <dt>

<span data-ttu-id="55d6a-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Classificazione*</span><span class="sxs-lookup"><span data-stu-id="55d6a-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Rating*</span></span>
</dt> <dd>

<span data-ttu-id="55d6a-135">Classificazione per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="55d6a-135">The rating for the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55d6a-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="55d6a-136">Remarks</span></span>

<span data-ttu-id="55d6a-137">Quando Windows Media Player 10 o versioni successive USA BITS per scaricare il contenuto, enumera i processi nella coda di trasferimento ed esamina la stringa di descrizione per ogni processo.</span><span class="sxs-lookup"><span data-stu-id="55d6a-137">When Windows Media Player 10 or later uses BITS to download content, it enumerates the jobs in the transfer queue and inspects the description string for each job.</span></span> <span data-ttu-id="55d6a-138">Se la stringa di descrizione corrisponde alla convenzione prevista, Windows Media Player Scarica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="55d6a-138">If the description string matches the expected convention, Windows Media Player downloads the content.</span></span>

<span data-ttu-id="55d6a-139">È necessario aggiungere un solo file multimediale digitale per il download a ogni processo BITS.</span><span class="sxs-lookup"><span data-stu-id="55d6a-139">You must add only one digital media file for download to each BITS job.</span></span>

<span data-ttu-id="55d6a-140">Dopo aver avviato un processo BITS utilizzando questa convenzione, è necessario consentire a Windows Media Player di completare il processo.</span><span class="sxs-lookup"><span data-stu-id="55d6a-140">After you start a BITS job using this convention, you must let Windows Media Player complete the job.</span></span> <span data-ttu-id="55d6a-141">Windows Media Player rimuoverà anche il processo dalla coda BITS, sposterà il file scaricato nel percorso in cui è stata salvata la musica rippata e aggiungerà il file scaricato alla libreria.</span><span class="sxs-lookup"><span data-stu-id="55d6a-141">Windows Media Player will also remove the job from the BITS queue, move the downloaded file to the location where ripped music is saved, and add the downloaded file to the library.</span></span>

<span data-ttu-id="55d6a-142">Il parametro *ServiceID* deve contenere un valore diverso da zero a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="55d6a-142">The *serviceId* parameter must contain a nonzero 32-bit value.</span></span> <span data-ttu-id="55d6a-143">Per creare questo valore, è consigliabile usare la funzione [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) .</span><span class="sxs-lookup"><span data-stu-id="55d6a-143">We recommend that you use the function [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) to create this value.</span></span>

<span data-ttu-id="55d6a-144">Il nome file specificato con il parametro *localName* di **Metodo ibackgroundcopyjob:: AddFile** deve avere un'estensione di file WMA, WMV, MP3 o ASF.</span><span class="sxs-lookup"><span data-stu-id="55d6a-144">The file name you specify using the *localName* parameter of **IBackgroundCopyJob::AddFile** must have a .wma, .wmv, .mp3, or .asf file name extension.</span></span>

<span data-ttu-id="55d6a-145">I parametri rimanenti sono progettati per contenere i valori dei metadati correlati al contenuto.</span><span class="sxs-lookup"><span data-stu-id="55d6a-145">The remaining parameters are designed to contain metadata values related to the content.</span></span> <span data-ttu-id="55d6a-146">È possibile recuperare questi valori dalla pagina Web del negozio online usando **DownloadItem. GetItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="55d6a-146">You can retrieve these values from your online store webpage by using **DownloadItem.getItemInfo**.</span></span> <span data-ttu-id="55d6a-147">È possibile recuperare la raccolta di download corretta chiamando **downloadmanager. Getdownloadcollection** e specificando *ServiceID* come parametro *CollectionId* .</span><span class="sxs-lookup"><span data-stu-id="55d6a-147">You can retrieve the correct download collection by calling **DownloadManager.getDownloadCollection** and providing *serviceId* as the *collectionId* parameter.</span></span>

<span data-ttu-id="55d6a-148">Windows Media Player controlla periodicamente la coda BITS mentre il lettore è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="55d6a-148">Windows Media Player inspects the BITS queue periodically while the Player is running.</span></span> <span data-ttu-id="55d6a-149">Per assicurarsi che Windows Media Player controlli la coda BITS per i processi di download, è necessario creare un valore nella seguente sottochiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="55d6a-149">To ensure that Windows Media Player checks the BITS queue for download jobs, you should create a value in the following registry subkey:</span></span>

<span data-ttu-id="55d6a-150">**HKEY \_ \_ software utente \\ corrente \\ Microsoft \\ MediaPlayer \\ Services**</span><span class="sxs-lookup"><span data-stu-id="55d6a-150">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Services**</span></span>

<span data-ttu-id="55d6a-151">Il valore deve essere creato nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="55d6a-151">The value should be created as follows.</span></span>



| <span data-ttu-id="55d6a-152">Nome</span><span class="sxs-lookup"><span data-stu-id="55d6a-152">Name</span></span>                | <span data-ttu-id="55d6a-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="55d6a-153">Type</span></span>      | <span data-ttu-id="55d6a-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55d6a-154">Description</span></span>                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d6a-155">**RefreshDownload**</span><span class="sxs-lookup"><span data-stu-id="55d6a-155">**RefreshDownload**</span></span> | <span data-ttu-id="55d6a-156">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="55d6a-156">**DWORD**</span></span> | <span data-ttu-id="55d6a-157">Specifica se Windows Media Player deve controllare la coda BITS per i processi di download.</span><span class="sxs-lookup"><span data-stu-id="55d6a-157">Specifies whether Windows Media Player should inspect the BITS queue for download jobs.</span></span> <span data-ttu-id="55d6a-158">Se il valore è zero, il lettore non verificherà la coda BITS.</span><span class="sxs-lookup"><span data-stu-id="55d6a-158">If the value is zero, the Player will not inspect the BITS queue.</span></span> <span data-ttu-id="55d6a-159">Il lettore deve controllare la coda se il valore è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="55d6a-159">The Player must inspect the queue if the value is nonzero.</span></span> |



 

<span data-ttu-id="55d6a-160">È possibile utilizzare la sintassi alternativa seguente per aggiungere processi BITS non completati da Windows Media Player, ma per i quali vengono semplicemente visualizzate le informazioni sullo stato:</span><span class="sxs-lookup"><span data-stu-id="55d6a-160">You can use the following alternate syntax to add BITS jobs that Windows Media Player does not complete, but for which it simply shows status information:</span></span>

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

<span data-ttu-id="55d6a-161">Quando si usa la sintassi precedente, è necessario scrivere il codice per completare il download dei bit, organizzare il contenuto nel computer dell'utente e aggiungere il contenuto alla libreria, se necessario.</span><span class="sxs-lookup"><span data-stu-id="55d6a-161">When you use the preceding syntax, you must write code to complete the BITS download, organize the content on the user's computer, and add the content to the library, if desired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55d6a-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55d6a-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55d6a-163">CryptGenRandom</span><span class="sxs-lookup"><span data-stu-id="55d6a-163">CryptGenRandom</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[<span data-ttu-id="55d6a-164">**DownloadItem. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="55d6a-164">**DownloadItem.getItemInfo**</span></span>](downloaditem-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="55d6a-165">**DownloadManager. getdownloadcollection**</span><span class="sxs-lookup"><span data-stu-id="55d6a-165">**DownloadManager.getDownloadCollection**</span></span>](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="55d6a-166">**Riferimento per negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="55d6a-166">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 