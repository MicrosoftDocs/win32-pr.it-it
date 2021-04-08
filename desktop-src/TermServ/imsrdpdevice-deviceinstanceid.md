---
title: Proprietà DeviceInstanceId di IMsRdpDevice
description: Recupera l'identificatore dell'istanza del dispositivo.
ms.assetid: 54bdda17-39da-4821-9ac3-2ce80f5015f4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DeviceInstanceId
- Servizi Desktop remoto proprietà DeviceInstanceId, interfaccia IMsRdpDevice
- Interfaccia IMsRdpDevice Servizi Desktop remoto, proprietà DeviceInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceInstanceId
- IMsRdpDevice.get_DeviceInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a159911e4294e2207ad4ae989d4ef9e390384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964975"
---
# <a name="imsrdpdevicedeviceinstanceid-property"></a><span data-ttu-id="63590-106">IMsRdpDevice::D Proprietà eviceInstanceId</span><span class="sxs-lookup"><span data-stu-id="63590-106">IMsRdpDevice::DeviceInstanceId property</span></span>

<span data-ttu-id="63590-107">Recupera l'identificatore dell'istanza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63590-107">Retrieves the device instance identifier of the device.</span></span>

<span data-ttu-id="63590-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="63590-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63590-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63590-109">Syntax</span></span>


```C++
HRESULT get_DeviceInstanceId(
  [out] BSTR *pDevInstanceId
);
```



## <a name="property-value"></a><span data-ttu-id="63590-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="63590-110">Property value</span></span>

<span data-ttu-id="63590-111">Identificatore dell'istanza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="63590-111">The device instance identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63590-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="63590-112">Error codes</span></span>

<span data-ttu-id="63590-113">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="63590-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="63590-114">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="63590-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="63590-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63590-115">Requirements</span></span>



| <span data-ttu-id="63590-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="63590-116">Requirement</span></span> | <span data-ttu-id="63590-117">Valore</span><span class="sxs-lookup"><span data-stu-id="63590-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63590-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63590-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63590-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63590-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="63590-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63590-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63590-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63590-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="63590-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="63590-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="63590-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63590-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="63590-124">DLL</span><span class="sxs-lookup"><span data-stu-id="63590-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63590-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63590-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="63590-126">IID</span><span class="sxs-lookup"><span data-stu-id="63590-126">IID</span></span><br/>                      | <span data-ttu-id="63590-127">IID \_ IMsRdpDevice è definito come 60c3b9c8-9E92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="63590-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="63590-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63590-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63590-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="63590-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





