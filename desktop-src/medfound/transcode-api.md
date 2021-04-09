---
description: Questa sezione descrive come usare l'API transcode per ricodificare i file multimediali. L'API transcode è stata introdotta in Windows 7.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: API transcodifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880586"
---
# <a name="transcode-api"></a><span data-ttu-id="35477-104">API transcodifica</span><span class="sxs-lookup"><span data-stu-id="35477-104">Transcode API</span></span>

<span data-ttu-id="35477-105">Questa sezione descrive come usare l'API transcode per ricodificare i file multimediali.</span><span class="sxs-lookup"><span data-stu-id="35477-105">This section describes how to use the transcode API to re-encode media files.</span></span> <span data-ttu-id="35477-106">L'API transcode è stata introdotta in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="35477-106">The transcode API was introduced in Windows 7.</span></span>

<span data-ttu-id="35477-107">La *transcodifica* è la conversione di un file multimediale digitale da un formato a un altro.</span><span class="sxs-lookup"><span data-stu-id="35477-107">*Transcoding* is the conversion of a digital media file from one format to another.</span></span> <span data-ttu-id="35477-108">L'API transcode è progettata per essere usata con la [sessione multimediale](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="35477-108">The transcode API is designed to be used with the [Media Session](media-session.md).</span></span> <span data-ttu-id="35477-109">Semplifica l'uso della sessione multimediale per determinati tipi di applicazioni di transcodifica:</span><span class="sxs-lookup"><span data-stu-id="35477-109">It simplifies the use of the Media Session for certain types of transcoding applications:</span></span>

-   <span data-ttu-id="35477-110">Codifica della velocità in bit costante (CBR), in cui la velocità in bit della destinazione è nota in anticipo.</span><span class="sxs-lookup"><span data-stu-id="35477-110">Constant bit rate (CBR) encoding, where the target bit rate is known in advance.</span></span>
-   <span data-ttu-id="35477-111">Al massimo un flusso audio e un flusso video.</span><span class="sxs-lookup"><span data-stu-id="35477-111">At most one audio stream and one video stream.</span></span>
-   <span data-ttu-id="35477-112">Codifica da e in un file.</span><span class="sxs-lookup"><span data-stu-id="35477-112">Encoding from and to a file.</span></span>

<span data-ttu-id="35477-113">L'API transcode non supporta quanto segue:</span><span class="sxs-lookup"><span data-stu-id="35477-113">Transcode API does not support the following:</span></span>

-   <span data-ttu-id="35477-114">Velocità in bit variabile (VBR) o codifica Multipass.</span><span class="sxs-lookup"><span data-stu-id="35477-114">Variable bit rate (VBR) or multi-pass encoding.</span></span>
-   <span data-ttu-id="35477-115">Più flussi audio o più flussi video.</span><span class="sxs-lookup"><span data-stu-id="35477-115">Multiple audio streams or multiple video streams.</span></span>
-   <span data-ttu-id="35477-116">Contenuto protetto da DRM diverso da file ASF protetti con WMDRM.</span><span class="sxs-lookup"><span data-stu-id="35477-116">DRM-protected content other than ASF files protected with WMDRM.</span></span>
-   <span data-ttu-id="35477-117">Streaming Live, ad esempio streaming live-to-file o streaming live-to-Live.</span><span class="sxs-lookup"><span data-stu-id="35477-117">Live streaming, such as live-to-file streaming or live-to-live streaming.</span></span>

<span data-ttu-id="35477-118">Se l'applicazione di codifica rientra in questi vincoli, l'API transcode è un modello di programmazione più semplice rispetto all'uso della sessione multimediale da solo.</span><span class="sxs-lookup"><span data-stu-id="35477-118">If your encoding application fits within these constraints, the transcode API a simpler programming model than using the Media Session alone.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="35477-119">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="35477-119">In this section</span></span>



| <span data-ttu-id="35477-120">Argomento</span><span class="sxs-lookup"><span data-stu-id="35477-120">Topic</span></span>                                                                                          | <span data-ttu-id="35477-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35477-121">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35477-122">Informazioni sull'API transcodifica</span><span class="sxs-lookup"><span data-stu-id="35477-122">About the Transcode API</span></span>](about-the-transcode-api.md)<br/>                              | <span data-ttu-id="35477-123">Viene fornita una panoramica generale dell'API transcodifica.</span><span class="sxs-lookup"><span data-stu-id="35477-123">Provides a general overview of the transcode API.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="35477-124">Uso dell'API transcode</span><span class="sxs-lookup"><span data-stu-id="35477-124">Using the Transcode API</span></span>](fast-transcode-objects.md)<br/>                               | <span data-ttu-id="35477-125">Viene descritto il modo in cui un'applicazione utilizza l'API transcode.</span><span class="sxs-lookup"><span data-stu-id="35477-125">Describes how an application uses the transcode API.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="35477-126">Esercitazione: codifica di un file MP4</span><span class="sxs-lookup"><span data-stu-id="35477-126">Tutorial: Encoding an MP4 File</span></span>](tutorial--encoding-an-mp4-file-.md)<br/>               | <span data-ttu-id="35477-127">Esercitazione dettagliata che illustra come usare l'API transcode per codificare un file MP4.</span><span class="sxs-lookup"><span data-stu-id="35477-127">A step-by-step tutorial that shows how to use the transcode API to encode an MP4 file.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="35477-128">Esercitazione: codifica di un file WMA</span><span class="sxs-lookup"><span data-stu-id="35477-128">Tutorial: Encoding a WMA File</span></span>](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | <span data-ttu-id="35477-129">Viene illustrato come utilizzare l'API transcode per codificare un file WMA.</span><span class="sxs-lookup"><span data-stu-id="35477-129">Shows how to use the transcode API to encode a WMA file.</span></span> <span data-ttu-id="35477-130">Questa esercitazione modifica il codice illustrato in [esercitazione: codifica di un file MP4](tutorial--encoding-an-mp4-file-.md), quindi è consigliabile leggere prima l'esercitazione.</span><span class="sxs-lookup"><span data-stu-id="35477-130">This tutorial modifies the code shown in [Tutorial: Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="35477-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35477-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35477-132">Codifica e creazione di file</span><span class="sxs-lookup"><span data-stu-id="35477-132">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="35477-133">Media Foundation: concetti essenziali</span><span class="sxs-lookup"><span data-stu-id="35477-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="35477-134">Cenni preliminari sulla codifica in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35477-134">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




