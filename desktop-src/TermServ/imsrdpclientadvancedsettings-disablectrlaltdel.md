---
title: Proprietà DisableCtrlAltDel di IMsRdpClientAdvancedSettings
description: Specifica se la schermata iniziale esplicativa in Winlogon dovrebbe essere visualizzata.
ms.assetid: 79212472-105f-4e92-8065-f97819637d02
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DisableCtrlAltDel
- Servizi Desktop remoto proprietà DisableCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà DisableCtrlAltDel
- Servizi Desktop remoto proprietà DisableCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà DisableCtrlAltDel
- Servizi Desktop remoto proprietà DisableCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà DisableCtrlAltDel
- Servizi Desktop remoto proprietà DisableCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà DisableCtrlAltDel
- Servizi Desktop remoto proprietà DisableCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà DisableCtrlAltDel
- Servizi Desktop remoto proprietà DisableCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà DisableCtrlAltDel
- Servizi Desktop remoto proprietà DisableCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà DisableCtrlAltDel
- Servizi Desktop remoto proprietà DisableCtrlAltDel, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà DisableCtrlAltDel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_DisableCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3380aa78c16c7e937637cc727fe81f054649f929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740559"
---
# <a name="imsrdpclientadvancedsettingsdisablectrlaltdel-property"></a><span data-ttu-id="c0b82-120">IMsRdpClientAdvancedSettings::D Proprietà isableCtrlAltDel</span><span class="sxs-lookup"><span data-stu-id="c0b82-120">IMsRdpClientAdvancedSettings::DisableCtrlAltDel property</span></span>

<span data-ttu-id="c0b82-121">Specifica se la schermata iniziale esplicativa in Winlogon dovrebbe essere visualizzata.</span><span class="sxs-lookup"><span data-stu-id="c0b82-121">Specifies if the initial explanatory screen in Winlogon should display.</span></span>

<span data-ttu-id="c0b82-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c0b82-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b82-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0b82-123">Syntax</span></span>


```C++
HRESULT put_DisableCtrlAltDel(
  [in]  LONG disableCtrlAltDel
);

HRESULT get_DisableCtrlAltDel(
  [out] LONG *pdisableCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="c0b82-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c0b82-124">Property value</span></span>

<span data-ttu-id="c0b82-125">Impostare questo parametro su 0 per disabilitare la funzionalità o un valore diverso da zero per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c0b82-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0b82-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c0b82-126">Error codes</span></span>

<span data-ttu-id="c0b82-127">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c0b82-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0b82-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0b82-128">Remarks</span></span>

<span data-ttu-id="c0b82-129">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c0b82-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b82-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0b82-130">Requirements</span></span>



| <span data-ttu-id="c0b82-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0b82-131">Requirement</span></span> | <span data-ttu-id="c0b82-132">Valore</span><span class="sxs-lookup"><span data-stu-id="c0b82-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b82-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0b82-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b82-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0b82-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="c0b82-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0b82-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b82-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0b82-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="c0b82-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c0b82-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0b82-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0b82-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c0b82-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c0b82-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0b82-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0b82-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c0b82-141">IID</span><span class="sxs-lookup"><span data-stu-id="c0b82-141">IID</span></span><br/>                      | <span data-ttu-id="c0b82-142">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="c0b82-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0b82-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0b82-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b82-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c0b82-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c0b82-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c0b82-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c0b82-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c0b82-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c0b82-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c0b82-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c0b82-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c0b82-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c0b82-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c0b82-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c0b82-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c0b82-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c0b82-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c0b82-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





