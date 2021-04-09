---
title: Proprietà Compress IMsTscAdvancedSettings
description: Specifica se la compressione è abilitata.
ms.assetid: 274774b3-0442-4a46-95f8-7857f885bfdb
ms.tgt_platform: multiple
keywords:
- Comprimi Servizi Desktop remoto proprietà
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà Compress
- Comprimi Servizi Desktop remoto proprietà, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà Compress
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.Compress
- IMsTscAdvancedSettings.get_Compress
- IMsTscAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings.Compress
- IMsRdpClientAdvancedSettings.get_Compress
- IMsRdpClientAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings2.Compress
- IMsRdpClientAdvancedSettings2.get_Compress
- IMsRdpClientAdvancedSettings2.put_Compress
- IMsRdpClientAdvancedSettings3.Compress
- IMsRdpClientAdvancedSettings3.get_Compress
- IMsRdpClientAdvancedSettings3.put_Compress
- IMsRdpClientAdvancedSettings4.Compress
- IMsRdpClientAdvancedSettings4.get_Compress
- IMsRdpClientAdvancedSettings4.put_Compress
- IMsRdpClientAdvancedSettings5.Compress
- IMsRdpClientAdvancedSettings5.get_Compress
- IMsRdpClientAdvancedSettings5.put_Compress
- IMsRdpClientAdvancedSettings6.Compress
- IMsRdpClientAdvancedSettings6.get_Compress
- IMsRdpClientAdvancedSettings6.put_Compress
- IMsRdpClientAdvancedSettings7.Compress
- IMsRdpClientAdvancedSettings7.get_Compress
- IMsRdpClientAdvancedSettings7.put_Compress
- IMsRdpClientAdvancedSettings8.Compress
- IMsRdpClientAdvancedSettings8.get_Compress
- IMsRdpClientAdvancedSettings8.put_Compress
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c588784d9b06bd2e8e1605a96c8aa9fd157c10eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964422"
---
# <a name="imstscadvancedsettingscompress-property"></a><span data-ttu-id="03ecc-122">Proprietà IMsTscAdvancedSettings:: Compress</span><span class="sxs-lookup"><span data-stu-id="03ecc-122">IMsTscAdvancedSettings::Compress property</span></span>

<span data-ttu-id="03ecc-123">Specifica se la compressione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="03ecc-123">Specifies whether compression is enabled.</span></span>

<span data-ttu-id="03ecc-124">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="03ecc-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ecc-125">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03ecc-125">Syntax</span></span>


```C++
HRESULT put_Compress(
  [in]  LONG compress
);

HRESULT get_Compress(
  [out] LONG *pcompress
);
```



## <a name="property-value"></a><span data-ttu-id="03ecc-126">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="03ecc-126">Property value</span></span>

<span data-ttu-id="03ecc-127">Impostare questo parametro su 0 per disabilitare la compressione o un valore diverso da zero per abilitare la compressione.</span><span class="sxs-lookup"><span data-stu-id="03ecc-127">Set this parameter to 0 to disable compression or a nonzero value to enable compression.</span></span>

## <a name="error-codes"></a><span data-ttu-id="03ecc-128">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="03ecc-128">Error codes</span></span>

<span data-ttu-id="03ecc-129">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="03ecc-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="03ecc-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="03ecc-130">Remarks</span></span>

<span data-ttu-id="03ecc-131">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="03ecc-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03ecc-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03ecc-132">Requirements</span></span>



| <span data-ttu-id="03ecc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="03ecc-133">Requirement</span></span> | <span data-ttu-id="03ecc-134">Valore</span><span class="sxs-lookup"><span data-stu-id="03ecc-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ecc-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03ecc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="03ecc-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03ecc-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="03ecc-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03ecc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="03ecc-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03ecc-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="03ecc-139">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="03ecc-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="03ecc-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03ecc-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="03ecc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="03ecc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03ecc-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03ecc-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="03ecc-143">IID</span><span class="sxs-lookup"><span data-stu-id="03ecc-143">IID</span></span><br/>                      | <span data-ttu-id="03ecc-144">IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="03ecc-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="03ecc-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03ecc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ecc-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="03ecc-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="03ecc-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="03ecc-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="03ecc-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="03ecc-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="03ecc-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="03ecc-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="03ecc-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="03ecc-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="03ecc-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="03ecc-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="03ecc-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="03ecc-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="03ecc-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="03ecc-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="03ecc-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="03ecc-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





