---
description: Indica all'allocatore del video di esempio di creare trame condivisibili tramite mutex con chiave.
ms.assetid: 798CA474-3B1A-4795-81B7-563749197104
title: Attributo MF_SA_D3D11_SHARED (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6ecb23a99a732e183bc16942e33bbb4f8e3a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231773"
---
# <a name="mf_sa_d3d11_shared-attribute"></a><span data-ttu-id="f23e8-103">\_ \_ Attributo condiviso MF SA d3d11 \_</span><span class="sxs-lookup"><span data-stu-id="f23e8-103">MF\_SA\_D3D11\_SHARED attribute</span></span>

<span data-ttu-id="f23e8-104">Indica all'allocatore del video di esempio di creare trame condivisibili tramite mutex con chiave.</span><span class="sxs-lookup"><span data-stu-id="f23e8-104">Indicates to the video sample allocator to create textures as shareable using keyed-mutex.</span></span>

## <a name="data-type"></a><span data-ttu-id="f23e8-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f23e8-105">Data type</span></span>

<span data-ttu-id="f23e8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f23e8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f23e8-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f23e8-107">Remarks</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="f23e8-108">Allocatore di esempio</span><span class="sxs-lookup"><span data-stu-id="f23e8-108">Sample Allocator</span></span>

<span data-ttu-id="f23e8-109">Questo attributo può essere impostato nell'allocatore video di esempio, nel metodo [**IMFVideoSampleAllocatorEx:: InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) .</span><span class="sxs-lookup"><span data-stu-id="f23e8-109">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f23e8-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f23e8-110">Requirements</span></span>



| <span data-ttu-id="f23e8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f23e8-111">Requirement</span></span> | <span data-ttu-id="f23e8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f23e8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f23e8-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f23e8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f23e8-114">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f23e8-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f23e8-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f23e8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f23e8-116">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="f23e8-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f23e8-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f23e8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f23e8-118"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="f23e8-118"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23e8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f23e8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23e8-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f23e8-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f23e8-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span><span class="sxs-lookup"><span data-stu-id="f23e8-121">**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex)
</dt> <dt>

[<span data-ttu-id="f23e8-122">MF \_ sa \_ d3d11 \_ condiviso \_ senza \_ mutex</span><span class="sxs-lookup"><span data-stu-id="f23e8-122">MF\_SA\_D3D11\_SHARED\_WITHOUT\_MUTEX</span></span>](mf-sa-d3d11-shared-without-mutex.md)
</dt> </dl>

 

 




