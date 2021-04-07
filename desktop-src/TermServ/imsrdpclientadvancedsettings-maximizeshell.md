---
title: Proprietà MaximizeShell di IMsRdpClientAdvancedSettings
description: Specifica se è necessario ingrandire i programmi avviati con la proprietà StartProgram.
ms.assetid: d8c194b6-04ef-495f-a763-7e18064230e6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà MaximizeShell
- Servizi Desktop remoto proprietà MaximizeShell, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà MaximizeShell
- Servizi Desktop remoto proprietà MaximizeShell, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà MaximizeShell
- Servizi Desktop remoto proprietà MaximizeShell, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà MaximizeShell
- Servizi Desktop remoto proprietà MaximizeShell, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà MaximizeShell
- Servizi Desktop remoto proprietà MaximizeShell, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà MaximizeShell
- Servizi Desktop remoto proprietà MaximizeShell, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà MaximizeShell
- Servizi Desktop remoto proprietà MaximizeShell, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà MaximizeShell
- Servizi Desktop remoto proprietà MaximizeShell, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà MaximizeShell
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MaximizeShell
- IMsRdpClientAdvancedSettings.get_MaximizeShell
- IMsRdpClientAdvancedSettings.put_MaximizeShell
- IMsRdpClientAdvancedSettings2.MaximizeShell
- IMsRdpClientAdvancedSettings2.get_MaximizeShell
- IMsRdpClientAdvancedSettings2.put_MaximizeShell
- IMsRdpClientAdvancedSettings3.MaximizeShell
- IMsRdpClientAdvancedSettings3.get_MaximizeShell
- IMsRdpClientAdvancedSettings3.put_MaximizeShell
- IMsRdpClientAdvancedSettings4.MaximizeShell
- IMsRdpClientAdvancedSettings4.get_MaximizeShell
- IMsRdpClientAdvancedSettings4.put_MaximizeShell
- IMsRdpClientAdvancedSettings5.MaximizeShell
- IMsRdpClientAdvancedSettings5.get_MaximizeShell
- IMsRdpClientAdvancedSettings5.put_MaximizeShell
- IMsRdpClientAdvancedSettings6.MaximizeShell
- IMsRdpClientAdvancedSettings6.get_MaximizeShell
- IMsRdpClientAdvancedSettings6.put_MaximizeShell
- IMsRdpClientAdvancedSettings7.MaximizeShell
- IMsRdpClientAdvancedSettings7.get_MaximizeShell
- IMsRdpClientAdvancedSettings7.put_MaximizeShell
- IMsRdpClientAdvancedSettings8.MaximizeShell
- IMsRdpClientAdvancedSettings8.get_MaximizeShell
- IMsRdpClientAdvancedSettings8.put_MaximizeShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c172dd71fcf57f2028f6ba64c93ceaeec2ffb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963973"
---
# <a name="imsrdpclientadvancedsettingsmaximizeshell-property"></a><span data-ttu-id="ba9db-120">Proprietà IMsRdpClientAdvancedSettings:: MaximizeShell</span><span class="sxs-lookup"><span data-stu-id="ba9db-120">IMsRdpClientAdvancedSettings::MaximizeShell property</span></span>

<span data-ttu-id="ba9db-121">Specifica se è necessario ingrandire i programmi avviati con la proprietà [**StartProgram**](imstscsecuredsettings-startprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="ba9db-121">Specifies if programs launched with the [**StartProgram**](imstscsecuredsettings-startprogram.md) property should be maximized.</span></span>

<span data-ttu-id="ba9db-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ba9db-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba9db-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba9db-123">Syntax</span></span>


```C++
HRESULT put_MaximizeShell(
  [in]  LONG maximizeShell
);

HRESULT get_MaximizeShell(
  [out] LONG *pmaximizeShell
);
```



## <a name="property-value"></a><span data-ttu-id="ba9db-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ba9db-124">Property value</span></span>

<span data-ttu-id="ba9db-125">Impostare questo parametro su 0 per disabilitare la funzionalità o un valore diverso da zero per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ba9db-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba9db-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ba9db-126">Error codes</span></span>

<span data-ttu-id="ba9db-127">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ba9db-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba9db-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba9db-128">Remarks</span></span>

<span data-ttu-id="ba9db-129">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ba9db-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba9db-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba9db-130">Requirements</span></span>



| <span data-ttu-id="ba9db-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba9db-131">Requirement</span></span> | <span data-ttu-id="ba9db-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ba9db-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9db-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba9db-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ba9db-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba9db-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ba9db-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba9db-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ba9db-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba9db-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ba9db-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ba9db-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="ba9db-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba9db-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ba9db-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ba9db-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba9db-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba9db-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ba9db-141">IID</span><span class="sxs-lookup"><span data-stu-id="ba9db-141">IID</span></span><br/>                      | <span data-ttu-id="ba9db-142">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ba9db-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba9db-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba9db-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba9db-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ba9db-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ba9db-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ba9db-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ba9db-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ba9db-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ba9db-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ba9db-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ba9db-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ba9db-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ba9db-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ba9db-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ba9db-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ba9db-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ba9db-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ba9db-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





