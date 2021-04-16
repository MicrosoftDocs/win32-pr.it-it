---
description: Le funzioni seguenti riguardano gli oggetti del tipo di supporto.
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: Funzioni helper del tipo di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e5edb9748bad8ee16903eb9ff1ada50c1c043b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530529"
---
# <a name="media-type-helper-functions"></a><span data-ttu-id="c1b11-103">Funzioni helper del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="c1b11-103">Media Type Helper Functions</span></span>

<span data-ttu-id="c1b11-104">Le funzioni seguenti riguardano gli oggetti del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c1b11-104">The following functions pertain to media type objects.</span></span>



| <span data-ttu-id="c1b11-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="c1b11-105">Function</span></span>                                                                     | <span data-ttu-id="c1b11-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1b11-106">Description</span></span>                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="c1b11-107">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="c1b11-107">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="c1b11-108">Calcola la frequenza dei fotogrammi dalla durata media di un frame video.</span><span class="sxs-lookup"><span data-stu-id="c1b11-108">Calculates the frame rate from the average duration of a video frame.</span></span> |
| [<span data-ttu-id="c1b11-109">**MFCalculateImageSize**</span><span class="sxs-lookup"><span data-stu-id="c1b11-109">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="c1b11-110">Recupera le dimensioni dell'immagine per un formato video non compresso.</span><span class="sxs-lookup"><span data-stu-id="c1b11-110">Retrieves the image size for an uncompressed video format.</span></span>            |
| [<span data-ttu-id="c1b11-111">**MFCompareFullToPartialMediaType**</span><span class="sxs-lookup"><span data-stu-id="c1b11-111">**MFCompareFullToPartialMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | <span data-ttu-id="c1b11-112">Confronta un tipo di supporto completo con un tipo di supporto parziale.</span><span class="sxs-lookup"><span data-stu-id="c1b11-112">Compares a full media type to a partial media type.</span></span>                   |
| [<span data-ttu-id="c1b11-113">**MFCreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="c1b11-113">**MFCreateMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | <span data-ttu-id="c1b11-114">Crea un tipo di supporto vuoto.</span><span class="sxs-lookup"><span data-stu-id="c1b11-114">Creates an empty media type.</span></span>                                          |
| [<span data-ttu-id="c1b11-115">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="c1b11-115">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="c1b11-116">Converte una frequenza di fotogrammi video in una durata del fotogramma.</span><span class="sxs-lookup"><span data-stu-id="c1b11-116">Converts a video frame rate into a frame duration.</span></span>                    |
| [<span data-ttu-id="c1b11-117">**MFGetStrideForBitmapInfoHeader**</span><span class="sxs-lookup"><span data-stu-id="c1b11-117">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="c1b11-118">Recupera lo stride minimo della superficie per un formato video.</span><span class="sxs-lookup"><span data-stu-id="c1b11-118">Retrieves the minimum surface stride for a video format.</span></span>              |
| [<span data-ttu-id="c1b11-119">**MFIsFormatYUV**</span><span class="sxs-lookup"><span data-stu-id="c1b11-119">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="c1b11-120">Esegue una query se un codice FOURCC o un valore **D3DFORMAT** è un formato YUV.</span><span class="sxs-lookup"><span data-stu-id="c1b11-120">Queries whether a FOURCC code or **D3DFORMAT** value is a YUV format.</span></span> |
| [<span data-ttu-id="c1b11-121">**MFValidateMediaTypeSize**</span><span class="sxs-lookup"><span data-stu-id="c1b11-121">**MFValidateMediaTypeSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | <span data-ttu-id="c1b11-122">Convalida la dimensione di un buffer per un blocco di formato video.</span><span class="sxs-lookup"><span data-stu-id="c1b11-122">Validates the size of a buffer for a video format block.</span></span>              |
| [<span data-ttu-id="c1b11-123">**MFWrapMediaType**</span><span class="sxs-lookup"><span data-stu-id="c1b11-123">**MFWrapMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | <span data-ttu-id="c1b11-124">Crea un tipo di supporto che esegue il wrapping di un altro tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c1b11-124">Creates a media type that wraps another media type.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="c1b11-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1b11-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1b11-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="c1b11-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="c1b11-127">Conversioni di tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="c1b11-127">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="c1b11-128">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="c1b11-128">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



