---
title: Proprietà BitmapPersistence di IMsRdpClientAdvancedSettings
description: Specifica se utilizzare la memorizzazione nella cache permanente della bitmap. La memorizzazione nella cache persistente può migliorare le prestazioni, ma richiede ulteriore spazio su disco.
ms.assetid: ffaa9277-9dd7-4b2a-9de5-009b7e8766bc
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BitmapPersistence
- Servizi Desktop remoto proprietà BitmapPersistence, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà BitmapPersistence
- Servizi Desktop remoto proprietà BitmapPersistence, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà BitmapPersistence
- Servizi Desktop remoto proprietà BitmapPersistence, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà BitmapPersistence
- Servizi Desktop remoto proprietà BitmapPersistence, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà BitmapPersistence
- Servizi Desktop remoto proprietà BitmapPersistence, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà BitmapPersistence
- Servizi Desktop remoto proprietà BitmapPersistence, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà BitmapPersistence
- Servizi Desktop remoto proprietà BitmapPersistence, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà BitmapPersistence
- Servizi Desktop remoto proprietà BitmapPersistence, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà BitmapPersistence
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapPersistence
- IMsRdpClientAdvancedSettings.get_BitmapPersistence
- IMsRdpClientAdvancedSettings.put_BitmapPersistence
- IMsRdpClientAdvancedSettings2.BitmapPersistence
- IMsRdpClientAdvancedSettings2.get_BitmapPersistence
- IMsRdpClientAdvancedSettings2.put_BitmapPersistence
- IMsRdpClientAdvancedSettings3.BitmapPersistence
- IMsRdpClientAdvancedSettings3.get_BitmapPersistence
- IMsRdpClientAdvancedSettings3.put_BitmapPersistence
- IMsRdpClientAdvancedSettings4.BitmapPersistence
- IMsRdpClientAdvancedSettings4.get_BitmapPersistence
- IMsRdpClientAdvancedSettings4.put_BitmapPersistence
- IMsRdpClientAdvancedSettings5.BitmapPersistence
- IMsRdpClientAdvancedSettings5.get_BitmapPersistence
- IMsRdpClientAdvancedSettings5.put_BitmapPersistence
- IMsRdpClientAdvancedSettings6.BitmapPersistence
- IMsRdpClientAdvancedSettings6.get_BitmapPersistence
- IMsRdpClientAdvancedSettings6.put_BitmapPersistence
- IMsRdpClientAdvancedSettings7.BitmapPersistence
- IMsRdpClientAdvancedSettings7.get_BitmapPersistence
- IMsRdpClientAdvancedSettings7.put_BitmapPersistence
- IMsRdpClientAdvancedSettings8.BitmapPersistence
- IMsRdpClientAdvancedSettings8.get_BitmapPersistence
- IMsRdpClientAdvancedSettings8.put_BitmapPersistence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65795b5217c785befe0db6ac529d5760a6211d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400456"
---
# <a name="imsrdpclientadvancedsettingsbitmappersistence-property"></a><span data-ttu-id="ee9f0-121">Proprietà IMsRdpClientAdvancedSettings:: BitmapPersistence</span><span class="sxs-lookup"><span data-stu-id="ee9f0-121">IMsRdpClientAdvancedSettings::BitmapPersistence property</span></span>

<span data-ttu-id="ee9f0-122">Specifica se utilizzare la memorizzazione nella cache permanente della bitmap.</span><span class="sxs-lookup"><span data-stu-id="ee9f0-122">Specifies if persistent bitmap caching should be used.</span></span> <span data-ttu-id="ee9f0-123">La memorizzazione nella cache persistente può migliorare le prestazioni, ma richiede ulteriore spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="ee9f0-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="ee9f0-124">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ee9f0-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee9f0-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee9f0-125">Syntax</span></span>


```C++
HRESULT put_BitmapPersistence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPersistence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="ee9f0-126">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ee9f0-126">Property value</span></span>

<span data-ttu-id="ee9f0-127">Impostare questo parametro su 0 per disabilitare la memorizzazione nella cache o un valore diverso da zero per abilitare la memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="ee9f0-127">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

> [!Note]  
> <span data-ttu-id="ee9f0-128">L'errore di ortografia nel nome del parametro si trova nella versione rilasciata del controllo.</span><span class="sxs-lookup"><span data-stu-id="ee9f0-128">The spelling error in the name of the parameter is in the released version of the control.</span></span>

 

## <a name="error-codes"></a><span data-ttu-id="ee9f0-129">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ee9f0-129">Error codes</span></span>

<span data-ttu-id="ee9f0-130">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ee9f0-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee9f0-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee9f0-131">Remarks</span></span>

<span data-ttu-id="ee9f0-132">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ee9f0-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee9f0-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee9f0-133">Requirements</span></span>



| <span data-ttu-id="ee9f0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee9f0-134">Requirement</span></span> | <span data-ttu-id="ee9f0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ee9f0-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee9f0-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee9f0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ee9f0-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee9f0-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ee9f0-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee9f0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ee9f0-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee9f0-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ee9f0-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ee9f0-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="ee9f0-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee9f0-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ee9f0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ee9f0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee9f0-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee9f0-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ee9f0-144">IID</span><span class="sxs-lookup"><span data-stu-id="ee9f0-144">IID</span></span><br/>                      | <span data-ttu-id="ee9f0-145">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ee9f0-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee9f0-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee9f0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee9f0-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ee9f0-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ee9f0-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ee9f0-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ee9f0-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ee9f0-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ee9f0-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ee9f0-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ee9f0-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ee9f0-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ee9f0-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ee9f0-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ee9f0-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ee9f0-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ee9f0-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ee9f0-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





