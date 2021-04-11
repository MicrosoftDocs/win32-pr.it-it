---
title: Proprietà TransportSettings di IMsRdpClient5
description: Recupera gli elementi passati tramite uno script all'interfaccia IMsRdpClientTransportSettings.
ms.assetid: 38f5a735-55c7-425a-835b-22f6e0900d57
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Proprietà TransportSettings
- Servizi Desktop remoto Proprietà TransportSettings, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, Proprietà TransportSettings
- Servizi Desktop remoto Proprietà TransportSettings, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, Proprietà TransportSettings
- Servizi Desktop remoto Proprietà TransportSettings, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, Proprietà TransportSettings
- Servizi Desktop remoto Proprietà TransportSettings, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, Proprietà TransportSettings
- Servizi Desktop remoto Proprietà TransportSettings, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, Proprietà TransportSettings
- Servizi Desktop remoto Proprietà TransportSettings, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, Proprietà TransportSettings
topic_type:
- apiref
api_name:
- IMsRdpClient5.TransportSettings
- IMsRdpClient5.get_TransportSettings
- IMsRdpClient6.TransportSettings
- IMsRdpClient6.get_TransportSettings
- IMsRdpClient7.TransportSettings
- IMsRdpClient7.get_TransportSettings
- IMsRdpClient8.TransportSettings
- IMsRdpClient8.get_TransportSettings
- IMsRdpClient9.TransportSettings
- IMsRdpClient9.get_TransportSettings
- IMsRdpClient10.TransportSettings
- IMsRdpClient10.get_TransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077ed94253c0ebadeed775e54c4db2ae6cbacf13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119270"
---
# <a name="imsrdpclient5transportsettings-property"></a><span data-ttu-id="d6ce6-116">Proprietà IMsRdpClient5:: TransportSettings</span><span class="sxs-lookup"><span data-stu-id="d6ce6-116">IMsRdpClient5::TransportSettings property</span></span>

<span data-ttu-id="d6ce6-117">Recupera gli elementi passati tramite uno script all'interfaccia [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="d6ce6-117">Retrieves what was passed through a script to the [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface.</span></span>

<span data-ttu-id="d6ce6-118">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d6ce6-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ce6-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6ce6-119">Syntax</span></span>


```C++
HRESULT get_TransportSettings(
  [out] IMsRdpClientTransportSettings **ppXportSet
);
```



## <a name="property-value"></a><span data-ttu-id="d6ce6-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d6ce6-120">Property value</span></span>

<span data-ttu-id="d6ce6-121">Puntatore di interfaccia [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="d6ce6-121">An [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6ce6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6ce6-122">Requirements</span></span>



| <span data-ttu-id="d6ce6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6ce6-123">Requirement</span></span> | <span data-ttu-id="d6ce6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d6ce6-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ce6-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6ce6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d6ce6-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6ce6-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d6ce6-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6ce6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d6ce6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6ce6-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d6ce6-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d6ce6-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6ce6-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6ce6-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d6ce6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d6ce6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6ce6-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6ce6-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d6ce6-133">IID</span><span class="sxs-lookup"><span data-stu-id="d6ce6-133">IID</span></span><br/>                      | <span data-ttu-id="d6ce6-134">IID \_ IMsRdpClient5 è definito come 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="d6ce6-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d6ce6-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6ce6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6ce6-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="d6ce6-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="d6ce6-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="d6ce6-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="d6ce6-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="d6ce6-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="d6ce6-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="d6ce6-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="d6ce6-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d6ce6-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d6ce6-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="d6ce6-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





