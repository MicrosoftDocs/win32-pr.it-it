---
title: Proprietà BitmapCacheSize di IMsRdpClientAdvancedSettings
description: Dimensioni, in kilobyte, del file di cache bitmap utilizzato per le bitmap a 8 bit per pixel.
ms.assetid: a2a4b739-0fa3-4a76-87ae-3cba913b7703
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà BitmapCacheSize
- Servizi Desktop remoto proprietà BitmapCacheSize, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà BitmapCacheSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.BitmapCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.BitmapCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.BitmapCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.BitmapCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.BitmapCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.BitmapCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.BitmapCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a38376bb0b06bd4efea36d3c4cad4e4aec0f35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400457"
---
# <a name="imsrdpclientadvancedsettingsbitmapcachesize-property"></a><span data-ttu-id="ec7f5-120">Proprietà IMsRdpClientAdvancedSettings:: BitmapCacheSize</span><span class="sxs-lookup"><span data-stu-id="ec7f5-120">IMsRdpClientAdvancedSettings::BitmapCacheSize property</span></span>

<span data-ttu-id="ec7f5-121">Dimensioni, in kilobyte, del file di cache bitmap utilizzato per le bitmap a 8 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="ec7f5-121">The size, in kilobytes, of the bitmap cache file used for 8-bits-per-pixel bitmaps.</span></span>

<span data-ttu-id="ec7f5-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ec7f5-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec7f5-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec7f5-123">Syntax</span></span>


```C++
HRESULT put_BitmapCacheSize(
  [in]  LONG bitmapCacheSize
);

HRESULT get_BitmapCacheSize(
  [out] LONG *pbitmapCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="ec7f5-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ec7f5-124">Property value</span></span>

<span data-ttu-id="ec7f5-125">Nuove dimensioni della cache, in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="ec7f5-125">The new cache size, in kilobytes.</span></span> <span data-ttu-id="ec7f5-126">I valori numerici validi sono compresi tra 1 e 32.</span><span class="sxs-lookup"><span data-stu-id="ec7f5-126">The valid numeric values are 1 to 32 inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ec7f5-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ec7f5-127">Error codes</span></span>

<span data-ttu-id="ec7f5-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ec7f5-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec7f5-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec7f5-129">Remarks</span></span>

<span data-ttu-id="ec7f5-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ec7f5-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec7f5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec7f5-131">Requirements</span></span>



| <span data-ttu-id="ec7f5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec7f5-132">Requirement</span></span> | <span data-ttu-id="ec7f5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ec7f5-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec7f5-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec7f5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ec7f5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec7f5-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ec7f5-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec7f5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ec7f5-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec7f5-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ec7f5-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ec7f5-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec7f5-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec7f5-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ec7f5-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ec7f5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec7f5-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec7f5-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ec7f5-142">IID</span><span class="sxs-lookup"><span data-stu-id="ec7f5-142">IID</span></span><br/>                      | <span data-ttu-id="ec7f5-143">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ec7f5-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec7f5-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec7f5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec7f5-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ec7f5-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ec7f5-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ec7f5-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ec7f5-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ec7f5-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ec7f5-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ec7f5-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ec7f5-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ec7f5-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ec7f5-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ec7f5-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ec7f5-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ec7f5-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ec7f5-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ec7f5-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





