---
description: Segnala i metadati e il buffer della maschera per una maschera di segmentazione dello sfondo che distingue tra lo sfondo e il primo piano di un fotogramma video.
title: MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK attributo (Mfapi.h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691850"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a><span data-ttu-id="d26a6-103">Attributo MF \_ CAPTURE METADATA FRAME BACKGROUND \_ \_ \_ \_ MASK</span><span class="sxs-lookup"><span data-stu-id="d26a6-103">MF\_CAPTURE\_METADATA\_FRAME\_BACKGROUND\_MASK attribute</span></span>

<span data-ttu-id="d26a6-104">Segnala i metadati e il buffer della maschera per una maschera di segmentazione dello sfondo che distingue tra lo sfondo e il primo piano di un fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="d26a6-104">Reports the metadata and mask buffer for a background segmentation mask that distinguishes between the background and foreground of a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="d26a6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d26a6-105">Data type</span></span>

<span data-ttu-id="d26a6-106">**Blob**</span><span class="sxs-lookup"><span data-stu-id="d26a6-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="d26a6-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d26a6-107">Remarks</span></span>

<span data-ttu-id="d26a6-108">I dati contenuti in questo attributo sono una struttura [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) che contiene informazioni sulle dimensioni della maschera di sfondo e sulla copertura del frame da cui viene dedotto, ovvero il frame restituito dal flusso.</span><span class="sxs-lookup"><span data-stu-id="d26a6-108">The data carried by this attribute is a [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) structure that contains information about the dimensions of the background mask as well as its coverage of the frame it is inferred from, which is the frame that is outputted by the stream.</span></span> <span data-ttu-id="d26a6-109">Contiene anche un buffer contiguo che rappresenta la maschera che l'app che utilizza per definire quali pixel sono considerati parte del primo piano o dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="d26a6-109">It also carries a contiguous buffer representing the mask to be leveraged by the consuming app to define which pixels are considered part of the foreground or background.</span></span> <span data-ttu-id="d26a6-110">Il ridimensionamento e la correlazione delle coordinate dell'immagine della maschera relativa al frame vengono gestiti dall'app che lo utilizza.</span><span class="sxs-lookup"><span data-stu-id="d26a6-110">The scaling and image coordinate correlation of the mask regarding the frame is handled by the consuming app.</span></span> 

## <a name="requirements"></a><span data-ttu-id="d26a6-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d26a6-111">Requirements</span></span>



| <span data-ttu-id="d26a6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d26a6-112">Requirement</span></span> | <span data-ttu-id="d26a6-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d26a6-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d26a6-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d26a6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d26a6-115">Windows Build 22000t</span><span class="sxs-lookup"><span data-stu-id="d26a6-115">Windows Build 22000t</span></span><br/>                          |
| <span data-ttu-id="d26a6-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d26a6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d26a6-117">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="d26a6-117">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="d26a6-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d26a6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d26a6-119"><dt>Mfapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="d26a6-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d26a6-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d26a6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d26a6-121">Elenco alfabetico degli Media Foundation personalizzati</span><span class="sxs-lookup"><span data-stu-id="d26a6-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d26a6-122">**IMFAttributes::GetBlob**</span><span class="sxs-lookup"><span data-stu-id="d26a6-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="d26a6-123">**IMFAttributes::SetBlob**</span><span class="sxs-lookup"><span data-stu-id="d26a6-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="d26a6-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d26a6-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="d26a6-125">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="d26a6-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 




