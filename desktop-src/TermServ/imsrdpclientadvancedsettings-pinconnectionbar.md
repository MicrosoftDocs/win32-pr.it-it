---
title: Proprietà PinConnectionBar di IMsRdpClientAdvancedSettings
description: Specifica lo stato della barra di connessione dell'interfaccia utente.
ms.assetid: b1f9cb02-3ee3-4574-a874-2584b0d5b47e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà PinConnectionBar
- Servizi Desktop remoto proprietà PinConnectionBar, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà PinConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PinConnectionBar
- IMsRdpClientAdvancedSettings.get_PinConnectionBar
- IMsRdpClientAdvancedSettings.put_PinConnectionBar
- IMsRdpClientAdvancedSettings2.PinConnectionBar
- IMsRdpClientAdvancedSettings2.get_PinConnectionBar
- IMsRdpClientAdvancedSettings2.put_PinConnectionBar
- IMsRdpClientAdvancedSettings3.PinConnectionBar
- IMsRdpClientAdvancedSettings3.get_PinConnectionBar
- IMsRdpClientAdvancedSettings3.put_PinConnectionBar
- IMsRdpClientAdvancedSettings4.PinConnectionBar
- IMsRdpClientAdvancedSettings4.get_PinConnectionBar
- IMsRdpClientAdvancedSettings4.put_PinConnectionBar
- IMsRdpClientAdvancedSettings5.PinConnectionBar
- IMsRdpClientAdvancedSettings5.get_PinConnectionBar
- IMsRdpClientAdvancedSettings5.put_PinConnectionBar
- IMsRdpClientAdvancedSettings6.PinConnectionBar
- IMsRdpClientAdvancedSettings6.get_PinConnectionBar
- IMsRdpClientAdvancedSettings6.put_PinConnectionBar
- IMsRdpClientAdvancedSettings7.PinConnectionBar
- IMsRdpClientAdvancedSettings7.get_PinConnectionBar
- IMsRdpClientAdvancedSettings7.put_PinConnectionBar
- IMsRdpClientAdvancedSettings8.PinConnectionBar
- IMsRdpClientAdvancedSettings8.get_PinConnectionBar
- IMsRdpClientAdvancedSettings8.put_PinConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0da294d933026194d7307a7fa0a175575761809e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873341"
---
# <a name="imsrdpclientadvancedsettingspinconnectionbar-property"></a><span data-ttu-id="b587d-120">IMsRdpClientAdvancedSettings::P proprietà inConnectionBar</span><span class="sxs-lookup"><span data-stu-id="b587d-120">IMsRdpClientAdvancedSettings::PinConnectionBar property</span></span>

<span data-ttu-id="b587d-121">Specifica lo stato della barra di connessione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="b587d-121">Specifies the state of the UI connection bar.</span></span>

<span data-ttu-id="b587d-122">Questa proprietà restituisce **E \_ NOTIMPL** se il contenitore chiama il metodo [**IObjectSafety:: SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b587d-122">This property returns **E\_NOTIMPL** if the container calls the [**IObjectSafety::SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) method.</span></span>

<span data-ttu-id="b587d-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b587d-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b587d-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b587d-124">Syntax</span></span>


```C++
HRESULT put_PinConnectionBar(
  [in]  VARIANT_BOOL fPinConnectionBar
);

HRESULT get_PinConnectionBar(
  [out] VARIANT_BOOL *pfPinConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="b587d-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b587d-125">Property value</span></span>

<span data-ttu-id="b587d-126">Impostando questa proprietà su **Variant \_ true** , lo stato viene impostato su "abbassato", ovvero invisibile per l'utente e non disponibile per l'input.</span><span class="sxs-lookup"><span data-stu-id="b587d-126">Setting this property to **VARIANT\_TRUE** sets the state to "lowered", that is, invisible to the user and unavailable for input.</span></span> <span data-ttu-id="b587d-127">**Variante \_ FALSE** imposta lo stato su "Raised" e disponibile per l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b587d-127">**VARIANT\_FALSE** sets the state to "raised" and available for user input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b587d-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b587d-128">Error codes</span></span>

<span data-ttu-id="b587d-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b587d-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b587d-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="b587d-130">Remarks</span></span>

<span data-ttu-id="b587d-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b587d-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b587d-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b587d-132">Requirements</span></span>



| <span data-ttu-id="b587d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b587d-133">Requirement</span></span> | <span data-ttu-id="b587d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b587d-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b587d-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b587d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b587d-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b587d-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="b587d-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b587d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b587d-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b587d-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="b587d-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b587d-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="b587d-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b587d-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b587d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b587d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b587d-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b587d-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b587d-143">IID</span><span class="sxs-lookup"><span data-stu-id="b587d-143">IID</span></span><br/>                      | <span data-ttu-id="b587d-144">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="b587d-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b587d-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b587d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b587d-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="b587d-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="b587d-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b587d-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b587d-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b587d-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="b587d-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b587d-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b587d-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b587d-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b587d-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b587d-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b587d-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b587d-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b587d-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b587d-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

