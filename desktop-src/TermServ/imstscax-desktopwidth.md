---
title: Proprietà DesktopWidth di IMsTscAx
description: Specifica la larghezza del controllo corrente, in pixel, sul desktop remoto iniziale.
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DesktopWidth
- Servizi Desktop remoto proprietà DesktopWidth, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà DesktopWidth
- Servizi Desktop remoto proprietà DesktopWidth, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà DesktopWidth
- Servizi Desktop remoto proprietà DesktopWidth, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà DesktopWidth
- Servizi Desktop remoto proprietà DesktopWidth, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà DesktopWidth
- Servizi Desktop remoto proprietà DesktopWidth, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà DesktopWidth
- Servizi Desktop remoto proprietà DesktopWidth, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà DesktopWidth
- Servizi Desktop remoto proprietà DesktopWidth, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà DesktopWidth
- Servizi Desktop remoto proprietà DesktopWidth, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà DesktopWidth
- Servizi Desktop remoto proprietà DesktopWidth, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà DesktopWidth
- Servizi Desktop remoto proprietà DesktopWidth, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà DesktopWidth
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16cd1391c6aeb27d9ec0f87317b06e9084337fbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517746"
---
# <a name="imstscaxdesktopwidth-property"></a><span data-ttu-id="0f55d-124">IMsTscAx::D Proprietà esktopWidth</span><span class="sxs-lookup"><span data-stu-id="0f55d-124">IMsTscAx::DesktopWidth property</span></span>

<span data-ttu-id="0f55d-125">Specifica la larghezza del controllo corrente, in pixel, sul desktop remoto iniziale.</span><span class="sxs-lookup"><span data-stu-id="0f55d-125">Specifies the current control's width, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="0f55d-126">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0f55d-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f55d-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f55d-127">Syntax</span></span>


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="0f55d-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0f55d-128">Property value</span></span>

<span data-ttu-id="0f55d-129">Nuova larghezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="0f55d-129">The new width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0f55d-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0f55d-130">Error codes</span></span>

<span data-ttu-id="0f55d-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="0f55d-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f55d-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f55d-132">Remarks</span></span>

<span data-ttu-id="0f55d-133">L'impostazione della proprietà **DesktopWidth** è facoltativa, ma deve essere impostata prima di chiamare il metodo [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0f55d-133">Setting the **DesktopWidth** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="0f55d-134">Se non viene specificata una larghezza del desktop o è impostata su zero, la larghezza del desktop viene impostata sulla larghezza del controllo.</span><span class="sxs-lookup"><span data-stu-id="0f55d-134">If a desktop width is not specified, or is set to zero, the desktop width is set to the width of the control.</span></span> <span data-ttu-id="0f55d-135">I valori minimo e massimo dipendono dalla versione del sistema operativo del client Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0f55d-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="0f55d-136"><span id="_"></span>Windows 8/Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f55d-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="0f55d-137">200 minimo, 8192 massimo</span><span class="sxs-lookup"><span data-stu-id="0f55d-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="0f55d-138"><span id="_"></span>Windows 7/Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f55d-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="0f55d-139">200 minimo, 2048 massimo</span><span class="sxs-lookup"><span data-stu-id="0f55d-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="0f55d-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f55d-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="0f55d-141">200 minimo, 1200 massimo</span><span class="sxs-lookup"><span data-stu-id="0f55d-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="0f55d-142">Una volta stabilita una connessione, qualsiasi modifica apportata alla larghezza del controllo non modifica la larghezza del desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0f55d-142">After a connection is established, any changes to the control's width do not change the width of the remote desktop.</span></span> <span data-ttu-id="0f55d-143">Al contrario, il controllo Visualizza le barre di scorrimento o Centra il desktop remoto, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="0f55d-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="0f55d-144">Per modificare le dimensioni del desktop di una connessione attiva, usare il metodo [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0f55d-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="0f55d-145">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0f55d-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f55d-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f55d-146">Requirements</span></span>



| <span data-ttu-id="0f55d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f55d-147">Requirement</span></span> | <span data-ttu-id="0f55d-148">Valore</span><span class="sxs-lookup"><span data-stu-id="0f55d-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f55d-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f55d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0f55d-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f55d-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0f55d-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f55d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0f55d-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f55d-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0f55d-153">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0f55d-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f55d-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f55d-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f55d-155">DLL</span><span class="sxs-lookup"><span data-stu-id="0f55d-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f55d-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f55d-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f55d-157">IID</span><span class="sxs-lookup"><span data-stu-id="0f55d-157">IID</span></span><br/>                      | <span data-ttu-id="0f55d-158">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="0f55d-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0f55d-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f55d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f55d-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="0f55d-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0f55d-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0f55d-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0f55d-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0f55d-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0f55d-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0f55d-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0f55d-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0f55d-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0f55d-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0f55d-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0f55d-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0f55d-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0f55d-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0f55d-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0f55d-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0f55d-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0f55d-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="0f55d-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





