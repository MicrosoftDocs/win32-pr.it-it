---
title: Proprietà NumBitmapCaches di IMsRdpClientAdvancedSettings
description: Questa proprietà non è supportata. | Proprietà NumBitmapCaches di IMsRdpClientAdvancedSettings
ms.assetid: a413b2c0-7661-415d-bc38-e8fd55006e8c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà NumBitmapCaches
- Servizi Desktop remoto proprietà NumBitmapCaches, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà NumBitmapCaches
- Servizi Desktop remoto proprietà NumBitmapCaches, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà NumBitmapCaches
- Servizi Desktop remoto proprietà NumBitmapCaches, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà NumBitmapCaches
- Servizi Desktop remoto proprietà NumBitmapCaches, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà NumBitmapCaches
- Servizi Desktop remoto proprietà NumBitmapCaches, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà NumBitmapCaches
- Servizi Desktop remoto proprietà NumBitmapCaches, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà NumBitmapCaches
- Servizi Desktop remoto proprietà NumBitmapCaches, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà NumBitmapCaches
- Servizi Desktop remoto proprietà NumBitmapCaches, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà NumBitmapCaches
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.NumBitmapCaches
- IMsRdpClientAdvancedSettings.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.NumBitmapCaches
- IMsRdpClientAdvancedSettings2.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.NumBitmapCaches
- IMsRdpClientAdvancedSettings3.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.NumBitmapCaches
- IMsRdpClientAdvancedSettings4.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.NumBitmapCaches
- IMsRdpClientAdvancedSettings5.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.NumBitmapCaches
- IMsRdpClientAdvancedSettings6.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.NumBitmapCaches
- IMsRdpClientAdvancedSettings7.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.NumBitmapCaches
- IMsRdpClientAdvancedSettings8.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.put_NumBitmapCaches
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae60423287da041e3f84b28d8d51388e9a4050b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321635"
---
# <a name="imsrdpclientadvancedsettingsnumbitmapcaches-property"></a><span data-ttu-id="78b06-121">Proprietà IMsRdpClientAdvancedSettings:: NumBitmapCaches</span><span class="sxs-lookup"><span data-stu-id="78b06-121">IMsRdpClientAdvancedSettings::NumBitmapCaches property</span></span>

<span data-ttu-id="78b06-122">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="78b06-122">This property is not supported.</span></span>

<span data-ttu-id="78b06-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="78b06-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="78b06-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78b06-124">Syntax</span></span>


```C++
HRESULT put_NumBitmapCaches(
  [in]  LONG numBitmapCaches
);

HRESULT get_NumBitmapCaches(
  [out] LONG *pnumBitmapCaches
);
```



## <a name="property-value"></a><span data-ttu-id="78b06-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="78b06-125">Property value</span></span>

<span data-ttu-id="78b06-126">Nuovo numero di cache.</span><span class="sxs-lookup"><span data-stu-id="78b06-126">The new number of caches.</span></span> <span data-ttu-id="78b06-127">Il valore predefinito è 3, che consente di ottenere prestazioni ottimali.</span><span class="sxs-lookup"><span data-stu-id="78b06-127">The default value is 3, which results in the best performance.</span></span>

## <a name="error-codes"></a><span data-ttu-id="78b06-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="78b06-128">Error codes</span></span>

<span data-ttu-id="78b06-129">Restituisce un valore **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="78b06-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="78b06-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="78b06-130">Remarks</span></span>

<span data-ttu-id="78b06-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="78b06-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78b06-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78b06-132">Requirements</span></span>



| <span data-ttu-id="78b06-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="78b06-133">Requirement</span></span> | <span data-ttu-id="78b06-134">Valore</span><span class="sxs-lookup"><span data-stu-id="78b06-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78b06-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78b06-135">Minimum supported client</span></span><br/> | <span data-ttu-id="78b06-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="78b06-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="78b06-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78b06-137">Minimum supported server</span></span><br/> | <span data-ttu-id="78b06-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="78b06-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="78b06-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="78b06-139">End of client support</span></span><br/>    | <span data-ttu-id="78b06-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="78b06-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="78b06-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="78b06-141">End of server support</span></span><br/>    | <span data-ttu-id="78b06-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="78b06-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="78b06-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="78b06-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="78b06-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78b06-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="78b06-145">DLL</span><span class="sxs-lookup"><span data-stu-id="78b06-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78b06-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78b06-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="78b06-147">IID</span><span class="sxs-lookup"><span data-stu-id="78b06-147">IID</span></span><br/>                      | <span data-ttu-id="78b06-148">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="78b06-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78b06-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78b06-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78b06-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="78b06-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="78b06-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="78b06-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="78b06-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="78b06-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="78b06-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="78b06-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="78b06-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="78b06-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="78b06-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="78b06-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="78b06-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="78b06-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="78b06-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="78b06-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





