---
description: Per i tipi di Supporto YUV, definisce la matrice di conversione dallo spazio colore YCbCr allo spazio colore RGB.
ms.assetid: b268d16d-b4cc-4026-9ba7-805cc5409b95
title: Attributo MF_MT_YUV_MATRIX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0c6976e4652c69b3bddc910dcc536a3d07bf39a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318060"
---
# <a name="mf_mt_yuv_matrix-attribute"></a><span data-ttu-id="ce69f-103">\_ \_ Attributo matrice YUV MF mt \_</span><span class="sxs-lookup"><span data-stu-id="ce69f-103">MF\_MT\_YUV\_MATRIX attribute</span></span>

<span data-ttu-id="ce69f-104">Per i tipi di Supporto YUV, definisce la matrice di conversione dallo spazio colore Cb'Cr "allo spazio colore SOTTOCAMPIONATURA".</span><span class="sxs-lookup"><span data-stu-id="ce69f-104">For YUV media types, defines the conversion matrix from the Y'Cb'Cr' color space to the R'G'B' color space.</span></span>

## <a name="data-type"></a><span data-ttu-id="ce69f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ce69f-105">Data type</span></span>

<span data-ttu-id="ce69f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ce69f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ce69f-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce69f-107">Remarks</span></span>

<span data-ttu-id="ce69f-108">Il valore di questo attributo è un membro dell'enumerazione [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) .</span><span class="sxs-lookup"><span data-stu-id="ce69f-108">The value of this attribute is a member of the [**MFVideoTransferMatrix**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix) enumeration.</span></span>

<span data-ttu-id="ce69f-109">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ce69f-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce69f-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce69f-110">Requirements</span></span>



| <span data-ttu-id="ce69f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce69f-111">Requirement</span></span> | <span data-ttu-id="ce69f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="ce69f-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce69f-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce69f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ce69f-114">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ce69f-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ce69f-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce69f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ce69f-116">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ce69f-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ce69f-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce69f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce69f-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce69f-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce69f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce69f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce69f-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce69f-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce69f-121">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="ce69f-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ce69f-122">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="ce69f-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ce69f-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="ce69f-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ce69f-124">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="ce69f-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce69f-125">Informazioni sui colori estesi</span><span class="sxs-lookup"><span data-stu-id="ce69f-125">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




