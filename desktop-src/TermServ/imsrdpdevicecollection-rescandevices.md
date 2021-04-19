---
title: Metodo IMsRdpDeviceCollection RescanDevices
description: Aggiorna l'elenco di oggetti nella raccolta. | Metodo IMsRdpDeviceCollection RescanDevices
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RescanDevices
- Metodo RescanDevices Servizi Desktop remoto, interfaccia IMsRdpDeviceCollection
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto, metodo RescanDevices
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773231ffd89a0998f6073f844a3f974920625987
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321770"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a><span data-ttu-id="c3a13-107">Metodo IMsRdpDeviceCollection:: RescanDevices</span><span class="sxs-lookup"><span data-stu-id="c3a13-107">IMsRdpDeviceCollection::RescanDevices method</span></span>

<span data-ttu-id="c3a13-108">Aggiorna l'elenco di oggetti nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="c3a13-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a13-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3a13-109">Syntax</span></span>


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="c3a13-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3a13-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3a13-111">*vboolDynRedir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3a13-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3a13-112">Stato di reindirizzamento predefinito che verrà applicato alle unità o ai dispositivi appena individuati.</span><span class="sxs-lookup"><span data-stu-id="c3a13-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3a13-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3a13-113">Return value</span></span>

<span data-ttu-id="c3a13-114">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="c3a13-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="c3a13-115">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="c3a13-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a13-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3a13-116">Requirements</span></span>



| <span data-ttu-id="c3a13-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3a13-117">Requirement</span></span> | <span data-ttu-id="c3a13-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c3a13-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a13-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3a13-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c3a13-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3a13-120">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="c3a13-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3a13-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c3a13-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3a13-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c3a13-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c3a13-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c3a13-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3a13-124"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c3a13-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c3a13-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3a13-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3a13-126"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c3a13-127">IID</span><span class="sxs-lookup"><span data-stu-id="c3a13-127">IID</span></span><br/>                      | <span data-ttu-id="c3a13-128">IID \_ IMsRdpDeviceCollection è definito come 56540617-D281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="c3a13-128">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3a13-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3a13-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a13-130">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="c3a13-130">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





