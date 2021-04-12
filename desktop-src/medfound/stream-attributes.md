---
description: Attributi di flusso
ms.assetid: 83b64ad8-2552-41d1-bc61-20361831020b
title: Attributi di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25de9ae6cf769268b3868d36bac2e293cfd8d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527823"
---
# <a name="stream-attributes"></a><span data-ttu-id="58390-103">Attributi di flusso</span><span class="sxs-lookup"><span data-stu-id="58390-103">Stream Attributes</span></span>

<span data-ttu-id="58390-104">Gli attributi seguenti si applicano ai flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="58390-104">The following attributes apply to media streams.</span></span> <span data-ttu-id="58390-105">Per ottenere gli attributi da un esempio multimediale, usare il metodo [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) .</span><span class="sxs-lookup"><span data-stu-id="58390-105">To get the attributes from a media sample, use the [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) method.</span></span>



| <span data-ttu-id="58390-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="58390-106">Attribute</span></span>                                                                                   | <span data-ttu-id="58390-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58390-107">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="58390-108">\_CameraExtrinsics MFStreamExtension</span><span class="sxs-lookup"><span data-stu-id="58390-108">MFStreamExtension\_CameraExtrinsics</span></span>](mfstreamextension-cameraextrinsics.md)               | <span data-ttu-id="58390-109">La fotocamera è estrinseca per il flusso.</span><span class="sxs-lookup"><span data-stu-id="58390-109">The camera extrinsics for the stream.</span></span>         |
| [<span data-ttu-id="58390-110">\_PinholeCameraIntrinsics MFStreamExtension</span><span class="sxs-lookup"><span data-stu-id="58390-110">MFStreamExtension\_PinholeCameraIntrinsics</span></span>](mfstreamextension-pinholecameraintrinsics.md) | <span data-ttu-id="58390-111">Funzioni intrinseche della fotocamera pinhole per il flusso.</span><span class="sxs-lookup"><span data-stu-id="58390-111">The pinhole camera intrinsics for the stream.</span></span> |



 

<span data-ttu-id="58390-112">Non tutti i flussi multimediali contengono tutti gli attributi elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="58390-112">Not every media stream contains every attribute listed here.</span></span> <span data-ttu-id="58390-113">In alcuni casi, un attributo si applica solo a determinati tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="58390-113">In some cases, an attribute applies only to certain kinds of data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58390-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58390-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58390-115">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="58390-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="58390-116">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="58390-116">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="58390-117">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="58390-117">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 



