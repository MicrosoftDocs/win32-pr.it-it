---
title: Proprietà minInputSendInterval di IMsRdpClientAdvancedSettings
description: Specifica l'intervallo minimo, in millisecondi, tra l'invio degli eventi del mouse.
ms.assetid: d186c05f-0b45-47bd-8a8e-e1f9baf2bd75
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà minInputSendInterval
- Servizi Desktop remoto proprietà minInputSendInterval, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà minInputSendInterval
- Servizi Desktop remoto proprietà minInputSendInterval, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà minInputSendInterval
- Servizi Desktop remoto proprietà minInputSendInterval, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà minInputSendInterval
- Servizi Desktop remoto proprietà minInputSendInterval, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà minInputSendInterval
- Servizi Desktop remoto proprietà minInputSendInterval, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà minInputSendInterval
- Servizi Desktop remoto proprietà minInputSendInterval, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà minInputSendInterval
- Servizi Desktop remoto proprietà minInputSendInterval, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà minInputSendInterval
- Servizi Desktop remoto proprietà minInputSendInterval, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà minInputSendInterval
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.minInputSendInterval
- IMsRdpClientAdvancedSettings.get_minInputSendInterval
- IMsRdpClientAdvancedSettings.put_minInputSendInterval
- IMsRdpClientAdvancedSettings2.minInputSendInterval
- IMsRdpClientAdvancedSettings2.get_minInputSendInterval
- IMsRdpClientAdvancedSettings2.put_minInputSendInterval
- IMsRdpClientAdvancedSettings3.minInputSendInterval
- IMsRdpClientAdvancedSettings3.get_minInputSendInterval
- IMsRdpClientAdvancedSettings3.put_minInputSendInterval
- IMsRdpClientAdvancedSettings4.minInputSendInterval
- IMsRdpClientAdvancedSettings4.get_minInputSendInterval
- IMsRdpClientAdvancedSettings4.put_minInputSendInterval
- IMsRdpClientAdvancedSettings5.minInputSendInterval
- IMsRdpClientAdvancedSettings5.get_minInputSendInterval
- IMsRdpClientAdvancedSettings5.put_minInputSendInterval
- IMsRdpClientAdvancedSettings6.minInputSendInterval
- IMsRdpClientAdvancedSettings6.get_minInputSendInterval
- IMsRdpClientAdvancedSettings6.put_minInputSendInterval
- IMsRdpClientAdvancedSettings7.minInputSendInterval
- IMsRdpClientAdvancedSettings7.get_minInputSendInterval
- IMsRdpClientAdvancedSettings7.put_minInputSendInterval
- IMsRdpClientAdvancedSettings8.minInputSendInterval
- IMsRdpClientAdvancedSettings8.get_minInputSendInterval
- IMsRdpClientAdvancedSettings8.put_minInputSendInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56070e2ba395c4b89dc9caa9e6e5181bb03d81ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400448"
---
# <a name="imsrdpclientadvancedsettingsmininputsendinterval-property"></a><span data-ttu-id="4d6fd-120">Proprietà IMsRdpClientAdvancedSettings:: minInputSendInterval</span><span class="sxs-lookup"><span data-stu-id="4d6fd-120">IMsRdpClientAdvancedSettings::minInputSendInterval property</span></span>

<span data-ttu-id="4d6fd-121">Specifica l'intervallo minimo, in millisecondi, tra l'invio degli eventi del mouse.</span><span class="sxs-lookup"><span data-stu-id="4d6fd-121">Specifies the minimum interval, in milliseconds, between the sending of mouse events.</span></span>

<span data-ttu-id="4d6fd-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4d6fd-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d6fd-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d6fd-123">Syntax</span></span>


```C++
HRESULT put_minInputSendInterval(
  [in]  LONG minInputSendInterval
);

HRESULT get_minInputSendInterval(
  [out] LONG *pminInputSendInterval
);
```



## <a name="property-value"></a><span data-ttu-id="4d6fd-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4d6fd-124">Property value</span></span>

<span data-ttu-id="4d6fd-125">Nuovo intervallo, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="4d6fd-125">The new interval, in milliseconds.</span></span> <span data-ttu-id="4d6fd-126">Il valore predefinito è 100.</span><span class="sxs-lookup"><span data-stu-id="4d6fd-126">The default value is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d6fd-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4d6fd-127">Error codes</span></span>

<span data-ttu-id="4d6fd-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4d6fd-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d6fd-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d6fd-129">Remarks</span></span>

<span data-ttu-id="4d6fd-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4d6fd-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d6fd-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d6fd-131">Requirements</span></span>



| <span data-ttu-id="4d6fd-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d6fd-132">Requirement</span></span> | <span data-ttu-id="4d6fd-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4d6fd-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d6fd-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d6fd-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4d6fd-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d6fd-135">Windows 7</span></span><br/>                                                                            |
| <span data-ttu-id="4d6fd-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d6fd-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4d6fd-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4d6fd-137">Windows Server 2008 R2</span></span><br/>                                                               |
| <span data-ttu-id="4d6fd-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4d6fd-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d6fd-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d6fd-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4d6fd-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4d6fd-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d6fd-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d6fd-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4d6fd-142">IID</span><span class="sxs-lookup"><span data-stu-id="4d6fd-142">IID</span></span><br/>                      | <span data-ttu-id="4d6fd-143">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="4d6fd-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d6fd-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d6fd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d6fd-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="4d6fd-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="4d6fd-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="4d6fd-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4d6fd-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="4d6fd-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="4d6fd-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4d6fd-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="4d6fd-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4d6fd-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4d6fd-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4d6fd-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4d6fd-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4d6fd-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4d6fd-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="4d6fd-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





