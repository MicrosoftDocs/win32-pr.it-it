---
title: Proprietà BitmapPeristence di IMsTscAdvancedSettings
description: Specifica se la memorizzazione nella cache bitmap è abilitata.
ms.assetid: 8cabeae8-26bc-4d33-82cc-47bb201d79b6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà BitmapPeristence
- Servizi Desktop remoto proprietà BitmapPeristence, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà BitmapPeristence
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.BitmapPeristence
- IMsTscAdvancedSettings.get_BitmapPeristence
- IMsTscAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings.BitmapPeristence
- IMsRdpClientAdvancedSettings.get_BitmapPeristence
- IMsRdpClientAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings2.BitmapPeristence
- IMsRdpClientAdvancedSettings2.get_BitmapPeristence
- IMsRdpClientAdvancedSettings2.put_BitmapPeristence
- IMsRdpClientAdvancedSettings3.BitmapPeristence
- IMsRdpClientAdvancedSettings3.get_BitmapPeristence
- IMsRdpClientAdvancedSettings3.put_BitmapPeristence
- IMsRdpClientAdvancedSettings4.BitmapPeristence
- IMsRdpClientAdvancedSettings4.get_BitmapPeristence
- IMsRdpClientAdvancedSettings4.put_BitmapPeristence
- IMsRdpClientAdvancedSettings5.BitmapPeristence
- IMsRdpClientAdvancedSettings5.get_BitmapPeristence
- IMsRdpClientAdvancedSettings5.put_BitmapPeristence
- IMsRdpClientAdvancedSettings6.BitmapPeristence
- IMsRdpClientAdvancedSettings6.get_BitmapPeristence
- IMsRdpClientAdvancedSettings6.put_BitmapPeristence
- IMsRdpClientAdvancedSettings7.BitmapPeristence
- IMsRdpClientAdvancedSettings7.get_BitmapPeristence
- IMsRdpClientAdvancedSettings7.put_BitmapPeristence
- IMsRdpClientAdvancedSettings8.BitmapPeristence
- IMsRdpClientAdvancedSettings8.get_BitmapPeristence
- IMsRdpClientAdvancedSettings8.put_BitmapPeristence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a543d24b200d8fa484939d5ffeabfeeac0b5f73f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479031"
---
# <a name="imstscadvancedsettingsbitmapperistence-property"></a><span data-ttu-id="f90a4-122">Proprietà IMsTscAdvancedSettings:: BitmapPeristence</span><span class="sxs-lookup"><span data-stu-id="f90a4-122">IMsTscAdvancedSettings::BitmapPeristence property</span></span>

<span data-ttu-id="f90a4-123">Specifica se la memorizzazione nella cache bitmap è abilitata.</span><span class="sxs-lookup"><span data-stu-id="f90a4-123">Specifies whether bitmap caching is enabled.</span></span> <span data-ttu-id="f90a4-124">La memorizzazione nella cache persistente può migliorare le prestazioni, ma richiede ulteriore spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="f90a4-124">Persistent caching can improve performance but requires additional disk space.</span></span>

> [!Note]  
> <span data-ttu-id="f90a4-125">L'errore di ortografia nel nome della proprietà e il relativo parametro si trova nella versione rilasciata del controllo.</span><span class="sxs-lookup"><span data-stu-id="f90a4-125">The spelling error in the name of the property and its parameter is in the released version of the control.</span></span>

 

<span data-ttu-id="f90a4-126">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f90a4-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f90a4-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f90a4-127">Syntax</span></span>


```C++
HRESULT put_BitmapPeristence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPeristence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="f90a4-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f90a4-128">Property value</span></span>

<span data-ttu-id="f90a4-129">Impostare questo parametro su 0 per disabilitare la memorizzazione nella cache o un valore diverso da zero per abilitare la memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="f90a4-129">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f90a4-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f90a4-130">Error codes</span></span>

<span data-ttu-id="f90a4-131">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f90a4-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f90a4-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="f90a4-132">Remarks</span></span>

<span data-ttu-id="f90a4-133">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f90a4-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f90a4-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f90a4-134">Requirements</span></span>



| <span data-ttu-id="f90a4-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f90a4-135">Requirement</span></span> | <span data-ttu-id="f90a4-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f90a4-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f90a4-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f90a4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f90a4-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f90a4-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="f90a4-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f90a4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f90a4-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f90a4-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f90a4-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f90a4-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="f90a4-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f90a4-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="f90a4-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f90a4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f90a4-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f90a4-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="f90a4-145">IID</span><span class="sxs-lookup"><span data-stu-id="f90a4-145">IID</span></span><br/>                      | <span data-ttu-id="f90a4-146">IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="f90a4-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f90a4-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f90a4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f90a4-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f90a4-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f90a4-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f90a4-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f90a4-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f90a4-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="f90a4-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f90a4-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f90a4-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f90a4-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f90a4-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f90a4-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f90a4-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f90a4-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f90a4-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f90a4-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f90a4-156">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f90a4-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





