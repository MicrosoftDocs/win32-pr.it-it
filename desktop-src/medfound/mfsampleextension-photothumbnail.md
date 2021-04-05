---
description: Contiene l'anteprima della foto di un IMFSample.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: Attributo MFSampleExtension_PhotoThumbnail (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131115"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a><span data-ttu-id="1da24-103">\_Attributo di anteprima MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="1da24-103">MFSampleExtension\_PhotoThumbnail attribute</span></span>

<span data-ttu-id="1da24-104">Contiene l'anteprima della foto di un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="1da24-104">Contains the photo thumbnail of a [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span>

## <a name="data-type"></a><span data-ttu-id="1da24-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1da24-105">Data type</span></span>

<span data-ttu-id="1da24-106">**IUnknown** archiviato come **IMFMediaBuffer**</span><span class="sxs-lookup"><span data-stu-id="1da24-106">**IUnknown** stored as **IMFMediaBuffer**</span></span>

<span data-ttu-id="1da24-107">L'anteprima viene configurata con **KSPROPERTYSETID \_ ExtendedCameraControl**.</span><span class="sxs-lookup"><span data-stu-id="1da24-107">The thumbnail is configured using the **KSPROPERTYSETID\_ExtendedCameraControl**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1da24-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="1da24-108">Remarks</span></span>

<span data-ttu-id="1da24-109">Questo attributo è impostato su [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) fornito da MFT0 ed è l'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associato all'anteprima foto.</span><span class="sxs-lookup"><span data-stu-id="1da24-109">This attribute is set on the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) provided by the MFT0 and is the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associated with the photo thumbnail.</span></span>

<span data-ttu-id="1da24-110">Il formato dell'anteprima foto può essere JPEG (immagine del tipo principale), NV12 o ARGB32.</span><span class="sxs-lookup"><span data-stu-id="1da24-110">The format of the photo thumbnail can be JPEG (major type image), NV12 or ARGB32.</span></span>

<span data-ttu-id="1da24-111">Il [ \_ PhotoThumbnailMediaType MFSampleExtension](mfsampleextension-photothumbnailmediatype.md) è necessario per le anteprime per descrivere il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="1da24-111">The [MFSampleExtension\_PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) is required for thumbnails to describe the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="1da24-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1da24-112">Requirements</span></span>



| <span data-ttu-id="1da24-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1da24-113">Requirement</span></span> | <span data-ttu-id="1da24-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1da24-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1da24-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1da24-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1da24-116">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1da24-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="1da24-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1da24-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1da24-118">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1da24-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1da24-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1da24-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1da24-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1da24-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1da24-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1da24-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1da24-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1da24-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1da24-123">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="1da24-123">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
