---
title: Proprietà IconIndex di IMsTscAdvancedSettings
description: Specifica l'indice dell'icona all'interno del file icona corrente.
ms.assetid: c29ae1a7-9c54-4e56-bb69-4e929e8a4e5c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà IconIndex
- Servizi Desktop remoto proprietà IconIndex, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà IconIndex
- Servizi Desktop remoto proprietà IconIndex, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà IconIndex
- Servizi Desktop remoto proprietà IconIndex, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà IconIndex
- Servizi Desktop remoto proprietà IconIndex, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà IconIndex
- Servizi Desktop remoto proprietà IconIndex, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà IconIndex
- Servizi Desktop remoto proprietà IconIndex, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà IconIndex
- Servizi Desktop remoto proprietà IconIndex, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà IconIndex
- Servizi Desktop remoto proprietà IconIndex, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà IconIndex
- Servizi Desktop remoto proprietà IconIndex, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà IconIndex
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconIndex
- IMsTscAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings.IconIndex
- IMsRdpClientAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings2.IconIndex
- IMsRdpClientAdvancedSettings2.put_IconIndex
- IMsRdpClientAdvancedSettings3.IconIndex
- IMsRdpClientAdvancedSettings3.put_IconIndex
- IMsRdpClientAdvancedSettings4.IconIndex
- IMsRdpClientAdvancedSettings4.put_IconIndex
- IMsRdpClientAdvancedSettings5.IconIndex
- IMsRdpClientAdvancedSettings5.put_IconIndex
- IMsRdpClientAdvancedSettings6.IconIndex
- IMsRdpClientAdvancedSettings6.put_IconIndex
- IMsRdpClientAdvancedSettings7.IconIndex
- IMsRdpClientAdvancedSettings7.put_IconIndex
- IMsRdpClientAdvancedSettings8.IconIndex
- IMsRdpClientAdvancedSettings8.put_IconIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be56eab5dbe7f03155c6082e4e70fc4bd439253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517751"
---
# <a name="imstscadvancedsettingsiconindex-property"></a><span data-ttu-id="59993-122">Proprietà IMsTscAdvancedSettings:: IconIndex</span><span class="sxs-lookup"><span data-stu-id="59993-122">IMsTscAdvancedSettings::IconIndex property</span></span>

<span data-ttu-id="59993-123">Specifica l'indice dell'icona all'interno del file icona corrente.</span><span class="sxs-lookup"><span data-stu-id="59993-123">Specifies the index of the icon within the current icon file.</span></span>

> [!Note]  
> <span data-ttu-id="59993-124">Questa proprietà non è supportata nel controllo ActiveX (MsRdp. ocx).</span><span class="sxs-lookup"><span data-stu-id="59993-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="59993-125">È supportato nella libreria MsTscAx.dll inclusa nel client standard (MsTsc.exe).</span><span class="sxs-lookup"><span data-stu-id="59993-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="59993-126">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="59993-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="59993-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59993-127">Syntax</span></span>


```C++
HRESULT put_IconIndex(
  [in] LONG IconIndex
);
```



## <a name="property-value"></a><span data-ttu-id="59993-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="59993-128">Property value</span></span>

<span data-ttu-id="59993-129">Indice dell'icona.</span><span class="sxs-lookup"><span data-stu-id="59993-129">The index of the icon.</span></span>

## <a name="error-codes"></a><span data-ttu-id="59993-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="59993-130">Error codes</span></span>

<span data-ttu-id="59993-131">Restituisce un valore **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="59993-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="59993-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="59993-132">Remarks</span></span>

<span data-ttu-id="59993-133">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="59993-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="59993-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59993-134">Requirements</span></span>



| <span data-ttu-id="59993-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="59993-135">Requirement</span></span> | <span data-ttu-id="59993-136">Valore</span><span class="sxs-lookup"><span data-stu-id="59993-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="59993-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59993-137">Minimum supported client</span></span><br/> | <span data-ttu-id="59993-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59993-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="59993-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59993-139">Minimum supported server</span></span><br/> | <span data-ttu-id="59993-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59993-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="59993-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="59993-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="59993-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59993-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="59993-143">DLL</span><span class="sxs-lookup"><span data-stu-id="59993-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59993-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59993-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="59993-145">IID</span><span class="sxs-lookup"><span data-stu-id="59993-145">IID</span></span><br/>                      | <span data-ttu-id="59993-146">IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="59993-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59993-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59993-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59993-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="59993-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="59993-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="59993-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="59993-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="59993-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="59993-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="59993-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="59993-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="59993-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="59993-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="59993-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="59993-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="59993-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="59993-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="59993-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="59993-156">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="59993-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





