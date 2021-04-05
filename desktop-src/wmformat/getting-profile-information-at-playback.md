---
title: Recupero delle informazioni sul profilo durante la riproduzione
description: Recupero delle informazioni sul profilo durante la riproduzione
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Media Format SDK, profili
- ASF (Advanced Systems Format), profili
- ASF (formato avanzato dei sistemi), profili
- Formato di sistemi avanzati (ASF), esclusione reciproca
- ASF (formato avanzato dei sistemi), esclusione reciproca
- ASF (Advanced Systems Format), condivisione della larghezza di banda
- ASF (formato avanzato dei sistemi), condivisione della larghezza di banda
- flussi, recupero di informazioni sul profilo durante la riproduzione
- profili, recupero di informazioni durante la riproduzione
- esclusione reciproca, recupero di informazioni sul profilo durante la riproduzione
- condivisione della larghezza di banda, recupero delle informazioni sul profilo durante la riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5c7083f7bf9e986e8a23ba2c78dfe4404942a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117387"
---
# <a name="getting-profile-information-at-playback"></a><span data-ttu-id="eac11-114">Recupero delle informazioni sul profilo durante la riproduzione</span><span class="sxs-lookup"><span data-stu-id="eac11-114">Getting Profile Information at Playback</span></span>

<span data-ttu-id="eac11-115">Le informazioni del profilo utilizzato per creare un file vengono archiviate nella sezione dell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="eac11-115">Information from the profile used to create a file is stored in the header section of the file.</span></span> <span data-ttu-id="eac11-116">Entrambi gli oggetti Reader possono accedere alle informazioni sul profilo dall'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="eac11-116">Both reader objects can access the profile information from the file header.</span></span> <span data-ttu-id="eac11-117">Esistono diversi motivi per cui è possibile che si desideri accedere ai dati del profilo dal reader.</span><span class="sxs-lookup"><span data-stu-id="eac11-117">There are several reasons why you might want to access profile data from the reader.</span></span> <span data-ttu-id="eac11-118">In genere, è necessario recuperare informazioni sui flussi, sugli oggetti di esclusione reciproca e sugli oggetti di condivisione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="eac11-118">Most commonly, you will need to retrieve information about streams, mutual exclusion objects, and bandwidth sharing objects.</span></span>

<span data-ttu-id="eac11-119">È possibile eseguire query sull'oggetto Reader asincrono e sull'oggetto Reader sincrono per l'interfaccia [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="eac11-119">Both the asynchronous reader object and the synchronous reader object can be queried for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="eac11-120">Nessuna modifica apportata alle informazioni sul profilo può avere alcun effetto sul file nel lettore.</span><span class="sxs-lookup"><span data-stu-id="eac11-120">No changes made to the profile information can have any affect on the file in the reader.</span></span> <span data-ttu-id="eac11-121">Per ulteriori informazioni sull'accesso alle informazioni sul profilo, vedere [utilizzo dei profili](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="eac11-121">For more information about accessing profile information, see [Working with Profiles](working-with-profiles.md).</span></span>

## <a name="stream-information"></a><span data-ttu-id="eac11-122">Informazioni sul flusso</span><span class="sxs-lookup"><span data-stu-id="eac11-122">Stream Information</span></span>

<span data-ttu-id="eac11-123">A volte è importante capire come viene configurato un flusso.</span><span class="sxs-lookup"><span data-stu-id="eac11-123">It is sometimes important to know how a stream is configured.</span></span> <span data-ttu-id="eac11-124">Quando si recuperano le proprietà dei supporti da uno degli oggetti Reader, si ottengono le proprietà degli output.</span><span class="sxs-lookup"><span data-stu-id="eac11-124">When you retrieve media properties from the either of the reader objects, you get the properties of the outputs.</span></span> <span data-ttu-id="eac11-125">Le proprietà di output descrivono il modo in cui i dati non compressi da un flusso verranno recapitati dal lettore, non come il flusso viene configurato nel file ASF.</span><span class="sxs-lookup"><span data-stu-id="eac11-125">Output properties describe how the uncompressed data from a stream is going to be delivered by the reader, not how the stream is configured within the ASF file.</span></span>

<span data-ttu-id="eac11-126">Quando si ricevono esempi di flusso non compressi da uno dei due oggetti Reader, è necessario usare le informazioni sul profilo per identificare il formato dei dati compressi.</span><span class="sxs-lookup"><span data-stu-id="eac11-126">When receiving uncompressed stream samples from either reader object, you must use the profile information to identify the format of the compressed data.</span></span> <span data-ttu-id="eac11-127">Questa operazione è particolarmente importante se si intende scrivere il flusso compresso in un altro file ASF.</span><span class="sxs-lookup"><span data-stu-id="eac11-127">This is particularly important if you are going to write the compressed stream to another ASF file.</span></span>

<span data-ttu-id="eac11-128">È anche necessario accedere alle informazioni sul flusso quando si usa la ricompressione intelligente per transcodificare un flusso audio a una velocità in bit più bassa.</span><span class="sxs-lookup"><span data-stu-id="eac11-128">You also need to access stream information when using smart recompression to transcode an audio stream to a lower bit rate.</span></span>

<span data-ttu-id="eac11-129">Potrebbe essere necessario determinare se un flusso è stato scritto utilizzando la codifica con velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="eac11-129">You may want to determine whether a stream was written using variable bit rate (VBR) encoding.</span></span> <span data-ttu-id="eac11-130">Non è possibile accedere alle informazioni di VBR dall'interfaccia **IWMProfile** di uno dei due oggetti Reader.</span><span class="sxs-lookup"><span data-stu-id="eac11-130">You cannot access any VBR information from the **IWMProfile** interface of either reader object.</span></span> <span data-ttu-id="eac11-131">Ciò è dovuto al fatto che le informazioni VBR non vengono archiviate nel file dopo la codifica.</span><span class="sxs-lookup"><span data-stu-id="eac11-131">This is because the VBR information is not stored in the file after encoding.</span></span> <span data-ttu-id="eac11-132">È possibile determinare se un flusso è stato creato usando la codifica VBR ottenendo un puntatore all'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) dell'oggetto Reader e chiamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="eac11-132">You can determine whether a stream was created using VBR encoding by obtaining a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface of the reader object and calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span> <span data-ttu-id="eac11-133">È necessario specificare il numero del flusso e passare g \_ wszIsVBR come nome dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="eac11-133">You must specify the stream number and pass g\_wszIsVBR as the attribute name.</span></span>

