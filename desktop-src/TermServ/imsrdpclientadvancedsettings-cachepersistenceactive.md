---
title: Proprietà CachePersistenceActive di IMsRdpClientAdvancedSettings
description: Specifica se utilizzare la memorizzazione nella cache persistente della bitmap. La memorizzazione nella cache persistente può migliorare le prestazioni, ma richiede ulteriore spazio su disco.
ms.assetid: 5eb986c4-98dd-426f-8d55-d3a9a526e1b2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà CachePersistenceActive
- Servizi Desktop remoto proprietà CachePersistenceActive, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà CachePersistenceActive
- Servizi Desktop remoto proprietà CachePersistenceActive, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà CachePersistenceActive
- Servizi Desktop remoto proprietà CachePersistenceActive, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà CachePersistenceActive
- Servizi Desktop remoto proprietà CachePersistenceActive, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà CachePersistenceActive
- Servizi Desktop remoto proprietà CachePersistenceActive, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà CachePersistenceActive
- Servizi Desktop remoto proprietà CachePersistenceActive, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà CachePersistenceActive
- Servizi Desktop remoto proprietà CachePersistenceActive, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà CachePersistenceActive
- Servizi Desktop remoto proprietà CachePersistenceActive, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà CachePersistenceActive
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.CachePersistenceActive
- IMsRdpClientAdvancedSettings.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.CachePersistenceActive
- IMsRdpClientAdvancedSettings2.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.CachePersistenceActive
- IMsRdpClientAdvancedSettings3.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.CachePersistenceActive
- IMsRdpClientAdvancedSettings4.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.CachePersistenceActive
- IMsRdpClientAdvancedSettings5.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.CachePersistenceActive
- IMsRdpClientAdvancedSettings6.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.CachePersistenceActive
- IMsRdpClientAdvancedSettings7.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.CachePersistenceActive
- IMsRdpClientAdvancedSettings8.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.put_CachePersistenceActive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb34e90cc028e95c750a444d53f42c9c0ab77400
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302617"
---
# <a name="imsrdpclientadvancedsettingscachepersistenceactive-property"></a><span data-ttu-id="d462f-121">Proprietà IMsRdpClientAdvancedSettings:: CachePersistenceActive</span><span class="sxs-lookup"><span data-stu-id="d462f-121">IMsRdpClientAdvancedSettings::CachePersistenceActive property</span></span>

<span data-ttu-id="d462f-122">Specifica se utilizzare la memorizzazione nella cache persistente della bitmap.</span><span class="sxs-lookup"><span data-stu-id="d462f-122">Specifies whether persistent bitmap caching should be used.</span></span> <span data-ttu-id="d462f-123">La memorizzazione nella cache persistente può migliorare le prestazioni, ma richiede ulteriore spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="d462f-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="d462f-124">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d462f-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d462f-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d462f-125">Syntax</span></span>


```C++
HRESULT put_CachePersistenceActive(
  [in]  LONG cachePersistenceActive
);

HRESULT get_CachePersistenceActive(
  [out] LONG *pcachePersistenceActive
);
```



## <a name="property-value"></a><span data-ttu-id="d462f-126">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d462f-126">Property value</span></span>

<span data-ttu-id="d462f-127">Impostare questo parametro su 0 per disabilitare la funzionalità o un valore diverso da zero per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d462f-127">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d462f-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d462f-128">Error codes</span></span>

<span data-ttu-id="d462f-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d462f-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d462f-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="d462f-130">Remarks</span></span>

<span data-ttu-id="d462f-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d462f-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d462f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d462f-132">Requirements</span></span>



| <span data-ttu-id="d462f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d462f-133">Requirement</span></span> | <span data-ttu-id="d462f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="d462f-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d462f-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d462f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d462f-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d462f-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d462f-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d462f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d462f-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d462f-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d462f-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d462f-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="d462f-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d462f-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d462f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d462f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d462f-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d462f-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d462f-143">IID</span><span class="sxs-lookup"><span data-stu-id="d462f-143">IID</span></span><br/>                      | <span data-ttu-id="d462f-144">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="d462f-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d462f-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d462f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d462f-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d462f-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d462f-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d462f-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d462f-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d462f-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d462f-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d462f-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d462f-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d462f-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d462f-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d462f-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d462f-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d462f-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d462f-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="d462f-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





