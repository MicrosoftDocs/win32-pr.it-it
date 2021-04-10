---
title: Uso di High-Resolution audio PCM
description: Uso di High-Resolution audio PCM
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- ASF (Advanced Systems Format), audio PCM a risoluzione elevata
- ASF (Advanced Systems Format), audio PCM ad alta risoluzione
- profili, audio PCM ad alta risoluzione
- codec, audio PCM ad alta risoluzione
- ASF (Advanced Systems Format), audio PCM
- ASF (formato avanzato dei sistemi), audio PCM
- profili, audio PCM
- codec, audio PCM
- audio PCM ad alta risoluzione
- Audio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963198"
---
# <a name="working-with-high-resolution-pcm-audio"></a><span data-ttu-id="b2e3d-113">Uso di High-Resolution audio PCM</span><span class="sxs-lookup"><span data-stu-id="b2e3d-113">Working with High-Resolution PCM Audio</span></span>

<span data-ttu-id="b2e3d-114">Alcuni formati di input per il codec Windows Media Audio 9 Professional e il codec Windows Media Audio 9 Lossless sono formati PCM ad alta risoluzione.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-114">Some of the input formats for the Windows Media Audio 9 Professional codec and the Windows Media Audio 9 Lossless codec are high-resolution PCM formats.</span></span> <span data-ttu-id="b2e3d-115">Si tratta di formati PCM con più di due canali o più di 16 bit per campione (l'audio con più di due canali è denominato anche audio multicanale).</span><span class="sxs-lookup"><span data-stu-id="b2e3d-115">These are PCM formats that have more than two channels, or more than 16 bits per sample (audio with more than two channels is also called multichannel audio).</span></span>

<span data-ttu-id="b2e3d-116">Questi formati sono configurati utilizzando un'estensione strutturata della struttura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) , denominata [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b2e3d-116">These formats are configured by using a structured extension of the [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) structure, called [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span></span> <span data-ttu-id="b2e3d-117">La struttura **WAVEFORMATEXTENSIBLE** include informazioni sui canali inclusi nell'audio.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-117">The **WAVEFORMATEXTENSIBLE** structure includes information about the channels included in the audio.</span></span> <span data-ttu-id="b2e3d-118">Questa struttura è obbligatoria quando si usa audio PCM ad alta risoluzione, perché alcune API Windows non accettano strutture **WAVEFORMATEX** che contengono valori ad alta risoluzione.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-118">This structure is required when using high-resolution PCM audio, because some Windows APIs will not accept **WAVEFORMATEX** structures that contain high-resolution values.</span></span>

<span data-ttu-id="b2e3d-119">I formati PCM ad alta risoluzione hanno 22 byte di dati estesi, specificati nel membro **cbSize** della struttura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="b2e3d-119">High-resolution PCM formats have 22 bytes of extended data, which is specified in the **cbSize** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="b2e3d-120">I formati audio Windows Media ad alta risoluzione non usano la struttura **WAVEFORMATEXTENSIBLE** , ma hanno dati estesi aggiunti alla struttura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="b2e3d-120">High-resolution Windows Media audio formats do not use the **WAVEFORMATEXTENSIBLE** structure, but do have extended data appended to the **WAVEFORMATEX** structure.</span></span>

<span data-ttu-id="b2e3d-121">I codec audio Windows Media supportano solo la decodifica in formati PCM ad alta risoluzione quando l'applicazione è in esecuzione in Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-121">The Windows Media audio codecs only support decoding to high-resolution PCM formats when the application is running on Windows XP or later.</span></span> <span data-ttu-id="b2e3d-122">Nelle versioni precedenti di Microsoft Windows, i codec decodificano in un formato con un massimo di 16 bit per campione e 2 canali.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-122">On previous versions of Microsoft Windows, the codecs decode to a format with a maximum of 16 bits per sample and 2 channels.</span></span> <span data-ttu-id="b2e3d-123">Inoltre, è necessario specificare che si vuole che il codec decodifichi il PCM ad alta definizione impostando l' \_ impostazione di output g wszEnableDiscreteOutput su **true** usando il metodo [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) .</span><span class="sxs-lookup"><span data-stu-id="b2e3d-123">In addition, you must specify that you want the codec to decode to high-definition PCM by setting the g\_wszEnableDiscreteOutput output setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="b2e3d-124">Dopo aver effettuato questa chiamata, gli output enumerati dal reader includeranno formati ad alta definizione.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-124">After making this call, the outputs enumerated by the reader will include high-definition formats.</span></span>

<span data-ttu-id="b2e3d-125">L'audio multicanale richiede una maggiore configurazione.</span><span class="sxs-lookup"><span data-stu-id="b2e3d-125">Multichannel audio requires more configuration.</span></span> <span data-ttu-id="b2e3d-126">Per ulteriori informazioni, vedere [lettura di audio multicanale](reading-multichannel-audio.md).</span><span class="sxs-lookup"><span data-stu-id="b2e3d-126">For more information, see [Reading Multichannel Audio](reading-multichannel-audio.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2e3d-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b2e3d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e3d-128">**Utilizzo degli input**</span><span class="sxs-lookup"><span data-stu-id="b2e3d-128">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 