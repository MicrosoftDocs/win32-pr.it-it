---
description: Specifica se la sessione multimediale usa il preroll sul sink multimediale rappresentato da questo nodo di topologia.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: Attributo MF_TOPONODE_DISABLE_PREROLL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318045"
---
# <a name="mf_toponode_disable_preroll-attribute"></a><span data-ttu-id="15f40-103">MF \_ TOPONODE \_ disabilitare l' \_ attributo preroll</span><span class="sxs-lookup"><span data-stu-id="15f40-103">MF\_TOPONODE\_DISABLE\_PREROLL attribute</span></span>

<span data-ttu-id="15f40-104">Specifica se la sessione multimediale usa il preroll sul sink multimediale rappresentato da questo nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="15f40-104">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="15f40-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="15f40-105">Data type</span></span>

<span data-ttu-id="15f40-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="15f40-106">**UINT32**</span></span>

<span data-ttu-id="15f40-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="15f40-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15f40-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="15f40-108">Remarks</span></span>

<span data-ttu-id="15f40-109">Questo attributo si applica ai nodi di output (**\_ nodo di \_ output \_ della topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="15f40-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="15f40-110">Se il valore di questo attributo è **true**, la sessione multimediale non esegue la preregistrazione dei dati nel sink multimediale, anche se il sink multimediale espone l'interfaccia [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) .</span><span class="sxs-lookup"><span data-stu-id="15f40-110">If the value of this attribute is **TRUE**, the Media Session does not preroll any data to the media sink, even if the media sink exposes the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span> <span data-ttu-id="15f40-111">Se il valore è **false**, la sessione multimediale esegue il prerolling dei dati se il sink multimediale implementa **IMFMediaSinkPreroll**.</span><span class="sxs-lookup"><span data-stu-id="15f40-111">If the value is **FALSE**, the Media Session prerolls data if the media sink implements **IMFMediaSinkPreroll**.</span></span> <span data-ttu-id="15f40-112">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="15f40-112">The default value is **FALSE**.</span></span>

<span data-ttu-id="15f40-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="15f40-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="15f40-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15f40-114">Requirements</span></span>



| <span data-ttu-id="15f40-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="15f40-115">Requirement</span></span> | <span data-ttu-id="15f40-116">Valore</span><span class="sxs-lookup"><span data-stu-id="15f40-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15f40-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15f40-117">Minimum supported client</span></span><br/> | <span data-ttu-id="15f40-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15f40-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="15f40-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15f40-119">Minimum supported server</span></span><br/> | <span data-ttu-id="15f40-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15f40-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="15f40-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15f40-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="15f40-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="15f40-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15f40-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15f40-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f40-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15f40-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="15f40-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="15f40-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="15f40-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="15f40-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="15f40-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="15f40-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="15f40-128">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="15f40-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




