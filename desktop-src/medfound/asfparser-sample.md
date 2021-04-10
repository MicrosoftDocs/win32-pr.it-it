---
description: Esempio ASFParser
ms.assetid: 6be1e12f-7d4a-4564-88ae-14fd71fd2cf9
title: Esempio ASFParser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159b481e22d77b0bee9adccbbb74073398c12b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225838"
---
# <a name="asfparser-sample"></a><span data-ttu-id="c5b73-103">Esempio ASFParser</span><span class="sxs-lookup"><span data-stu-id="c5b73-103">ASFParser Sample</span></span>

<span data-ttu-id="c5b73-104">Viene illustrato come analizzare i dati da un file Advanced Systems Format (ASF) utilizzando i componenti ASF di basso livello in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c5b73-104">Shows how to parse data from an Advanced Systems Format (ASF) file by using the low-level ASF components in Media Foundation.</span></span> <span data-ttu-id="c5b73-105">Nell'esempio vengono illustrate le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5b73-105">The sample demonstrates the following tasks:</span></span>

-   <span data-ttu-id="c5b73-106">Enumerazione dei flussi audio e video in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="c5b73-106">Enumerating the audio and video streams in an ASF file.</span></span>
-   <span data-ttu-id="c5b73-107">Selezione di un flusso audio o video per l'analisi.</span><span class="sxs-lookup"><span data-stu-id="c5b73-107">Selecting an audio or a video stream for parsing.</span></span>
-   <span data-ttu-id="c5b73-108">Ricerca di un pacchetto al momento della riproduzione desiderata.</span><span class="sxs-lookup"><span data-stu-id="c5b73-108">Seeking to a packet at a desired playback time.</span></span>
-   <span data-ttu-id="c5b73-109">Generazione di esempi compressi per il flusso selezionato.</span><span class="sxs-lookup"><span data-stu-id="c5b73-109">Generating compressed samples for the selected stream.</span></span>
-   <span data-ttu-id="c5b73-110">Decodifica di esempi audio e video.</span><span class="sxs-lookup"><span data-stu-id="c5b73-110">Decoding audio and video samples.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="c5b73-111">API illustrate</span><span class="sxs-lookup"><span data-stu-id="c5b73-111">APIs Demonstrated</span></span>

<span data-ttu-id="c5b73-112">In questo esempio vengono illustrate le interfacce Microsoft Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5b73-112">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="c5b73-113">**IMFASFContentInfo**</span><span class="sxs-lookup"><span data-stu-id="c5b73-113">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)
-   [<span data-ttu-id="c5b73-114">**IMFASFIndexer**</span><span class="sxs-lookup"><span data-stu-id="c5b73-114">**IMFASFIndexer**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)
-   [<span data-ttu-id="c5b73-115">**IMFASFSplitter**</span><span class="sxs-lookup"><span data-stu-id="c5b73-115">**IMFASFSplitter**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter)

## <a name="usage"></a><span data-ttu-id="c5b73-116">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="c5b73-116">Usage</span></span>

1.  <span data-ttu-id="c5b73-117">Per aprire un file ASF, fare clic sul pulsante **Apri file multimediale...** .</span><span class="sxs-lookup"><span data-stu-id="c5b73-117">To open an ASF file, click the **Open Media File...** button.</span></span>
2.  <span data-ttu-id="c5b73-118">Selezionare un file ASF e fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="c5b73-118">Select an ASF file and click **Open**.</span></span> <span data-ttu-id="c5b73-119">Le informazioni sul file vengono visualizzate nel riquadro **informazioni** .</span><span class="sxs-lookup"><span data-stu-id="c5b73-119">Information about the file is shown on the **Information** pane.</span></span>
3.  <span data-ttu-id="c5b73-120">In **configurazione parser** selezionare un flusso da analizzare.</span><span class="sxs-lookup"><span data-stu-id="c5b73-120">Under **Parser Configuration**, select a stream to parse.</span></span>
4.  <span data-ttu-id="c5b73-121">Per generare gli esempi in ordine inverso, selezionare **Inverti**.</span><span class="sxs-lookup"><span data-stu-id="c5b73-121">To generate samples in reverse, select **Reverse**.</span></span>
5.  <span data-ttu-id="c5b73-122">Per specificare il punto iniziale, trascinare il dispositivo di scorrimento nella posizione desiderata.</span><span class="sxs-lookup"><span data-stu-id="c5b73-122">To specify the start point, drag the slider to the desired location.</span></span>
6.  <span data-ttu-id="c5b73-123">Per iniziare l'analisi, fare clic sul pulsante **genera esempi** .</span><span class="sxs-lookup"><span data-stu-id="c5b73-123">To begin parsing, click the **Generate Samples** button.</span></span> <span data-ttu-id="c5b73-124">Le informazioni sugli esempi sono visualizzate nel riquadro **informazioni** .</span><span class="sxs-lookup"><span data-stu-id="c5b73-124">Information about the samples is shown on the **Information** pane.</span></span>
7.  <span data-ttu-id="c5b73-125">Per testare gli esempi per il flusso audio, fare clic sul pulsante **prova audio** .</span><span class="sxs-lookup"><span data-stu-id="c5b73-125">To test the samples for the audio stream, click the **Test Audio** button.</span></span>
8.  <span data-ttu-id="c5b73-126">Per testare gli esempi per il flusso video, fare clic sul pulsante **Mostra bitmap** .</span><span class="sxs-lookup"><span data-stu-id="c5b73-126">To test the samples for the video stream, click the **Show Bitmap** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b73-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5b73-127">Requirements</span></span>



| <span data-ttu-id="c5b73-128">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c5b73-128">Product</span></span>                                                        | <span data-ttu-id="c5b73-129">Versione</span><span class="sxs-lookup"><span data-stu-id="c5b73-129">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="c5b73-130">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c5b73-130">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="c5b73-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c5b73-131">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c5b73-132">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="c5b73-132">Downloading the Sample</span></span>

<span data-ttu-id="c5b73-133">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span><span class="sxs-lookup"><span data-stu-id="c5b73-133">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/asfparser).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5b73-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c5b73-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5b73-135">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="c5b73-135">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="c5b73-136">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5b73-136">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="c5b73-137">Esercitazione: lettura di un file ASF</span><span class="sxs-lookup"><span data-stu-id="c5b73-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="c5b73-138">Componenti ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="c5b73-138">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



