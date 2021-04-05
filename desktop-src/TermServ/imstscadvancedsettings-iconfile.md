---
title: Proprietà IconFile di IMsTscAdvancedSettings
description: Specifica il nome del file che contiene i dati dell'icona a cui sarà possibile accedere quando viene visualizzato il client in modalità schermo intero.
ms.assetid: 2b6ac2ad-9745-4b80-a415-4840cd8aa8b3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà IconFile
- Servizi Desktop remoto Proprietà IconFile, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà IconFile
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconFile
- IMsTscAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings.IconFile
- IMsRdpClientAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings2.IconFile
- IMsRdpClientAdvancedSettings2.put_IconFile
- IMsRdpClientAdvancedSettings3.IconFile
- IMsRdpClientAdvancedSettings3.put_IconFile
- IMsRdpClientAdvancedSettings4.IconFile
- IMsRdpClientAdvancedSettings4.put_IconFile
- IMsRdpClientAdvancedSettings5.IconFile
- IMsRdpClientAdvancedSettings5.put_IconFile
- IMsRdpClientAdvancedSettings6.IconFile
- IMsRdpClientAdvancedSettings6.put_IconFile
- IMsRdpClientAdvancedSettings7.IconFile
- IMsRdpClientAdvancedSettings7.put_IconFile
- IMsRdpClientAdvancedSettings8.IconFile
- IMsRdpClientAdvancedSettings8.put_IconFile
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d8f996e70873d5584bb80bbf4f40f71a7deae8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741506"
---
# <a name="imstscadvancedsettingsiconfile-property"></a><span data-ttu-id="cf932-122">Proprietà IMsTscAdvancedSettings:: IconFile</span><span class="sxs-lookup"><span data-stu-id="cf932-122">IMsTscAdvancedSettings::IconFile property</span></span>

<span data-ttu-id="cf932-123">Specifica il nome del file che contiene i dati dell'icona a cui sarà possibile accedere quando viene visualizzato il client in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="cf932-123">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="cf932-124">Questa proprietà non è supportata nel controllo ActiveX (MsRdp. ocx).</span><span class="sxs-lookup"><span data-stu-id="cf932-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="cf932-125">È supportato nella libreria MsTscAx.dll inclusa nel client standard (MsTsc.exe).</span><span class="sxs-lookup"><span data-stu-id="cf932-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="cf932-126">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="cf932-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf932-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf932-127">Syntax</span></span>


```C++
HRESULT put_IconFile(
  [in] BSTR IconFile
);
```



## <a name="property-value"></a><span data-ttu-id="cf932-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="cf932-128">Property value</span></span>

<span data-ttu-id="cf932-129">Percorso completo del file icona o di un file contenente i dati delle icone, ad esempio una DLL.</span><span class="sxs-lookup"><span data-stu-id="cf932-129">The fully qualified path of icon file or a file containing icon data, such as a DLL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cf932-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="cf932-130">Error codes</span></span>

<span data-ttu-id="cf932-131">Restituisce un valore **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="cf932-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf932-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf932-132">Remarks</span></span>

<span data-ttu-id="cf932-133">L'estensione del nome file di un file icona è ". ico".</span><span class="sxs-lookup"><span data-stu-id="cf932-133">The file name extension of an icon file is ".ico".</span></span>

<span data-ttu-id="cf932-134">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cf932-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf932-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf932-135">Requirements</span></span>



| <span data-ttu-id="cf932-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf932-136">Requirement</span></span> | <span data-ttu-id="cf932-137">Valore</span><span class="sxs-lookup"><span data-stu-id="cf932-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf932-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf932-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cf932-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf932-139">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="cf932-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cf932-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cf932-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf932-141">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="cf932-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="cf932-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="cf932-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf932-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="cf932-144">DLL</span><span class="sxs-lookup"><span data-stu-id="cf932-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf932-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf932-145"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="cf932-146">IID</span><span class="sxs-lookup"><span data-stu-id="cf932-146">IID</span></span><br/>                      | <span data-ttu-id="cf932-147">IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="cf932-147">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf932-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf932-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf932-149">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="cf932-149">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="cf932-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="cf932-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="cf932-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="cf932-151">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="cf932-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="cf932-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="cf932-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="cf932-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="cf932-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="cf932-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="cf932-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="cf932-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="cf932-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="cf932-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="cf932-157">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="cf932-157">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





