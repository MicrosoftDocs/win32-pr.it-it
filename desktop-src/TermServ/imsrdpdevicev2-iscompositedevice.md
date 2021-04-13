---
title: Proprietà IsCompositeDevice di IMsRdpDeviceV2
description: Specifica se il dispositivo è un dispositivo composito.
ms.assetid: cc54f3f0-de0b-4f75-b5a1-4f061ac95ab5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà IsCompositeDevice
- Servizi Desktop remoto proprietà IsCompositeDevice, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, proprietà IsCompositeDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsCompositeDevice
- IMsRdpDeviceV2.get_IsCompositeDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2341544543f436272486a839ffdd3ee68a4a4478
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475220"
---
# <a name="imsrdpdevicev2iscompositedevice-property"></a><span data-ttu-id="ca0c6-106">Proprietà IMsRdpDeviceV2:: IsCompositeDevice</span><span class="sxs-lookup"><span data-stu-id="ca0c6-106">IMsRdpDeviceV2::IsCompositeDevice property</span></span>

<span data-ttu-id="ca0c6-107">Specifica se il dispositivo è un dispositivo composito.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-107">Specifies if the device is a composite device.</span></span>

<span data-ttu-id="ca0c6-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca0c6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca0c6-109">Syntax</span></span>


```C++
HRESULT get_IsCompositeDevice(
  [out, retval] VARIANT_BOOL *pvboolCompositeDevice
);
```



## <a name="property-value"></a><span data-ttu-id="ca0c6-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ca0c6-110">Property value</span></span>

<span data-ttu-id="ca0c6-111">**true** se il dispositivo è un dispositivo composito; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="ca0c6-111">**true** if the device is a composite device; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca0c6-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca0c6-112">Requirements</span></span>



| <span data-ttu-id="ca0c6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca0c6-113">Requirement</span></span> | <span data-ttu-id="ca0c6-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ca0c6-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca0c6-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca0c6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ca0c6-116">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="ca0c6-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="ca0c6-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca0c6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ca0c6-118">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="ca0c6-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="ca0c6-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ca0c6-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca0c6-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca0c6-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ca0c6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ca0c6-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca0c6-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca0c6-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ca0c6-123">IID</span><span class="sxs-lookup"><span data-stu-id="ca0c6-123">IID</span></span><br/>                      | <span data-ttu-id="ca0c6-124">IID \_ IMsRdpDeviceV2 è definito come 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="ca0c6-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="ca0c6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca0c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca0c6-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="ca0c6-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





