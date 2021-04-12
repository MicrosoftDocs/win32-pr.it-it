---
title: Ridimensionamento video
description: Ridimensionamento video
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows Media Format SDK, ridimensionamento video
- Windows Media Format SDK, ridimensionamento del video
- ASF (Advanced Systems Format), ridimensionamento video
- ASF (Advanced Systems Format), ridimensionamento video
- ASF (Advanced Systems Format), ridimensionamento del video
- ASF (Advanced Systems Format), ridimensionamento del video
- ridimensionamento video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221208"
---
# <a name="video-resizing"></a><span data-ttu-id="d8aa3-110">Ridimensionamento video</span><span class="sxs-lookup"><span data-stu-id="d8aa3-110">Video Resizing</span></span>

<span data-ttu-id="d8aa3-111">Quando si definiscono le impostazioni per un flusso video, è necessario specificare una larghezza e un'altezza per i fotogrammi video.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-111">When you define the settings for a video stream, you must specify a width and height for the video frames.</span></span> <span data-ttu-id="d8aa3-112">Questa dimensione video determina la dimensione dei fotogrammi video codificati nella sezione dati del file.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-112">This video size determines the size of the video frames encoded in the data section of the file.</span></span> <span data-ttu-id="d8aa3-113">Tuttavia, le dimensioni del video in un profilo non determinano, o limitano, le dimensioni del supporto di input recapitato al writer o la dimensione del supporto di output ricevuto dal lettore.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-113">However, the video size in a profile does not determine, or limit, the size of the input media that you deliver to the writer, or the size of the output media you receive from the reader.</span></span> <span data-ttu-id="d8aa3-114">Il writer può ridimensionare i fotogrammi video in base alle esigenze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-114">The writer can resize the video frames to suit the needs of your application.</span></span>

<span data-ttu-id="d8aa3-115">Le dimensioni dell'immagine video possono essere considerate come in tre fasi: dimensioni del video di input, dimensioni del video di flusso e dimensioni del video di output.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-115">Video image size can be thought of as going through three stages: input video size, stream video size, and output video size.</span></span>

<span data-ttu-id="d8aa3-116">Dimensioni video di input è la dimensione dei frame passati come campioni all'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-116">Input video size is the size of the frames that you pass as samples to the writer object.</span></span> <span data-ttu-id="d8aa3-117">Queste dimensioni vengono definite come una delle proprietà di input video obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-117">You define this size as one of the required video input properties.</span></span> <span data-ttu-id="d8aa3-118">Per ulteriori informazioni sulle proprietà di input, vedere [per enumerare i formati di input](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="d8aa3-118">For more information about input properties, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

<span data-ttu-id="d8aa3-119">Dimensioni video flusso corrisponde alla dimensione dei frame nella sezione dati del file ASF.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-119">Stream video size is the size of the frames in the data section of the ASF file.</span></span> <span data-ttu-id="d8aa3-120">Queste dimensioni vengono definite come una delle impostazioni di configurazione del flusso necessarie nel profilo.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-120">You define this size as one of the required stream configuration settings in the profile.</span></span> <span data-ttu-id="d8aa3-121">Se si scrive un file e le dimensioni del video di input sono diverse dalle dimensioni del video del flusso, il writer ridimensiona i frame durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-121">If you are writing a file and the input video size is different from the stream video size, the writer resizes the frames while encoding.</span></span> <span data-ttu-id="d8aa3-122">Per ulteriori informazioni sulle proprietà del flusso video, vedere [Configuring video](configuring-video-streams.md)Streams.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-122">For more information about video stream properties, see [Configuring Video Streams](configuring-video-streams.md).</span></span>

<span data-ttu-id="d8aa3-123">Dimensioni video di output corrisponde alla dimensione dei frame recapitati dal lettore o dal lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-123">Output video size is the size of the frames delivered by the reader or synchronous reader.</span></span> <span data-ttu-id="d8aa3-124">Queste dimensioni vengono definite come una delle proprietà di output video obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-124">You define this size as one of the required video output properties.</span></span> <span data-ttu-id="d8aa3-125">Se si legge un file e le dimensioni del video di output sono diverse dalla dimensione del video del flusso, il lettore ridimensiona i frame durante la decodifica.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-125">If you are reading a file and the output video size is different from the stream video size, the reader resizes the frames while decoding.</span></span>

<span data-ttu-id="d8aa3-126">Non è possibile impostare una dimensione del video del flusso su un numero dispari di pixel in larghezza.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-126">You cannot set a stream video size to an odd number of pixels wide.</span></span> <span data-ttu-id="d8aa3-127">Se si imposta la larghezza di un flusso video su un valore dispari, il profilo non verrà accettato dal writer oppure il video risultante verrà codificato con una linea nera verso il basso di una parte per compensare la differenza.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-127">If you set the width of a video stream to an odd value, either the profile will not be accepted by the writer, or the resulting video will be encoded with a black line down one side to make up the difference.</span></span>

<span data-ttu-id="d8aa3-128">È necessario prestare attenzione durante il ridimensionamento del video.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-128">You should take care when resizing video.</span></span> <span data-ttu-id="d8aa3-129">Le immagini tendono a essere più adatte alla soluzione originale.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-129">Images tend to look their best at their original resolution.</span></span> <span data-ttu-id="d8aa3-130">Le immagini di ridimensionamento possono spesso provocare distorsioni e rendere il testo illeggibile.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-130">Resizing images can often cause distortion and make text illegible.</span></span> <span data-ttu-id="d8aa3-131">Se si comprime il video a una velocità in bit bassa, si noterà anche che le distorsioni di ridimensionamento possono causare artefatti di compressione gravi.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-131">If you are compressing video to a low bit rate, you will also find that resizing distortions can lead to severe compression artifacts.</span></span>

<span data-ttu-id="d8aa3-132">Il codec della schermata Windows Media Video 9 non supporta il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="d8aa3-132">The Windows Media Video 9 Screen codec does not support resizing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8aa3-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8aa3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8aa3-134">**Funzionalità di scrittura di file**</span><span class="sxs-lookup"><span data-stu-id="d8aa3-134">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="d8aa3-135">**Utilizzo degli input**</span><span class="sxs-lookup"><span data-stu-id="d8aa3-135">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="d8aa3-136">**Uso degli output**</span><span class="sxs-lookup"><span data-stu-id="d8aa3-136">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




