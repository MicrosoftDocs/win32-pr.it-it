---
title: Proprietà RedirectPrinters di IMsRdpClientAdvancedSettings
description: Specifica se è consentito il reindirizzamento delle stampanti.
ms.assetid: 7d4f28a7-a99d-4d0b-ab51-832a78881900
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectPrinters
- Servizi Desktop remoto proprietà RedirectPrinters, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà RedirectPrinters
- Servizi Desktop remoto proprietà RedirectPrinters, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà RedirectPrinters
- Servizi Desktop remoto proprietà RedirectPrinters, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà RedirectPrinters
- Servizi Desktop remoto proprietà RedirectPrinters, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà RedirectPrinters
- Servizi Desktop remoto proprietà RedirectPrinters, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà RedirectPrinters
- Servizi Desktop remoto proprietà RedirectPrinters, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà RedirectPrinters
- Servizi Desktop remoto proprietà RedirectPrinters, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà RedirectPrinters
- Servizi Desktop remoto proprietà RedirectPrinters, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà RedirectPrinters
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPrinters
- IMsRdpClientAdvancedSettings.get_RedirectPrinters
- IMsRdpClientAdvancedSettings.put_RedirectPrinters
- IMsRdpClientAdvancedSettings2.RedirectPrinters
- IMsRdpClientAdvancedSettings2.get_RedirectPrinters
- IMsRdpClientAdvancedSettings2.put_RedirectPrinters
- IMsRdpClientAdvancedSettings3.RedirectPrinters
- IMsRdpClientAdvancedSettings3.get_RedirectPrinters
- IMsRdpClientAdvancedSettings3.put_RedirectPrinters
- IMsRdpClientAdvancedSettings4.RedirectPrinters
- IMsRdpClientAdvancedSettings4.get_RedirectPrinters
- IMsRdpClientAdvancedSettings4.put_RedirectPrinters
- IMsRdpClientAdvancedSettings5.RedirectPrinters
- IMsRdpClientAdvancedSettings5.get_RedirectPrinters
- IMsRdpClientAdvancedSettings5.put_RedirectPrinters
- IMsRdpClientAdvancedSettings6.RedirectPrinters
- IMsRdpClientAdvancedSettings6.get_RedirectPrinters
- IMsRdpClientAdvancedSettings6.put_RedirectPrinters
- IMsRdpClientAdvancedSettings7.RedirectPrinters
- IMsRdpClientAdvancedSettings7.get_RedirectPrinters
- IMsRdpClientAdvancedSettings7.put_RedirectPrinters
- IMsRdpClientAdvancedSettings8.RedirectPrinters
- IMsRdpClientAdvancedSettings8.get_RedirectPrinters
- IMsRdpClientAdvancedSettings8.put_RedirectPrinters
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fecc3b6f72b8706168c75d220d78fc49340752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740023"
---
# <a name="imsrdpclientadvancedsettingsredirectprinters-property"></a><span data-ttu-id="745a1-120">Proprietà IMsRdpClientAdvancedSettings:: RedirectPrinters</span><span class="sxs-lookup"><span data-stu-id="745a1-120">IMsRdpClientAdvancedSettings::RedirectPrinters property</span></span>

<span data-ttu-id="745a1-121">Specifica se è consentito il reindirizzamento delle stampanti.</span><span class="sxs-lookup"><span data-stu-id="745a1-121">Specifies if redirection of printers is allowed.</span></span>

<span data-ttu-id="745a1-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="745a1-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="745a1-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="745a1-123">Syntax</span></span>


```C++
HRESULT put_RedirectPrinters(
  [in]  VARIANT_BOOL redirectPrinters
);

HRESULT get_RedirectPrinters(
  [out] VARIANT_BOOL *predirectPrinters
);
```



## <a name="property-value"></a><span data-ttu-id="745a1-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="745a1-124">Property value</span></span>

<span data-ttu-id="745a1-125">Impostare questo parametro su **Variant \_ true** per consentire il reindirizzamento o la **variante \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="745a1-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="745a1-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="745a1-126">Error codes</span></span>

<span data-ttu-id="745a1-127">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="745a1-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="745a1-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="745a1-128">Remarks</span></span>

<span data-ttu-id="745a1-129">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="745a1-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="745a1-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="745a1-130">Requirements</span></span>



| <span data-ttu-id="745a1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="745a1-131">Requirement</span></span> | <span data-ttu-id="745a1-132">Valore</span><span class="sxs-lookup"><span data-stu-id="745a1-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="745a1-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="745a1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="745a1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="745a1-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="745a1-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="745a1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="745a1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="745a1-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="745a1-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="745a1-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="745a1-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="745a1-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="745a1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="745a1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="745a1-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="745a1-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="745a1-141">IID</span><span class="sxs-lookup"><span data-stu-id="745a1-141">IID</span></span><br/>                      | <span data-ttu-id="745a1-142">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="745a1-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="745a1-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="745a1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="745a1-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="745a1-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="745a1-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="745a1-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="745a1-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="745a1-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="745a1-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="745a1-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="745a1-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="745a1-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="745a1-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="745a1-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="745a1-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="745a1-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="745a1-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="745a1-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





