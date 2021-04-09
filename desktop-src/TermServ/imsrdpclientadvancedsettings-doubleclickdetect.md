---
title: Proprietà DoubleClickDetect di IMsRdpClientAdvancedSettings
description: Specifica se il client identifica i doppio clic per il server.
ms.assetid: 39e76bef-3d12-406d-a074-8c084fbe9ccc
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DoubleClickDetect
- Servizi Desktop remoto proprietà DoubleClickDetect, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà DoubleClickDetect
- Servizi Desktop remoto proprietà DoubleClickDetect, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà DoubleClickDetect
- Servizi Desktop remoto proprietà DoubleClickDetect, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà DoubleClickDetect
- Servizi Desktop remoto proprietà DoubleClickDetect, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà DoubleClickDetect
- Servizi Desktop remoto proprietà DoubleClickDetect, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà DoubleClickDetect
- Servizi Desktop remoto proprietà DoubleClickDetect, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà DoubleClickDetect
- Servizi Desktop remoto proprietà DoubleClickDetect, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà DoubleClickDetect
- Servizi Desktop remoto proprietà DoubleClickDetect, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà DoubleClickDetect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DoubleClickDetect
- IMsRdpClientAdvancedSettings.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.DoubleClickDetect
- IMsRdpClientAdvancedSettings2.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.DoubleClickDetect
- IMsRdpClientAdvancedSettings3.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.DoubleClickDetect
- IMsRdpClientAdvancedSettings4.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.DoubleClickDetect
- IMsRdpClientAdvancedSettings5.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.DoubleClickDetect
- IMsRdpClientAdvancedSettings6.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.DoubleClickDetect
- IMsRdpClientAdvancedSettings7.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.DoubleClickDetect
- IMsRdpClientAdvancedSettings8.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.put_DoubleClickDetect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd771614a80d909e0e7a748ab7256a5310084deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121230"
---
# <a name="imsrdpclientadvancedsettingsdoubleclickdetect-property"></a><span data-ttu-id="816a6-120">IMsRdpClientAdvancedSettings::D Proprietà oubleClickDetect</span><span class="sxs-lookup"><span data-stu-id="816a6-120">IMsRdpClientAdvancedSettings::DoubleClickDetect property</span></span>

<span data-ttu-id="816a6-121">Specifica se il client identifica i doppio clic per il server.</span><span class="sxs-lookup"><span data-stu-id="816a6-121">Specifies if the client identifies double-clicks for the server.</span></span>

<span data-ttu-id="816a6-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="816a6-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="816a6-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="816a6-123">Syntax</span></span>


```C++
HRESULT put_DoubleClickDetect(
  [in]  LONG doubleClickDetect
);

HRESULT get_DoubleClickDetect(
  [out] LONG *pdoubleClickDetect
);
```



## <a name="property-value"></a><span data-ttu-id="816a6-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="816a6-124">Property value</span></span>

<span data-ttu-id="816a6-125">Impostare questo parametro su 0 per disabilitare la funzionalità o un valore diverso da zero per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="816a6-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="816a6-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="816a6-126">Error codes</span></span>

<span data-ttu-id="816a6-127">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="816a6-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="816a6-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="816a6-128">Remarks</span></span>

<span data-ttu-id="816a6-129">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="816a6-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="816a6-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="816a6-130">Requirements</span></span>



| <span data-ttu-id="816a6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="816a6-131">Requirement</span></span> | <span data-ttu-id="816a6-132">Valore</span><span class="sxs-lookup"><span data-stu-id="816a6-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="816a6-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="816a6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="816a6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="816a6-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="816a6-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="816a6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="816a6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="816a6-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="816a6-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="816a6-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="816a6-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="816a6-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="816a6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="816a6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="816a6-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="816a6-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="816a6-141">IID</span><span class="sxs-lookup"><span data-stu-id="816a6-141">IID</span></span><br/>                      | <span data-ttu-id="816a6-142">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="816a6-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="816a6-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="816a6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="816a6-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="816a6-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="816a6-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="816a6-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="816a6-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="816a6-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="816a6-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="816a6-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="816a6-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="816a6-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="816a6-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="816a6-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="816a6-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="816a6-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="816a6-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="816a6-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





