---
title: Proprietà DeviceByIndex di IMsRdpDeviceCollection
description: Recupera il dispositivo in corrispondenza dell'indice specificato.
ms.assetid: fcfc459b-46e1-4f26-a331-745fcf06638b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DeviceByIndex
- Servizi Desktop remoto proprietà DeviceByIndex, interfaccia IMsRdpDeviceCollection
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto, proprietà DeviceByIndex
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceByIndex
- IMsRdpDeviceCollection.get_DeviceByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12d763d4c147efa26e904a1903149504ee557ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479282"
---
# <a name="imsrdpdevicecollectiondevicebyindex-property"></a><span data-ttu-id="e3a6f-106">IMsRdpDeviceCollection::D Proprietà eviceByIndex</span><span class="sxs-lookup"><span data-stu-id="e3a6f-106">IMsRdpDeviceCollection::DeviceByIndex property</span></span>

<span data-ttu-id="e3a6f-107">Recupera il dispositivo in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="e3a6f-107">Retrieves the device at the specified index.</span></span>

<span data-ttu-id="e3a6f-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e3a6f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a6f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3a6f-109">Syntax</span></span>


```C++
HRESULT get_DeviceByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="e3a6f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e3a6f-110">Property value</span></span>

<span data-ttu-id="e3a6f-111">Puntatore di interfaccia [**IMsRdpDevice**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="e3a6f-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e3a6f-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e3a6f-112">Error codes</span></span>

<span data-ttu-id="e3a6f-113">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="e3a6f-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="e3a6f-114">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e3a6f-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a6f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3a6f-115">Requirements</span></span>



| <span data-ttu-id="e3a6f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a6f-116">Requirement</span></span> | <span data-ttu-id="e3a6f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e3a6f-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a6f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3a6f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e3a6f-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3a6f-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="e3a6f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3a6f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e3a6f-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3a6f-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e3a6f-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e3a6f-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3a6f-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3a6f-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="e3a6f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e3a6f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3a6f-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3a6f-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="e3a6f-126">IID</span><span class="sxs-lookup"><span data-stu-id="e3a6f-126">IID</span></span><br/>                      | <span data-ttu-id="e3a6f-127">IID \_ IMsRdpDeviceCollection è definito come 56540617-D281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="e3a6f-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3a6f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3a6f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a6f-129">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="e3a6f-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





