---
description: Indica all'allocatore del video di esempio di creare trame come condivisibili usando il meccanismo legacy.
ms.assetid: A9F4D4AF-BB47-48E2-B40A-D0245FD61FAF
title: Attributo MF_SA_D3D11_SHARED_WITHOUT_MUTEX (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9139328c9d272007be6e5cd9434614cb1de8c9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308462"
---
# <a name="mf_sa_d3d11_shared_without_mutex-attribute"></a><span data-ttu-id="70b60-103">MF \_ sa \_ d3d11 \_ condiviso \_ senza l' \_ attributo mutex</span><span class="sxs-lookup"><span data-stu-id="70b60-103">MF\_SA\_D3D11\_SHARED\_WITHOUT\_MUTEX attribute</span></span>

<span data-ttu-id="70b60-104">Indica all'allocatore del video di esempio di creare trame come condivisibili usando il meccanismo legacy.</span><span class="sxs-lookup"><span data-stu-id="70b60-104">Indicates to the video sample allocator to create textures as shareable using the legacy mechanism.</span></span>

## <a name="data-type"></a><span data-ttu-id="70b60-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="70b60-105">Data type</span></span>

<span data-ttu-id="70b60-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="70b60-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="70b60-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="70b60-107">Remarks</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="70b60-108">Allocatore di esempio</span><span class="sxs-lookup"><span data-stu-id="70b60-108">Sample Allocator</span></span>

<span data-ttu-id="70b60-109">Questo attributo può essere impostato nell'allocatore video di esempio, nel metodo [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="70b60-109">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="70b60-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70b60-110">Requirements</span></span>



| <span data-ttu-id="70b60-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="70b60-111">Requirement</span></span> | <span data-ttu-id="70b60-112">Valore</span><span class="sxs-lookup"><span data-stu-id="70b60-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b60-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70b60-113">Minimum supported client</span></span><br/> | <span data-ttu-id="70b60-114">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="70b60-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="70b60-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70b60-115">Minimum supported server</span></span><br/> | <span data-ttu-id="70b60-116">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="70b60-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="70b60-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70b60-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="70b60-118"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="70b60-118"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70b60-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70b60-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b60-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="70b60-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="70b60-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span><span class="sxs-lookup"><span data-stu-id="70b60-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[<span data-ttu-id="70b60-122">MF \_ sa \_ d3d11 \_ condiviso</span><span class="sxs-lookup"><span data-stu-id="70b60-122">MF\_SA\_D3D11\_SHARED</span></span>](mf-sa-d3d11-shared.md)
</dt> </dl>

 

 




