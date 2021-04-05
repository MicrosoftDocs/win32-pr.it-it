---
title: Proprietà DeviceDescription di IMsRdpDevice
description: Recupera la descrizione del dispositivo da visualizzare all'utente se il nome visualizzato non è disponibile.
ms.assetid: 969f96c6-5655-4cac-9e91-059114dc3815
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DeviceDescription
- Servizi Desktop remoto proprietà DeviceDescription, interfaccia IMsRdpDevice
- Interfaccia IMsRdpDevice Servizi Desktop remoto, proprietà DeviceDescription
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceDescription
- IMsRdpDevice.get_DeviceDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e352acef945c09c6be592174dd86a46cd8689aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120394"
---
# <a name="imsrdpdevicedevicedescription-property"></a><span data-ttu-id="208f9-106">IMsRdpDevice::D Proprietà eviceDescription</span><span class="sxs-lookup"><span data-stu-id="208f9-106">IMsRdpDevice::DeviceDescription property</span></span>

<span data-ttu-id="208f9-107">Recupera la descrizione del dispositivo da visualizzare all'utente se il nome visualizzato non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="208f9-107">Retrieves the device description to be displayed to the user if the display name is not available.</span></span>

<span data-ttu-id="208f9-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="208f9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="208f9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="208f9-109">Syntax</span></span>


```C++
HRESULT get_DeviceDescription(
  [out] BSTR *pDeviceDescription
);
```



## <a name="property-value"></a><span data-ttu-id="208f9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="208f9-110">Property value</span></span>

<span data-ttu-id="208f9-111">Descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="208f9-111">The device description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="208f9-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="208f9-112">Error codes</span></span>

<span data-ttu-id="208f9-113">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="208f9-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="208f9-114">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="208f9-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="208f9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="208f9-115">Requirements</span></span>



| <span data-ttu-id="208f9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="208f9-116">Requirement</span></span> | <span data-ttu-id="208f9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="208f9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="208f9-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="208f9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="208f9-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="208f9-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="208f9-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="208f9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="208f9-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="208f9-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="208f9-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="208f9-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="208f9-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="208f9-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="208f9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="208f9-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="208f9-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="208f9-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="208f9-126">IID</span><span class="sxs-lookup"><span data-stu-id="208f9-126">IID</span></span><br/>                      | <span data-ttu-id="208f9-127">IID \_ IMsRdpDevice è definito come 60c3b9c8-9E92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="208f9-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="208f9-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="208f9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="208f9-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="208f9-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





