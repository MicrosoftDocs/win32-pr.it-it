---
title: Proprietà BitmapVirtualCache16BppSize di IMsRdpClientAdvancedSettings
description: Specifica le dimensioni, in megabyte, del file di cache bitmap persistente da usare per le impostazioni di colore alto a 15 e 16 bit per pixel.
ms.assetid: f2558c88-d60f-4be3-9941-8e0e18bbb778
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BitmapVirtualCache16BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache16BppSize, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà BitmapVirtualCache16BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache16BppSize, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà BitmapVirtualCache16BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache16BppSize, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà BitmapVirtualCache16BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache16BppSize, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà BitmapVirtualCache16BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache16BppSize, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà BitmapVirtualCache16BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache16BppSize, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà BitmapVirtualCache16BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache16BppSize, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà BitmapVirtualCache16BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache16BppSize, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà BitmapVirtualCache16BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache16BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fd0a11a1cf3b313c1f6f2c12d1a73b61c6f45a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300997"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcache16bppsize-property"></a><span data-ttu-id="e0672-120">Proprietà IMsRdpClientAdvancedSettings:: BitmapVirtualCache16BppSize</span><span class="sxs-lookup"><span data-stu-id="e0672-120">IMsRdpClientAdvancedSettings::BitmapVirtualCache16BppSize property</span></span>

<span data-ttu-id="e0672-121">Specifica le dimensioni, in megabyte, del file di cache bitmap persistente da usare per le impostazioni di colore alto a 15 e 16 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="e0672-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for the 15 and 16 bits-per-pixel high-color settings.</span></span>

<span data-ttu-id="e0672-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e0672-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0672-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0672-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache16BppSize(
  [in]  LONG bitmapVirtualCache16BppSize
);

HRESULT get_BitmapVirtualCache16BppSize(
  [out] LONG *pbitmapVirtualCache16BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="e0672-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e0672-124">Property value</span></span>

<span data-ttu-id="e0672-125">Nuove dimensioni della cache.</span><span class="sxs-lookup"><span data-stu-id="e0672-125">The new cache size.</span></span> <span data-ttu-id="e0672-126">I valori validi sono compresi tra 1 e 32 e il valore predefinito è 20.</span><span class="sxs-lookup"><span data-stu-id="e0672-126">The valid values are 1 to 32 inclusive, and the default value is 20.</span></span> <span data-ttu-id="e0672-127">Si noti che la dimensione massima per tutti i file della cache virtuale è 128 MB.</span><span class="sxs-lookup"><span data-stu-id="e0672-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e0672-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e0672-128">Error codes</span></span>

<span data-ttu-id="e0672-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e0672-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0672-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0672-130">Remarks</span></span>

<span data-ttu-id="e0672-131">Le proprietà correlate includono le proprietà **BitmapVirtualCacheSize** e **BitmapVirtualCache24BppSize** .</span><span class="sxs-lookup"><span data-stu-id="e0672-131">Related properties include the **BitmapVirtualCacheSize** and **BitmapVirtualCache24BppSize** properties.</span></span>

<span data-ttu-id="e0672-132">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e0672-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0672-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0672-133">Requirements</span></span>



| <span data-ttu-id="e0672-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0672-134">Requirement</span></span> | <span data-ttu-id="e0672-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e0672-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0672-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0672-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e0672-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0672-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="e0672-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0672-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e0672-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0672-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="e0672-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e0672-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0672-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0672-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e0672-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e0672-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0672-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0672-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e0672-144">IID</span><span class="sxs-lookup"><span data-stu-id="e0672-144">IID</span></span><br/>                      | <span data-ttu-id="e0672-145">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="e0672-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0672-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0672-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0672-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e0672-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e0672-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e0672-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e0672-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e0672-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e0672-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e0672-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e0672-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e0672-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e0672-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e0672-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e0672-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e0672-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e0672-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e0672-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





