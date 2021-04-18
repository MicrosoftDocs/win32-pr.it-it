---
description: '\_Esempio di AUDIODELAY MFT'
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: Esempio MFT_AudioDelay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309084"
---
# <a name="mft_audiodelay-sample"></a><span data-ttu-id="f5c84-103">\_Esempio di AUDIODELAY MFT</span><span class="sxs-lookup"><span data-stu-id="f5c84-103">MFT\_AudioDelay Sample</span></span>

<span data-ttu-id="f5c84-104">Viene illustrato come implementare un effetto audio come una trasformazione di Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="f5c84-104">Shows how to implement an audio effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="f5c84-105">Il ritardo audio MFT accetta audio PCM come input, applica un effetto delay (ECHO) e restituisce i dati audio modificati.</span><span class="sxs-lookup"><span data-stu-id="f5c84-105">The audio delay MFT accepts PCM audio as input, applies a delay (echo) effect, and outputs the modified audio data.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="f5c84-106">API illustrate</span><span class="sxs-lookup"><span data-stu-id="f5c84-106">APIs Demonstrated</span></span>

<span data-ttu-id="f5c84-107">In questo esempio vengono illustrate le interfacce Microsoft Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="f5c84-107">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="f5c84-108">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="f5c84-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="f5c84-109">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f5c84-109">Usage</span></span>

<span data-ttu-id="f5c84-110">L' \_ esempio MFT AudioDelay compila una dll che è un server com per MFT.</span><span class="sxs-lookup"><span data-stu-id="f5c84-110">The MFT\_AudioDelay sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="f5c84-111">Prima di usare il file MFT, è necessario registrare la DLL.</span><span class="sxs-lookup"><span data-stu-id="f5c84-111">Before using the MFT, you must register the DLL.</span></span> <span data-ttu-id="f5c84-112">È possibile usare lo strumento TopoEdit per compilare una topologia che include il ritardo audio MFT.</span><span class="sxs-lookup"><span data-stu-id="f5c84-112">You can use the TopoEdit tool to build a topology that includes the audio delay MFT.</span></span> <span data-ttu-id="f5c84-113">Per ulteriori informazioni su TopoEdit, vedere [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="f5c84-113">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span> <span data-ttu-id="f5c84-114">È anche possibile modificare l' [esempio PlaybackFX](/previous-versions//bb970336(v=vs.85)) per usare il MFT.</span><span class="sxs-lookup"><span data-stu-id="f5c84-114">You can also modify the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)) to use the MFT.</span></span> <span data-ttu-id="f5c84-115">Sarà necessario modificare la funzione AddBranchToPartialTopology in Player. cpp.</span><span class="sxs-lookup"><span data-stu-id="f5c84-115">You will need to modify the AddBranchToPartialTopology function in Player.cpp.</span></span> <span data-ttu-id="f5c84-116">Modificare la riga seguente da:</span><span class="sxs-lookup"><span data-stu-id="f5c84-116">Change the following line from:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

<span data-ttu-id="f5c84-117">Con:</span><span class="sxs-lookup"><span data-stu-id="f5c84-117">To:</span></span>

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

<span data-ttu-id="f5c84-118">Il valore CLSID \_ DelayMFT è dichiarato nel file di intestazione AudioDelayUuids. h nella cartella di \_ esempio MFT AudioDelay.</span><span class="sxs-lookup"><span data-stu-id="f5c84-118">The value CLSID\_DelayMFT is declared in the header file AudioDelayUuids.h in the MFT\_AudioDelay sample folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c84-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5c84-119">Requirements</span></span>



| <span data-ttu-id="f5c84-120">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f5c84-120">Product</span></span>                                                        | <span data-ttu-id="f5c84-121">Versione</span><span class="sxs-lookup"><span data-stu-id="f5c84-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="f5c84-122">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f5c84-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="f5c84-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5c84-123">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f5c84-124">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f5c84-124">Downloading the Sample</span></span>

<span data-ttu-id="f5c84-125">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span><span class="sxs-lookup"><span data-stu-id="f5c84-125">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5c84-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5c84-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5c84-127">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="f5c84-127">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="f5c84-128">Trasformazioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5c84-128">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="f5c84-129">\_Esempio di scala di grigi MFT</span><span class="sxs-lookup"><span data-stu-id="f5c84-129">MFT\_Grayscale Sample</span></span>](mft-grayscale-sample.md)
</dt> <dt>

[<span data-ttu-id="f5c84-130">Scrittura di un MFT personalizzato</span><span class="sxs-lookup"><span data-stu-id="f5c84-130">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