## <a name="mutual-exclusion-information"></a><span data-ttu-id="eac11-134">Informazioni sull'esclusione reciproca</span><span class="sxs-lookup"><span data-stu-id="eac11-134">Mutual Exclusion Information</span></span>

<span data-ttu-id="eac11-135">Se si desidera creare un'applicazione di lettura che utilizza l'esclusione reciproca, sarà necessario accedere alle informazioni sugli oggetti di esclusione reciproca inclusi nel profilo.</span><span class="sxs-lookup"><span data-stu-id="eac11-135">If you want to create a reading application that uses mutual exclusion, you will want to access the information about any mutual exclusion objects included in the profile.</span></span> <span data-ttu-id="eac11-136">Per tutti i tipi di esclusione reciproca ad eccezione della velocità in bit, l'applicazione di lettura è responsabile di qualsiasi cambio di flusso necessario.</span><span class="sxs-lookup"><span data-stu-id="eac11-136">For all mutual exclusion types except bit rate, the reading application is responsible for any stream switching that is required.</span></span> <span data-ttu-id="eac11-137">Per cambiare flusso, è necessario individuare i flussi.</span><span class="sxs-lookup"><span data-stu-id="eac11-137">To switch streams, you need to know which streams are which.</span></span>

## <a name="bandwidth-sharing-information"></a><span data-ttu-id="eac11-138">Informazioni sulla condivisione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="eac11-138">Bandwidth Sharing Information</span></span>

<span data-ttu-id="eac11-139">Gli oggetti di condivisione della larghezza di banda inclusi in un profilo sono inclusi solo a scopo informativo.</span><span class="sxs-lookup"><span data-stu-id="eac11-139">Bandwidth sharing objects that are included in a profile are included only for informational purposes.</span></span> <span data-ttu-id="eac11-140">Né l'oggetto writer né uno degli oggetti Reader esegue alcuna azione a causa dei dati di condivisione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="eac11-140">Neither the writer object nor either of the reader objects takes any action as a result of bandwidth sharing data.</span></span> <span data-ttu-id="eac11-141">Se si vuole usare la condivisione della larghezza di banda nell'applicazione di lettura, è necessario accedere alle informazioni di condivisione della larghezza di banda dai dati del profilo.</span><span class="sxs-lookup"><span data-stu-id="eac11-141">If you want to use bandwidth sharing in your reading application, you must access the bandwidth sharing information from the profile data.</span></span>

> [!Note]  
> <span data-ttu-id="eac11-142">Non tutte le informazioni del profilo utilizzato per creare un file sono presenti nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="eac11-142">Not all of the information from the profile used to create a file is present in the file header.</span></span> <span data-ttu-id="eac11-143">Come regola generale, i dati utilizzati solo al momento della codifica non vengono mantenuti nel file.</span><span class="sxs-lookup"><span data-stu-id="eac11-143">As a general rule, data that is used only at the time of encoding is not persisted in the file.</span></span> <span data-ttu-id="eac11-144">Sono incluse le impostazioni di input impostate tramite il metodo [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) e le proprietà impostate utilizzando il metodo [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="eac11-144">This includes input settings that were set using the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method, as well as properties set using the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eac11-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eac11-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eac11-146">**Interfaccia IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="eac11-146">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="eac11-147">**Lettura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="eac11-147">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




