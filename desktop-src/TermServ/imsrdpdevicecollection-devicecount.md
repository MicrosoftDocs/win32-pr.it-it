---
title: Proprietà DeviceCount di IMsRdpDeviceCollection
description: Recupera il numero di oggetti nella raccolta. | Proprietà DeviceCount di IMsRdpDeviceCollection
ms.assetid: dc44f3b8-52c4-4e5f-a633-ea7555fd01dd
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DeviceCount
- Servizi Desktop remoto proprietà DeviceCount, interfaccia IMsRdpDeviceCollection
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto, proprietà DeviceCount
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceCount
- IMsRdpDeviceCollection.get_DeviceCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a389cd89699eb383b9f235858f0cf4a052606a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321579"
---
# <a name="imsrdpdevicecollectiondevicecount-property"></a><span data-ttu-id="e885d-107">IMsRdpDeviceCollection::D Proprietà eviceCount</span><span class="sxs-lookup"><span data-stu-id="e885d-107">IMsRdpDeviceCollection::DeviceCount property</span></span>

<span data-ttu-id="e885d-108">Recupera il numero di oggetti nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="e885d-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="e885d-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e885d-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e885d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e885d-110">Syntax</span></span>


```C++
HRESULT get_DeviceCount(
  [out] ULONG *pDeviceCount
);
```



## <a name="property-value"></a><span data-ttu-id="e885d-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e885d-111">Property value</span></span>

<span data-ttu-id="e885d-112">Conteggio oggetti.</span><span class="sxs-lookup"><span data-stu-id="e885d-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e885d-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e885d-113">Error codes</span></span>

<span data-ttu-id="e885d-114">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="e885d-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="e885d-115">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e885d-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e885d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e885d-116">Requirements</span></span>



| <span data-ttu-id="e885d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e885d-117">Requirement</span></span> | <span data-ttu-id="e885d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e885d-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e885d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e885d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e885d-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e885d-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="e885d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e885d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e885d-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e885d-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e885d-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e885d-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="e885d-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e885d-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="e885d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e885d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e885d-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e885d-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="e885d-127">IID</span><span class="sxs-lookup"><span data-stu-id="e885d-127">IID</span></span><br/>                      | <span data-ttu-id="e885d-128">IID \_ IMsRdpDeviceCollection è definito come 56540617-D281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="e885d-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e885d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e885d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e885d-130">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="e885d-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





