---
title: Proprietà CmDeviceInstance di IMsRdpDeviceV2
description: Contiene l'istanza del dispositivo di Configuration Manager del dispositivo.
ms.assetid: 2a3e7001-7889-417f-8f9d-cc7a1776249f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà CmDeviceInstance
- Servizi Desktop remoto proprietà CmDeviceInstance, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, proprietà CmDeviceInstance
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmDeviceInstance
- IMsRdpDeviceV2.get_CmDeviceInstance
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec036d5e2497f45fff389ec8af457a05fcc9fef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300990"
---
# <a name="imsrdpdevicev2cmdeviceinstance-property"></a><span data-ttu-id="58e6a-106">Proprietà IMsRdpDeviceV2:: CmDeviceInstance</span><span class="sxs-lookup"><span data-stu-id="58e6a-106">IMsRdpDeviceV2::CmDeviceInstance property</span></span>

<span data-ttu-id="58e6a-107">Contiene l'istanza del dispositivo di Configuration Manager del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58e6a-107">Contains the configuration manager device instance of the device.</span></span>

<span data-ttu-id="58e6a-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="58e6a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e6a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58e6a-109">Syntax</span></span>


```C++
HRESULT get_CmDeviceInstance(
  [out, retval] DWORD *pCmDeviceInstance
);
```



## <a name="property-value"></a><span data-ttu-id="58e6a-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="58e6a-110">Property value</span></span>

<span data-ttu-id="58e6a-111">Istanza del dispositivo di Configuration Manager del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58e6a-111">The configuration manager device instance of the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e6a-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58e6a-112">Requirements</span></span>



| <span data-ttu-id="58e6a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="58e6a-113">Requirement</span></span> | <span data-ttu-id="58e6a-114">Valore</span><span class="sxs-lookup"><span data-stu-id="58e6a-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58e6a-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58e6a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="58e6a-116">Windows 7 con SP1</span><span class="sxs-lookup"><span data-stu-id="58e6a-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="58e6a-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58e6a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="58e6a-118">Windows Server 2008 R2 con SP1</span><span class="sxs-lookup"><span data-stu-id="58e6a-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="58e6a-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="58e6a-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="58e6a-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e6a-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="58e6a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="58e6a-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58e6a-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e6a-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="58e6a-123">IID</span><span class="sxs-lookup"><span data-stu-id="58e6a-123">IID</span></span><br/>                      | <span data-ttu-id="58e6a-124">IID \_ IMsRdpDeviceV2 è definito come 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="58e6a-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="58e6a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58e6a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e6a-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="58e6a-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





