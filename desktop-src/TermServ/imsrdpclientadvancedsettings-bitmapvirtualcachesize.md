---
title: Proprietà BitmapVirtualCacheSize di IMsRdpClientAdvancedSettings
description: Specifica le dimensioni in megabyte del file di cache bitmap persistente da utilizzare per il colore a 8 bit per pixel.
ms.assetid: 4efcabd2-8671-40a3-ad12-af0b2b6e495a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
- Servizi Desktop remoto proprietà BitmapVirtualCacheSize, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà BitmapVirtualCacheSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb652c0f235cf7438b49e68a544188ac4622acad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048088"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcachesize-property"></a><span data-ttu-id="324fd-120">Proprietà IMsRdpClientAdvancedSettings:: BitmapVirtualCacheSize</span><span class="sxs-lookup"><span data-stu-id="324fd-120">IMsRdpClientAdvancedSettings::BitmapVirtualCacheSize property</span></span>

<span data-ttu-id="324fd-121">Specifica le dimensioni in megabyte del file di cache bitmap persistente da utilizzare per il colore a 8 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="324fd-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for 8-bits-per-pixel color.</span></span>

<span data-ttu-id="324fd-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="324fd-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="324fd-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="324fd-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCacheSize(
  [in]  LONG bitmapVirtualCacheSize
);

HRESULT get_BitmapVirtualCacheSize(
  [out] LONG *pbitmapVirtualCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="324fd-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="324fd-124">Property value</span></span>

<span data-ttu-id="324fd-125">Nuove dimensioni della cache.</span><span class="sxs-lookup"><span data-stu-id="324fd-125">The new cache size.</span></span> <span data-ttu-id="324fd-126">I valori validi sono compresi tra 1 e 32.</span><span class="sxs-lookup"><span data-stu-id="324fd-126">The valid values are 1 to 32 inclusive.</span></span> <span data-ttu-id="324fd-127">Si noti che la dimensione massima per tutti i file della cache virtuale è 128 MB.</span><span class="sxs-lookup"><span data-stu-id="324fd-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="324fd-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="324fd-128">Error codes</span></span>

<span data-ttu-id="324fd-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="324fd-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="324fd-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="324fd-130">Remarks</span></span>

<span data-ttu-id="324fd-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="324fd-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="324fd-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="324fd-132">Requirements</span></span>



| <span data-ttu-id="324fd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="324fd-133">Requirement</span></span> | <span data-ttu-id="324fd-134">Valore</span><span class="sxs-lookup"><span data-stu-id="324fd-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="324fd-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="324fd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="324fd-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="324fd-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="324fd-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="324fd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="324fd-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="324fd-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="324fd-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="324fd-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="324fd-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="324fd-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="324fd-141">DLL</span><span class="sxs-lookup"><span data-stu-id="324fd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="324fd-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="324fd-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="324fd-143">IID</span><span class="sxs-lookup"><span data-stu-id="324fd-143">IID</span></span><br/>                      | <span data-ttu-id="324fd-144">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="324fd-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="324fd-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="324fd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="324fd-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="324fd-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="324fd-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="324fd-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="324fd-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="324fd-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="324fd-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="324fd-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="324fd-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="324fd-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="324fd-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="324fd-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="324fd-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="324fd-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="324fd-153">**BitmapVirtualCache16BppSize**</span><span class="sxs-lookup"><span data-stu-id="324fd-153">**BitmapVirtualCache16BppSize**</span></span>](imsrdpclientadvancedsettings-bitmapvirtualcache16bppsize.md)
</dt> <dt>

[<span data-ttu-id="324fd-154">**BitmapVirtualCache24BppSize**</span><span class="sxs-lookup"><span data-stu-id="324fd-154">**BitmapVirtualCache24BppSize**</span></span>](imsrdpclientadvancedsettings-bitmapvirtualcache24bppsize.md)
</dt> <dt>

[<span data-ttu-id="324fd-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="324fd-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





