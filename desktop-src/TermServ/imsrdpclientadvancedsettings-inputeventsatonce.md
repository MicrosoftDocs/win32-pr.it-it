---
title: Proprietà InputEventsAtOnce di IMsRdpClientAdvancedSettings
description: Questa proprietà non è supportata. | Proprietà InputEventsAtOnce di IMsRdpClientAdvancedSettings
ms.assetid: 2f24b2cd-136d-4bde-9808-e5cb02bd7ce8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà InputEventsAtOnce
- Servizi Desktop remoto proprietà InputEventsAtOnce, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà InputEventsAtOnce
- Servizi Desktop remoto proprietà InputEventsAtOnce, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà InputEventsAtOnce
- Servizi Desktop remoto proprietà InputEventsAtOnce, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà InputEventsAtOnce
- Servizi Desktop remoto proprietà InputEventsAtOnce, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà InputEventsAtOnce
- Servizi Desktop remoto proprietà InputEventsAtOnce, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà InputEventsAtOnce
- Servizi Desktop remoto proprietà InputEventsAtOnce, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà InputEventsAtOnce
- Servizi Desktop remoto proprietà InputEventsAtOnce, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà InputEventsAtOnce
- Servizi Desktop remoto proprietà InputEventsAtOnce, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà InputEventsAtOnce
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.InputEventsAtOnce
- IMsRdpClientAdvancedSettings.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.put_InputEventsAtOnce
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999d00cb706e4fdd4cf0c9ed606c33de4a81e8d6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321580"
---
# <a name="imsrdpclientadvancedsettingsinputeventsatonce-property"></a><span data-ttu-id="a98de-121">Proprietà IMsRdpClientAdvancedSettings:: InputEventsAtOnce</span><span class="sxs-lookup"><span data-stu-id="a98de-121">IMsRdpClientAdvancedSettings::InputEventsAtOnce property</span></span>

<span data-ttu-id="a98de-122">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a98de-122">This property is not supported.</span></span>

<span data-ttu-id="a98de-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a98de-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a98de-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a98de-124">Syntax</span></span>


```C++
HRESULT put_InputEventsAtOnce(
  [in]  LONG inputEventsAtOnce
);

HRESULT get_InputEventsAtOnce(
  [out] LONG *pinputEventsAtOnce
);
```



## <a name="property-value"></a><span data-ttu-id="a98de-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a98de-125">Property value</span></span>

<span data-ttu-id="a98de-126">Nuovo numero di eventi di input.</span><span class="sxs-lookup"><span data-stu-id="a98de-126">The new number of input events.</span></span> <span data-ttu-id="a98de-127">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="a98de-127">The default is 10.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a98de-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a98de-128">Error codes</span></span>

<span data-ttu-id="a98de-129">Restituisce un valore **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="a98de-129">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a98de-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a98de-130">Requirements</span></span>



| <span data-ttu-id="a98de-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a98de-131">Requirement</span></span> | <span data-ttu-id="a98de-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a98de-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a98de-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a98de-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a98de-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a98de-134">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="a98de-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a98de-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a98de-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a98de-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="a98de-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a98de-137">End of client support</span></span><br/>    | <span data-ttu-id="a98de-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a98de-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="a98de-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a98de-139">End of server support</span></span><br/>    | <span data-ttu-id="a98de-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a98de-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="a98de-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a98de-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="a98de-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a98de-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a98de-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a98de-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a98de-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a98de-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a98de-145">IID</span><span class="sxs-lookup"><span data-stu-id="a98de-145">IID</span></span><br/>                      | <span data-ttu-id="a98de-146">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a98de-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a98de-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a98de-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a98de-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a98de-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a98de-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a98de-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a98de-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a98de-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a98de-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a98de-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a98de-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a98de-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a98de-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a98de-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a98de-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a98de-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a98de-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a98de-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





