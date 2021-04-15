---
title: Proprietà DeviceById di IMsRdpDeviceCollection
description: Recupera il dispositivo con l'identificatore specificato.
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DeviceById
- Servizi Desktop remoto proprietà DeviceById, interfaccia IMsRdpDeviceCollection
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto, proprietà DeviceById
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228e3c7cf03457ca740d4a415257008988215077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476450"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a><span data-ttu-id="b99c2-106">IMsRdpDeviceCollection::D Proprietà eviceById</span><span class="sxs-lookup"><span data-stu-id="b99c2-106">IMsRdpDeviceCollection::DeviceById property</span></span>

<span data-ttu-id="b99c2-107">Recupera il dispositivo con l'identificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="b99c2-107">Retrieves the device with the specified identifier.</span></span>

<span data-ttu-id="b99c2-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b99c2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b99c2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b99c2-109">Syntax</span></span>


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="b99c2-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b99c2-110">Property value</span></span>

<span data-ttu-id="b99c2-111">Puntatore di interfaccia [**IMsRdpDevice**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="b99c2-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b99c2-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b99c2-112">Error codes</span></span>

<span data-ttu-id="b99c2-113">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="b99c2-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="b99c2-114">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="b99c2-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b99c2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b99c2-115">Requirements</span></span>



| <span data-ttu-id="b99c2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b99c2-116">Requirement</span></span> | <span data-ttu-id="b99c2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b99c2-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b99c2-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b99c2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b99c2-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b99c2-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="b99c2-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b99c2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b99c2-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b99c2-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b99c2-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b99c2-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="b99c2-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b99c2-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="b99c2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b99c2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b99c2-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b99c2-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="b99c2-126">IID</span><span class="sxs-lookup"><span data-stu-id="b99c2-126">IID</span></span><br/>                      | <span data-ttu-id="b99c2-127">IID \_ IMsRdpDeviceCollection è definito come 56540617-D281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="b99c2-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b99c2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b99c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b99c2-129">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="b99c2-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





