---
title: Proprietà ShadowBitmap di IMsRdpClientAdvancedSettings
description: Specifica se devono essere utilizzate le bitmap Shadow.
ms.assetid: b329e367-7579-466d-877a-16253f85e5a2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, Proprietà ShadowBitmap
- Servizi Desktop remoto Proprietà ShadowBitmap, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, Proprietà ShadowBitmap
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ShadowBitmap
- IMsRdpClientAdvancedSettings.get_ShadowBitmap
- IMsRdpClientAdvancedSettings.put_ShadowBitmap
- IMsRdpClientAdvancedSettings2.ShadowBitmap
- IMsRdpClientAdvancedSettings2.get_ShadowBitmap
- IMsRdpClientAdvancedSettings2.put_ShadowBitmap
- IMsRdpClientAdvancedSettings3.ShadowBitmap
- IMsRdpClientAdvancedSettings3.get_ShadowBitmap
- IMsRdpClientAdvancedSettings3.put_ShadowBitmap
- IMsRdpClientAdvancedSettings4.ShadowBitmap
- IMsRdpClientAdvancedSettings4.get_ShadowBitmap
- IMsRdpClientAdvancedSettings4.put_ShadowBitmap
- IMsRdpClientAdvancedSettings5.ShadowBitmap
- IMsRdpClientAdvancedSettings5.get_ShadowBitmap
- IMsRdpClientAdvancedSettings5.put_ShadowBitmap
- IMsRdpClientAdvancedSettings6.ShadowBitmap
- IMsRdpClientAdvancedSettings6.get_ShadowBitmap
- IMsRdpClientAdvancedSettings6.put_ShadowBitmap
- IMsRdpClientAdvancedSettings7.ShadowBitmap
- IMsRdpClientAdvancedSettings7.get_ShadowBitmap
- IMsRdpClientAdvancedSettings7.put_ShadowBitmap
- IMsRdpClientAdvancedSettings8.ShadowBitmap
- IMsRdpClientAdvancedSettings8.get_ShadowBitmap
- IMsRdpClientAdvancedSettings8.put_ShadowBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6c43862b498fe5828d2746666c5e414de4c71e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475232"
---
# <a name="imsrdpclientadvancedsettingsshadowbitmap-property"></a><span data-ttu-id="9cd46-120">Proprietà IMsRdpClientAdvancedSettings:: ShadowBitmap</span><span class="sxs-lookup"><span data-stu-id="9cd46-120">IMsRdpClientAdvancedSettings::ShadowBitmap property</span></span>

<span data-ttu-id="9cd46-121">\[Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="9cd46-121">\[This property is not supported.</span></span> <span data-ttu-id="9cd46-122">A partire da Windows Server 2008 e Windows 7, le chiamate a **ShadowBitmap** restituiscono sempre **S \_ false**.\]</span><span class="sxs-lookup"><span data-stu-id="9cd46-122">Starting with Windows Server 2008 and Windows 7, calls to **ShadowBitmap** always return **S\_FALSE**.\]</span></span>

<span data-ttu-id="9cd46-123">Specifica se devono essere utilizzate le bitmap Shadow.</span><span class="sxs-lookup"><span data-stu-id="9cd46-123">Specifies if shadow bitmaps should be used.</span></span>

<span data-ttu-id="9cd46-124">Le bitmap Shadow sono sempre disabilitate in modalità schermo intero, pertanto questa proprietà non ha alcun effetto in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="9cd46-124">Shadow bitmaps are always disabled in full-screen mode, therefore this property has no effect when in full-screen mode.</span></span>

<span data-ttu-id="9cd46-125">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9cd46-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd46-126">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cd46-126">Syntax</span></span>


```C++
HRESULT put_ShadowBitmap(
  [in]  LONG shadowBitmap
);

HRESULT get_ShadowBitmap(
  [out] LONG *pshadowBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="9cd46-127">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9cd46-127">Property value</span></span>

<span data-ttu-id="9cd46-128">Impostare questo parametro su 0 per disabilitare la funzionalità o un valore diverso da zero per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="9cd46-128">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="9cd46-129">La disabilitazione di questa funzionalità consente in genere di migliorare le prestazioni, ma può generare artefatti quando si disegnano schermate.</span><span class="sxs-lookup"><span data-stu-id="9cd46-129">Disabling this feature typically improves performance but can result in artifacts when painting screens.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cd46-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cd46-130">Remarks</span></span>

<span data-ttu-id="9cd46-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9cd46-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cd46-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cd46-132">Requirements</span></span>



| <span data-ttu-id="9cd46-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cd46-133">Requirement</span></span> | <span data-ttu-id="9cd46-134">Valore</span><span class="sxs-lookup"><span data-stu-id="9cd46-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd46-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cd46-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9cd46-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cd46-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="9cd46-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cd46-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9cd46-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9cd46-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9cd46-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9cd46-139">End of client support</span></span><br/>    | <span data-ttu-id="9cd46-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cd46-140">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="9cd46-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="9cd46-141">End of server support</span></span><br/>    | <span data-ttu-id="9cd46-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9cd46-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9cd46-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9cd46-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="9cd46-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cd46-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9cd46-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9cd46-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cd46-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cd46-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9cd46-147">IID</span><span class="sxs-lookup"><span data-stu-id="9cd46-147">IID</span></span><br/>                      | <span data-ttu-id="9cd46-148">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="9cd46-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9cd46-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cd46-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd46-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="9cd46-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="9cd46-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9cd46-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="9cd46-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9cd46-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9cd46-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9cd46-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9cd46-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9cd46-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9cd46-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9cd46-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9cd46-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9cd46-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9cd46-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="9cd46-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





