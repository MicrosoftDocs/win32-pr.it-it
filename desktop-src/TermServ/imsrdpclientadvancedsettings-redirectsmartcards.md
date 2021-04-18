---
title: Proprietà RedirectSmartCards di IMsRdpClientAdvancedSettings
description: Specifica se è consentito il reindirizzamento delle smart card.
ms.assetid: 53b6b483-ccba-41eb-a417-241a4430958e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectSmartCards
- Servizi Desktop remoto proprietà RedirectSmartCards, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà RedirectSmartCards
- Servizi Desktop remoto proprietà RedirectSmartCards, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà RedirectSmartCards
- Servizi Desktop remoto proprietà RedirectSmartCards, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà RedirectSmartCards
- Servizi Desktop remoto proprietà RedirectSmartCards, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà RedirectSmartCards
- Servizi Desktop remoto proprietà RedirectSmartCards, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà RedirectSmartCards
- Servizi Desktop remoto proprietà RedirectSmartCards, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà RedirectSmartCards
- Servizi Desktop remoto proprietà RedirectSmartCards, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà RedirectSmartCards
- Servizi Desktop remoto proprietà RedirectSmartCards, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà RedirectSmartCards
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectSmartCards
- IMsRdpClientAdvancedSettings.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.RedirectSmartCards
- IMsRdpClientAdvancedSettings2.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.RedirectSmartCards
- IMsRdpClientAdvancedSettings3.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.RedirectSmartCards
- IMsRdpClientAdvancedSettings4.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.RedirectSmartCards
- IMsRdpClientAdvancedSettings5.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.RedirectSmartCards
- IMsRdpClientAdvancedSettings6.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.RedirectSmartCards
- IMsRdpClientAdvancedSettings7.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.RedirectSmartCards
- IMsRdpClientAdvancedSettings8.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.put_RedirectSmartCards
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba58a492ede5371c0f43d996f46ed7a898df7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300996"
---
# <a name="imsrdpclientadvancedsettingsredirectsmartcards-property"></a><span data-ttu-id="a797a-120">Proprietà IMsRdpClientAdvancedSettings:: RedirectSmartCards</span><span class="sxs-lookup"><span data-stu-id="a797a-120">IMsRdpClientAdvancedSettings::RedirectSmartCards property</span></span>

<span data-ttu-id="a797a-121">Specifica se è consentito il reindirizzamento delle smart card.</span><span class="sxs-lookup"><span data-stu-id="a797a-121">Specifies if redirection of smart cards is allowed.</span></span>

<span data-ttu-id="a797a-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a797a-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a797a-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a797a-123">Syntax</span></span>


```C++
HRESULT put_RedirectSmartCards(
  [in]  VARIANT_BOOL redirectSmartCards
);

HRESULT get_RedirectSmartCards(
  [out] VARIANT_BOOL *predirectSmartCards
);
```



## <a name="property-value"></a><span data-ttu-id="a797a-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a797a-124">Property value</span></span>

<span data-ttu-id="a797a-125">Impostare questo parametro su **Variant \_ true** per consentire il reindirizzamento o la **variante \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a797a-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="a797a-126">**Variante \_ TRUE** chiede all'utente di confermare la concessione del reindirizzamento al momento della connessione, per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a797a-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a797a-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a797a-127">Error codes</span></span>

<span data-ttu-id="a797a-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a797a-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a797a-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="a797a-129">Remarks</span></span>

<span data-ttu-id="a797a-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a797a-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a797a-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a797a-131">Requirements</span></span>



| <span data-ttu-id="a797a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a797a-132">Requirement</span></span> | <span data-ttu-id="a797a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a797a-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a797a-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a797a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a797a-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a797a-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="a797a-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a797a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a797a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a797a-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="a797a-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a797a-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="a797a-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a797a-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a797a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a797a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a797a-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a797a-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a797a-142">IID</span><span class="sxs-lookup"><span data-stu-id="a797a-142">IID</span></span><br/>                      | <span data-ttu-id="a797a-143">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a797a-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a797a-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a797a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a797a-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a797a-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a797a-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a797a-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a797a-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a797a-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a797a-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a797a-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a797a-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a797a-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a797a-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a797a-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a797a-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a797a-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a797a-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a797a-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





