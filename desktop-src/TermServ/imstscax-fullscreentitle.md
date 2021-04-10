---
title: Proprietà FullScreenTitle di IMsTscAx
description: Specifica il titolo della finestra visualizzata quando il controllo è in modalità schermo intero.
ms.assetid: 441aea43-2d1c-44b7-a74f-e375e711fb4f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà FullScreenTitle
- Servizi Desktop remoto proprietà FullScreenTitle, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà FullScreenTitle
topic_type:
- apiref
api_name:
- IMsTscAx.FullScreenTitle
- IMsTscAx.put_FullScreenTitle
- IMsRdpClient.FullScreenTitle
- IMsRdpClient.put_FullScreenTitle
- IMsRdpClient2.FullScreenTitle
- IMsRdpClient2.put_FullScreenTitle
- IMsRdpClient3.FullScreenTitle
- IMsRdpClient3.put_FullScreenTitle
- IMsRdpClient4.FullScreenTitle
- IMsRdpClient4.put_FullScreenTitle
- IMsRdpClient5.FullScreenTitle
- IMsRdpClient5.put_FullScreenTitle
- IMsRdpClient6.FullScreenTitle
- IMsRdpClient6.put_FullScreenTitle
- IMsRdpClient7.FullScreenTitle
- IMsRdpClient7.put_FullScreenTitle
- IMsRdpClient8.FullScreenTitle
- IMsRdpClient8.put_FullScreenTitle
- IMsRdpClient9.FullScreenTitle
- IMsRdpClient9.put_FullScreenTitle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1384d1582f4f0089df55030c22471438575bd072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120202"
---
# <a name="imstscaxfullscreentitle-property"></a><span data-ttu-id="e5221-124">Proprietà IMsTscAx:: FullScreenTitle</span><span class="sxs-lookup"><span data-stu-id="e5221-124">IMsTscAx::FullScreenTitle property</span></span>

<span data-ttu-id="e5221-125">Specifica il titolo della finestra visualizzata quando il controllo è in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="e5221-125">Specifies the window title displayed when the control is in full-screen mode.</span></span>

<span data-ttu-id="e5221-126">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="e5221-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5221-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5221-127">Syntax</span></span>


```C++
HRESULT put_FullScreenTitle(
  [in] BSTR fullScreenTitle
);
```



## <a name="property-value"></a><span data-ttu-id="e5221-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e5221-128">Property value</span></span>

<span data-ttu-id="e5221-129">Titolo della finestra.</span><span class="sxs-lookup"><span data-stu-id="e5221-129">The window title.</span></span> <span data-ttu-id="e5221-130">La lunghezza massima di questa stringa è MAX \_ Path-1 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e5221-130">The maximum length of this string is MAX\_PATH-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e5221-131">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e5221-131">Error codes</span></span>

<span data-ttu-id="e5221-132">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="e5221-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5221-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5221-133">Remarks</span></span>

<span data-ttu-id="e5221-134">Questa proprietà viene utilizzata per impostare il titolo della finestra del controllo quando la connessione viene aperta in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="e5221-134">This property is used to set the title of the control's window when the connection is opened in full-screen mode.</span></span> <span data-ttu-id="e5221-135">Non usare questa proprietà per la modalità a schermo intero gestita dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="e5221-135">Do not use this property for container-handled full-screen mode.</span></span> <span data-ttu-id="e5221-136">Quando viene chiamato il metodo [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) , nella finestra del contenitore viene visualizzato il titolo della finestra.</span><span class="sxs-lookup"><span data-stu-id="e5221-136">When the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called, the container window displays the window title.</span></span>

<span data-ttu-id="e5221-137">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e5221-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5221-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5221-138">Requirements</span></span>



| <span data-ttu-id="e5221-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5221-139">Requirement</span></span> | <span data-ttu-id="e5221-140">Valore</span><span class="sxs-lookup"><span data-stu-id="e5221-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5221-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5221-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e5221-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5221-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e5221-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5221-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e5221-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5221-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e5221-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e5221-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="e5221-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5221-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e5221-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e5221-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5221-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5221-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e5221-149">IID</span><span class="sxs-lookup"><span data-stu-id="e5221-149">IID</span></span><br/>                      | <span data-ttu-id="e5221-150">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="e5221-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e5221-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5221-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5221-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="e5221-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="e5221-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e5221-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e5221-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e5221-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e5221-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e5221-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e5221-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e5221-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e5221-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e5221-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e5221-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e5221-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e5221-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e5221-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e5221-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e5221-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e5221-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="e5221-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





