---
description: Specifica la data dell'Ultima modifica di una presentazione.
ms.assetid: 12990de2-7656-4781-943b-c46f42a0e38d
title: Attributo MF_PD_LAST_MODIFIED_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f97bf47cff32834b694f36cbd4c9062e06f2d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967843"
---
# <a name="mf_pd_last_modified_time-attribute"></a><span data-ttu-id="819f1-103">\_ \_ \_ Attributo ora Ultima modifica MF PD \_</span><span class="sxs-lookup"><span data-stu-id="819f1-103">MF\_PD\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="819f1-104">Specifica la data dell'Ultima modifica di una presentazione.</span><span class="sxs-lookup"><span data-stu-id="819f1-104">Specifies when a presentation was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="819f1-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="819f1-105">Data type</span></span>

<span data-ttu-id="819f1-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="819f1-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="819f1-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="819f1-107">Remarks</span></span>

<span data-ttu-id="819f1-108">Le origini supporto possono impostare questo attributo in un descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="819f1-108">Media sources can set this attribute on a presentation descriptor.</span></span> <span data-ttu-id="819f1-109">Il valore dell'attributo è una struttura **FILETIME** , documentata nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="819f1-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="819f1-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="819f1-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="819f1-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="819f1-111">Requirements</span></span>



| <span data-ttu-id="819f1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="819f1-112">Requirement</span></span> | <span data-ttu-id="819f1-113">Valore</span><span class="sxs-lookup"><span data-stu-id="819f1-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="819f1-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="819f1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="819f1-115">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="819f1-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="819f1-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="819f1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="819f1-117">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="819f1-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="819f1-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="819f1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="819f1-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="819f1-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="819f1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="819f1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="819f1-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="819f1-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="819f1-122">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="819f1-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="819f1-123">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="819f1-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="819f1-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="819f1-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="819f1-125">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="819f1-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




