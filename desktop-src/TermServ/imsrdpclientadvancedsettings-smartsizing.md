---
title: Proprietà SmartSizing di IMsRdpClientAdvancedSettings
description: Specifica se la visualizzazione deve essere ridimensionata per adattarsi all'area client del controllo. Si noti che le barre di scorrimento non vengono visualizzate quando la proprietà SmartSizing è abilitata.
ms.assetid: d0b93129-5f84-49c5-bf8c-048075ac1481
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SmartSizing
- Servizi Desktop remoto proprietà SmartSizing, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà SmartSizing
- Servizi Desktop remoto proprietà SmartSizing, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà SmartSizing
- Servizi Desktop remoto proprietà SmartSizing, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà SmartSizing
- Servizi Desktop remoto proprietà SmartSizing, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà SmartSizing
- Servizi Desktop remoto proprietà SmartSizing, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà SmartSizing
- Servizi Desktop remoto proprietà SmartSizing, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà SmartSizing
- Servizi Desktop remoto proprietà SmartSizing, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà SmartSizing
- Servizi Desktop remoto proprietà SmartSizing, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà SmartSizing
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmartSizing
- IMsRdpClientAdvancedSettings.get_SmartSizing
- IMsRdpClientAdvancedSettings.put_SmartSizing
- IMsRdpClientAdvancedSettings2.SmartSizing
- IMsRdpClientAdvancedSettings2.get_SmartSizing
- IMsRdpClientAdvancedSettings2.put_SmartSizing
- IMsRdpClientAdvancedSettings3.SmartSizing
- IMsRdpClientAdvancedSettings3.get_SmartSizing
- IMsRdpClientAdvancedSettings3.put_SmartSizing
- IMsRdpClientAdvancedSettings4.SmartSizing
- IMsRdpClientAdvancedSettings4.get_SmartSizing
- IMsRdpClientAdvancedSettings4.put_SmartSizing
- IMsRdpClientAdvancedSettings5.SmartSizing
- IMsRdpClientAdvancedSettings5.get_SmartSizing
- IMsRdpClientAdvancedSettings5.put_SmartSizing
- IMsRdpClientAdvancedSettings6.SmartSizing
- IMsRdpClientAdvancedSettings6.get_SmartSizing
- IMsRdpClientAdvancedSettings6.put_SmartSizing
- IMsRdpClientAdvancedSettings7.SmartSizing
- IMsRdpClientAdvancedSettings7.get_SmartSizing
- IMsRdpClientAdvancedSettings7.put_SmartSizing
- IMsRdpClientAdvancedSettings8.SmartSizing
- IMsRdpClientAdvancedSettings8.get_SmartSizing
- IMsRdpClientAdvancedSettings8.put_SmartSizing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec2a825725e01d876b9e8658f215de6595f32f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400240"
---
# <a name="imsrdpclientadvancedsettingssmartsizing-property"></a><span data-ttu-id="32801-121">Proprietà IMsRdpClientAdvancedSettings:: SmartSizing</span><span class="sxs-lookup"><span data-stu-id="32801-121">IMsRdpClientAdvancedSettings::SmartSizing property</span></span>

<span data-ttu-id="32801-122">Specifica se la visualizzazione deve essere ridimensionata per adattarsi all'area client del controllo.</span><span class="sxs-lookup"><span data-stu-id="32801-122">Specifies if the display should be scaled to fit the client area of the control.</span></span> <span data-ttu-id="32801-123">Si noti che le barre di scorrimento non vengono visualizzate quando la proprietà **SmartSizing** è abilitata.</span><span class="sxs-lookup"><span data-stu-id="32801-123">Note that scroll bars do not appear when the **SmartSizing** property is enabled.</span></span>

<span data-ttu-id="32801-124">A differenza della maggior parte delle altre proprietà, questa proprietà può essere impostata quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="32801-124">Unlike most other properties, this property can be set when the control is connected.</span></span>

<span data-ttu-id="32801-125">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="32801-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="32801-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32801-126">Syntax</span></span>


```C++
HRESULT put_SmartSizing(
  [in]  VARIANT_BOOL fSmartSizing
);

HRESULT get_SmartSizing(
  [out] VARIANT_BOOL *pfSmartSizing
);
```



## <a name="property-value"></a><span data-ttu-id="32801-127">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="32801-127">Property value</span></span>

<span data-ttu-id="32801-128">Impostare questo parametro su **Variant \_ false** per disabilitare la funzionalità o la **variante \_ true** per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="32801-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="32801-129">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="32801-129">Error codes</span></span>

<span data-ttu-id="32801-130">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="32801-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="32801-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="32801-131">Remarks</span></span>

<span data-ttu-id="32801-132">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="32801-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32801-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32801-133">Requirements</span></span>



| <span data-ttu-id="32801-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="32801-134">Requirement</span></span> | <span data-ttu-id="32801-135">Valore</span><span class="sxs-lookup"><span data-stu-id="32801-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32801-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32801-136">Minimum supported client</span></span><br/> | <span data-ttu-id="32801-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32801-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="32801-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32801-138">Minimum supported server</span></span><br/> | <span data-ttu-id="32801-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32801-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="32801-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="32801-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="32801-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32801-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="32801-142">DLL</span><span class="sxs-lookup"><span data-stu-id="32801-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32801-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32801-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="32801-144">IID</span><span class="sxs-lookup"><span data-stu-id="32801-144">IID</span></span><br/>                      | <span data-ttu-id="32801-145">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="32801-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32801-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32801-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32801-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="32801-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="32801-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="32801-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="32801-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="32801-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="32801-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="32801-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="32801-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="32801-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="32801-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="32801-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="32801-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="32801-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="32801-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="32801-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





