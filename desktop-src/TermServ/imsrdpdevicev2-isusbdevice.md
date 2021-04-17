---
title: Proprietà IsUSBDevice di IMsRdpDeviceV2
description: Specifica se il dispositivo è per il reindirizzamento USB.
ms.assetid: df4c9764-ad96-4f35-9537-3890293a944c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà IsUSBDevice
- Servizi Desktop remoto proprietà IsUSBDevice, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, proprietà IsUSBDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsUSBDevice
- IMsRdpDeviceV2.get_IsUSBDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3741972fdd81887713e75ed5b596e0ba1a10fd3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400233"
---
# <a name="imsrdpdevicev2isusbdevice-property"></a><span data-ttu-id="bfb59-106">Proprietà IMsRdpDeviceV2:: IsUSBDevice</span><span class="sxs-lookup"><span data-stu-id="bfb59-106">IMsRdpDeviceV2::IsUSBDevice property</span></span>

<span data-ttu-id="bfb59-107">Specifica se il dispositivo è per il reindirizzamento USB.</span><span class="sxs-lookup"><span data-stu-id="bfb59-107">Specifies if the device is for USB redirection.</span></span>

<span data-ttu-id="bfb59-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bfb59-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfb59-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfb59-109">Syntax</span></span>


```C++
HRESULT get_IsUSBDevice(
  [out, retval] VARIANT_BOOL *pvboolUSBDevice
);
```



## <a name="property-value"></a><span data-ttu-id="bfb59-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bfb59-110">Property value</span></span>

<span data-ttu-id="bfb59-111">**true** se il dispositivo è per il reindirizzamento USB; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfb59-111">**true** if the device is for USB redirection; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfb59-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfb59-112">Requirements</span></span>



| <span data-ttu-id="bfb59-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfb59-113">Requirement</span></span> | <span data-ttu-id="bfb59-114">Valore</span><span class="sxs-lookup"><span data-stu-id="bfb59-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb59-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfb59-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bfb59-116">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="bfb59-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="bfb59-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfb59-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bfb59-118">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="bfb59-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="bfb59-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bfb59-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="bfb59-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfb59-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfb59-121">DLL</span><span class="sxs-lookup"><span data-stu-id="bfb59-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfb59-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfb59-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfb59-123">IID</span><span class="sxs-lookup"><span data-stu-id="bfb59-123">IID</span></span><br/>                      | <span data-ttu-id="bfb59-124">IID \_ IMsRdpDeviceV2 è definito come 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="bfb59-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="bfb59-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfb59-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfb59-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="bfb59-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





