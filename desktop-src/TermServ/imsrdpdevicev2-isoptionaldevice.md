---
title: Proprietà IsOptionalDevice di IMsRdpDeviceV2
description: Specifica se il dispositivo è facoltativo per il reindirizzamento USB.
ms.assetid: a7226c40-7e22-48af-9895-b1fb1f861b58
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà IsOptionalDevice
- Servizi Desktop remoto proprietà IsOptionalDevice, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, proprietà IsOptionalDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsOptionalDevice
- IMsRdpDeviceV2.get_IsOptionalDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad0e459a91e88573515128ca37033768f7839ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477741"
---
# <a name="imsrdpdevicev2isoptionaldevice-property"></a><span data-ttu-id="535ee-106">Proprietà IMsRdpDeviceV2:: IsOptionalDevice</span><span class="sxs-lookup"><span data-stu-id="535ee-106">IMsRdpDeviceV2::IsOptionalDevice property</span></span>

<span data-ttu-id="535ee-107">Specifica se il dispositivo è facoltativo per il reindirizzamento USB.</span><span class="sxs-lookup"><span data-stu-id="535ee-107">Specifies if the device is optional for USB redirection.</span></span>

<span data-ttu-id="535ee-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="535ee-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="535ee-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="535ee-109">Syntax</span></span>


```C++
HRESULT get_IsOptionalDevice(
  [out, retval] VARIANT_BOOL *pvboolOptionalDevice
);
```



## <a name="property-value"></a><span data-ttu-id="535ee-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="535ee-110">Property value</span></span>

<span data-ttu-id="535ee-111">**true** se il dispositivo è facoltativo; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="535ee-111">**true** if the device is a optional; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="535ee-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="535ee-112">Requirements</span></span>



| <span data-ttu-id="535ee-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="535ee-113">Requirement</span></span> | <span data-ttu-id="535ee-114">Valore</span><span class="sxs-lookup"><span data-stu-id="535ee-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="535ee-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="535ee-115">Minimum supported client</span></span><br/> | <span data-ttu-id="535ee-116">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="535ee-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="535ee-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="535ee-117">Minimum supported server</span></span><br/> | <span data-ttu-id="535ee-118">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="535ee-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="535ee-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="535ee-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="535ee-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="535ee-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="535ee-121">DLL</span><span class="sxs-lookup"><span data-stu-id="535ee-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="535ee-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="535ee-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="535ee-123">IID</span><span class="sxs-lookup"><span data-stu-id="535ee-123">IID</span></span><br/>                      | <span data-ttu-id="535ee-124">IID \_ IMsRdpDeviceV2 è definito come 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="535ee-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="535ee-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="535ee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="535ee-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="535ee-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





