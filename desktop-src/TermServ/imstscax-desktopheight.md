---
title: Proprietà DesktopHeight di IMsTscAx
description: Specifica l'altezza, in pixel, del controllo corrente sul desktop remoto iniziale.
ms.assetid: 7071053b-bdd1-408b-ab69-965c504fafb0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DesktopHeight
- Servizi Desktop remoto proprietà DesktopHeight, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà DesktopHeight
- Servizi Desktop remoto proprietà DesktopHeight, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà DesktopHeight
- Servizi Desktop remoto proprietà DesktopHeight, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà DesktopHeight
- Servizi Desktop remoto proprietà DesktopHeight, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà DesktopHeight
- Servizi Desktop remoto proprietà DesktopHeight, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà DesktopHeight
- Servizi Desktop remoto proprietà DesktopHeight, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà DesktopHeight
- Servizi Desktop remoto proprietà DesktopHeight, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà DesktopHeight
- Servizi Desktop remoto proprietà DesktopHeight, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà DesktopHeight
- Servizi Desktop remoto proprietà DesktopHeight, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà DesktopHeight
- Servizi Desktop remoto proprietà DesktopHeight, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà DesktopHeight
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopHeight
- IMsTscAx.get_DesktopHeight
- IMsTscAx.put_DesktopHeight
- IMsRdpClient.DesktopHeight
- IMsRdpClient.get_DesktopHeight
- IMsRdpClient.put_DesktopHeight
- IMsRdpClient2.DesktopHeight
- IMsRdpClient2.get_DesktopHeight
- IMsRdpClient2.put_DesktopHeight
- IMsRdpClient3.DesktopHeight
- IMsRdpClient3.get_DesktopHeight
- IMsRdpClient3.put_DesktopHeight
- IMsRdpClient4.DesktopHeight
- IMsRdpClient4.get_DesktopHeight
- IMsRdpClient4.put_DesktopHeight
- IMsRdpClient5.DesktopHeight
- IMsRdpClient5.get_DesktopHeight
- IMsRdpClient5.put_DesktopHeight
- IMsRdpClient6.DesktopHeight
- IMsRdpClient6.get_DesktopHeight
- IMsRdpClient6.put_DesktopHeight
- IMsRdpClient7.DesktopHeight
- IMsRdpClient7.get_DesktopHeight
- IMsRdpClient7.put_DesktopHeight
- IMsRdpClient8.DesktopHeight
- IMsRdpClient8.get_DesktopHeight
- IMsRdpClient8.put_DesktopHeight
- IMsRdpClient9.DesktopHeight
- IMsRdpClient9.get_DesktopHeight
- IMsRdpClient9.put_DesktopHeight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb75467b35703420ce49fd99ea032b139d721505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964505"
---
# <a name="imstscaxdesktopheight-property"></a><span data-ttu-id="656dd-124">IMsTscAx::D Proprietà esktopHeight</span><span class="sxs-lookup"><span data-stu-id="656dd-124">IMsTscAx::DesktopHeight property</span></span>

<span data-ttu-id="656dd-125">Specifica l'altezza, in pixel, del controllo corrente sul desktop remoto iniziale.</span><span class="sxs-lookup"><span data-stu-id="656dd-125">Specifies the current control's height, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="656dd-126">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="656dd-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="656dd-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="656dd-127">Syntax</span></span>


```C++
HRESULT put_DesktopHeight(
  [in]  LONG newVal
);

HRESULT get_DesktopHeight(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="656dd-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="656dd-128">Property value</span></span>

<span data-ttu-id="656dd-129">Nuova altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="656dd-129">The new height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="656dd-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="656dd-130">Error codes</span></span>

<span data-ttu-id="656dd-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="656dd-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="656dd-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="656dd-132">Remarks</span></span>

<span data-ttu-id="656dd-133">L'impostazione della proprietà **DesktopHeight** è facoltativa, ma deve essere impostata prima di chiamare il metodo [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="656dd-133">Setting the **DesktopHeight** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="656dd-134">Se non viene specificata un'altezza del desktop o è impostata su zero, l'altezza del desktop viene impostata sull'altezza del controllo.</span><span class="sxs-lookup"><span data-stu-id="656dd-134">If a desktop height is not specified, or is set to zero, the desktop height is set to the height of the control.</span></span> <span data-ttu-id="656dd-135">I valori minimo e massimo dipendono dalla versione del sistema operativo del client Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="656dd-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="656dd-136"><span id="_"></span>Windows 8/Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="656dd-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="656dd-137">200 minimo, 8192 massimo</span><span class="sxs-lookup"><span data-stu-id="656dd-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="656dd-138"><span id="_"></span>Windows 7/Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="656dd-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="656dd-139">200 minimo, 2048 massimo</span><span class="sxs-lookup"><span data-stu-id="656dd-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="656dd-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="656dd-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="656dd-141">200 minimo, 1200 massimo</span><span class="sxs-lookup"><span data-stu-id="656dd-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="656dd-142">Una volta stabilita una connessione, tutte le modifiche apportate all'altezza del controllo non modificano l'altezza del desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="656dd-142">After a connection is established, any changes to the control's height do not change the height of the remote desktop.</span></span> <span data-ttu-id="656dd-143">Al contrario, il controllo Visualizza le barre di scorrimento o Centra il desktop remoto, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="656dd-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="656dd-144">Per modificare le dimensioni del desktop di una connessione attiva, usare il metodo [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="656dd-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="656dd-145">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="656dd-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="656dd-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="656dd-146">Requirements</span></span>



| <span data-ttu-id="656dd-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="656dd-147">Requirement</span></span> | <span data-ttu-id="656dd-148">Valore</span><span class="sxs-lookup"><span data-stu-id="656dd-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="656dd-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="656dd-149">Minimum supported client</span></span><br/> | <span data-ttu-id="656dd-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="656dd-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="656dd-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="656dd-151">Minimum supported server</span></span><br/> | <span data-ttu-id="656dd-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="656dd-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="656dd-153">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="656dd-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="656dd-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="656dd-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="656dd-155">DLL</span><span class="sxs-lookup"><span data-stu-id="656dd-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="656dd-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="656dd-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="656dd-157">IID</span><span class="sxs-lookup"><span data-stu-id="656dd-157">IID</span></span><br/>                      | <span data-ttu-id="656dd-158">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="656dd-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="656dd-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="656dd-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656dd-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="656dd-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="656dd-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="656dd-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="656dd-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="656dd-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="656dd-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="656dd-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="656dd-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="656dd-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="656dd-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="656dd-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="656dd-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="656dd-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="656dd-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="656dd-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="656dd-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="656dd-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="656dd-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="656dd-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





