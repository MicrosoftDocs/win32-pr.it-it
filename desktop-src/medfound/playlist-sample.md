---
description: Esempio di playlist
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Esempio di playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309036"
---
# <a name="playlist-sample"></a><span data-ttu-id="8ff97-103">Esempio di playlist</span><span class="sxs-lookup"><span data-stu-id="8ff97-103">Playlist Sample</span></span>

<span data-ttu-id="8ff97-104">Mostra come usare Microsoft Media Foundation per riprodurre una sequenza di file audio in una playlist.</span><span class="sxs-lookup"><span data-stu-id="8ff97-104">Shows how to use Microsoft Media Foundation to play a sequence of audio files in a playlist.</span></span> <span data-ttu-id="8ff97-105">Nell'esempio viene utilizzata l' [origine sequencer](sequencer-source.md) per creare e gestire la playlist.</span><span class="sxs-lookup"><span data-stu-id="8ff97-105">The sample uses the [Sequencer Source](sequencer-source.md) to create and manage the playlist.</span></span>

> [!Note]  
> <span data-ttu-id="8ff97-106">Questo esempio non è più incluso nell'SDK.</span><span class="sxs-lookup"><span data-stu-id="8ff97-106">This sample is no longer included in the SDK.</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="8ff97-107">API illustrate</span><span class="sxs-lookup"><span data-stu-id="8ff97-107">APIs Demonstrated</span></span>

<span data-ttu-id="8ff97-108">In questo esempio vengono illustrate le interfacce Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ff97-108">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="8ff97-109">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="8ff97-109">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [<span data-ttu-id="8ff97-110">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="8ff97-110">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [<span data-ttu-id="8ff97-111">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="8ff97-111">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a><span data-ttu-id="8ff97-112">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="8ff97-112">Usage</span></span>

<span data-ttu-id="8ff97-113">Nell'esempio playlist viene compilata un'applicazione Windows.</span><span class="sxs-lookup"><span data-stu-id="8ff97-113">The Playlist sample builds a Windows application.</span></span>

-   <span data-ttu-id="8ff97-114">Per creare una nuova playlist, scegliere **Aggiungi a playlist** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="8ff97-114">To create a new playlist, select **Add to Playlist** from the **File** menu.</span></span> <span data-ttu-id="8ff97-115">Nella finestra di dialogo **Apri file** selezionare uno o più file audio.</span><span class="sxs-lookup"><span data-stu-id="8ff97-115">In the **Open File** dialog, select one or more audio files.</span></span> <span data-ttu-id="8ff97-116">I file vengono aggiunti alla playlist.</span><span class="sxs-lookup"><span data-stu-id="8ff97-116">The files are added to the playlist.</span></span>
-   <span data-ttu-id="8ff97-117">Per riprodurre la sequenza, fare clic su **Riproduci**.</span><span class="sxs-lookup"><span data-stu-id="8ff97-117">To play the sequence, click **Play**.</span></span>
-   <span data-ttu-id="8ff97-118">Per sospendere il segmento corrente, fare clic su **Sospendi**.</span><span class="sxs-lookup"><span data-stu-id="8ff97-118">To pause the current segment, click **Pause**.</span></span>
-   <span data-ttu-id="8ff97-119">Per arrestare il segmento corrente, fare clic su **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="8ff97-119">To stop the current segment, click **Stop**.</span></span>
-   <span data-ttu-id="8ff97-120">Per passare a un file, fare doppio clic sull'elemento nella playlist.</span><span class="sxs-lookup"><span data-stu-id="8ff97-120">To skip to a file, double-click the item in the playlist.</span></span>
-   <span data-ttu-id="8ff97-121">Per eliminare un file dalla playlist, selezionare l'elemento nella playlist.</span><span class="sxs-lookup"><span data-stu-id="8ff97-121">To delete a file from the playlist, select the item in the playlist.</span></span> <span data-ttu-id="8ff97-122">Quindi selezionare **Rimuovi dalla playlist** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="8ff97-122">Then select **Remove from Playlist** from the **File** menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ff97-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ff97-123">Requirements</span></span>



| <span data-ttu-id="8ff97-124">Prodotto</span><span class="sxs-lookup"><span data-stu-id="8ff97-124">Product</span></span>                                                        | <span data-ttu-id="8ff97-125">Versione</span><span class="sxs-lookup"><span data-stu-id="8ff97-125">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="8ff97-126">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="8ff97-126">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="8ff97-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8ff97-127">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="8ff97-128">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="8ff97-128">Downloading the Sample</span></span>

<span data-ttu-id="8ff97-129">Questo esempio è disponibile nelle posizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="8ff97-129">This sample is available in the following locations.</span></span>



| <span data-ttu-id="8ff97-130">Location</span><span class="sxs-lookup"><span data-stu-id="8ff97-130">Location</span></span>                                                     | <span data-ttu-id="8ff97-131">Percorso/URL</span><span class="sxs-lookup"><span data-stu-id="8ff97-131">Path/URL</span></span>                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="8ff97-132">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="8ff97-132">Windows SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=8279) | <span data-ttu-id="8ff97-133">*Radice SDK* \\ \\ \\ Playlist mediafoundation Multimedia degli esempi \\</span><span class="sxs-lookup"><span data-stu-id="8ff97-133">*SDK Root*\\Samples\\multimedia\\mediafoundation\\Playlist</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8ff97-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ff97-134">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8ff97-135">[Esempio BasicPlayback](/previous-versions//bb970475(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8ff97-135">[BasicPlayback Sample](/previous-versions//bb970475(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8ff97-136">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="8ff97-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="8ff97-137">Origine sequencer</span><span class="sxs-lookup"><span data-stu-id="8ff97-137">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 
