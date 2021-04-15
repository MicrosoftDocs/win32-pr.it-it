---
description: Specifica se la trasformazione associata a un nodo della topologia supporta l'accelerazione video DirectX (DXVA).
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: Attributo MF_TOPONODE_D3DAWARE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485812"
---
# <a name="mf_toponode_d3daware-attribute"></a><span data-ttu-id="e3b43-103">\_Attributo MF TOPONODE \_ D3DAWARE</span><span class="sxs-lookup"><span data-stu-id="e3b43-103">MF\_TOPONODE\_D3DAWARE attribute</span></span>

<span data-ttu-id="e3b43-104">Specifica se la trasformazione associata a un nodo della topologia supporta l'accelerazione video DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="e3b43-104">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA).</span></span>

## <a name="data-type"></a><span data-ttu-id="e3b43-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e3b43-105">Data type</span></span>

<span data-ttu-id="e3b43-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e3b43-106">**UINT32**</span></span>

<span data-ttu-id="e3b43-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="e3b43-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3b43-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3b43-108">Remarks</span></span>

<span data-ttu-id="e3b43-109">Questo attributo si applica ai nodi di trasformazione (**\_ nodo di \_ trasformazione \_ della topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="e3b43-109">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="e3b43-110">Le applicazioni in genere non utilizzano direttamente questo attributo.</span><span class="sxs-lookup"><span data-stu-id="e3b43-110">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="e3b43-111">La sessione multimediale imposta questo attributo su un nodo di trasformazione se la trasformazione Media Foundation sottostante dispone dell'attributo in grado di riconoscere la tecnologia [**MF \_ sa \_ D3D \_**](mf-sa-d3d-aware-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e3b43-111">The Media Session sets this attribute on a transform node if the underlying Media Foundation transform has the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute.</span></span>

<span data-ttu-id="e3b43-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e3b43-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b43-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3b43-113">Requirements</span></span>



| <span data-ttu-id="e3b43-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b43-114">Requirement</span></span> | <span data-ttu-id="e3b43-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e3b43-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b43-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3b43-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e3b43-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3b43-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e3b43-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3b43-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e3b43-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3b43-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e3b43-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3b43-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3b43-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b43-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b43-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3b43-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b43-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3b43-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e3b43-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="e3b43-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e3b43-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="e3b43-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e3b43-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="e3b43-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e3b43-127">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="e3b43-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




