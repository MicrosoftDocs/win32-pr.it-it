---
description: Specifica la risoluzione finale dell'output dell'immagine decodificata, dopo l'elaborazione video.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: Attributo MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bbc0f01ef2a1d7062c6ab58c528b015383fc68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226530"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a><span data-ttu-id="ba796-103">\_ \_ \_ \_ Attributo hint di risoluzione video finale del decodificatore MFT \_</span><span class="sxs-lookup"><span data-stu-id="ba796-103">MFT\_DECODER\_FINAL\_VIDEO\_RESOLUTION\_HINT attribute</span></span>

<span data-ttu-id="ba796-104">Specifica la risoluzione finale dell'output dell'immagine decodificata, dopo l'elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="ba796-104">Specifies the final output resolution of the decoded image, after video processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="ba796-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ba796-105">Data type</span></span>

<span data-ttu-id="ba796-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ba796-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="ba796-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba796-107">Remarks</span></span>

<span data-ttu-id="ba796-108">Questo attributo è supportato da alcuni decodificatori video.</span><span class="sxs-lookup"><span data-stu-id="ba796-108">This attribute is supported by some video decoders.</span></span> <span data-ttu-id="ba796-109">Un'applicazione può impostare questo attributo per indicare la larghezza e l'altezza dell'immagine dopo l'elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="ba796-109">An application can set this attribute to indicate the width and height of the image after video processing.</span></span> <span data-ttu-id="ba796-110">Il decodificatore può usare queste informazioni per ottimizzare il processo di decodifica, soprattutto se le dimensioni dell'immagine finale sono molto più piccole delle dimensioni dell'immagine nativa.</span><span class="sxs-lookup"><span data-stu-id="ba796-110">The decoder can use this information to optimize the decoding process, especially if the final image size is much smaller than the native image size.</span></span> <span data-ttu-id="ba796-111">Ad esempio, il decodificatore potrebbe ignorare un filtro out-of-loop.</span><span class="sxs-lookup"><span data-stu-id="ba796-111">For example, the decoder might skip an out-of-loop filter.</span></span>

<span data-ttu-id="ba796-112">I 32 bit superiori contengono la larghezza e i 32 bit inferiori contengono l'altezza.</span><span class="sxs-lookup"><span data-stu-id="ba796-112">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="ba796-113">Per impostare l'attributo:</span><span class="sxs-lookup"><span data-stu-id="ba796-113">To set this attribute:</span></span>

1.  <span data-ttu-id="ba796-114">Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) nel decodificatore per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="ba796-114">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="ba796-115">Chiamare [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) per aggiungere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="ba796-115">Call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba796-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba796-116">Requirements</span></span>



| <span data-ttu-id="ba796-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba796-117">Requirement</span></span> | <span data-ttu-id="ba796-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ba796-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba796-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba796-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ba796-120">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ba796-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ba796-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba796-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ba796-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ba796-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ba796-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba796-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba796-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba796-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba796-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba796-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba796-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ba796-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba796-127">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="ba796-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




