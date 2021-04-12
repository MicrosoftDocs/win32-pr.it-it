---
title: Proprietà ExtendedDisconnectReason di IMsRdpClient
description: Contiene informazioni estese sul motivo del controllo per la disconnessione.
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ExtendedDisconnectReason
- Servizi Desktop remoto proprietà ExtendedDisconnectReason, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà ExtendedDisconnectReason
- Servizi Desktop remoto proprietà ExtendedDisconnectReason, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà ExtendedDisconnectReason
- Servizi Desktop remoto proprietà ExtendedDisconnectReason, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà ExtendedDisconnectReason
- Servizi Desktop remoto proprietà ExtendedDisconnectReason, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà ExtendedDisconnectReason
- Servizi Desktop remoto proprietà ExtendedDisconnectReason, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà ExtendedDisconnectReason
- Servizi Desktop remoto proprietà ExtendedDisconnectReason, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà ExtendedDisconnectReason
- Servizi Desktop remoto proprietà ExtendedDisconnectReason, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà ExtendedDisconnectReason
- Servizi Desktop remoto proprietà ExtendedDisconnectReason, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà ExtendedDisconnectReason
- Servizi Desktop remoto proprietà ExtendedDisconnectReason, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà ExtendedDisconnectReason
- Servizi Desktop remoto proprietà ExtendedDisconnectReason, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà ExtendedDisconnectReason
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518838"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a><span data-ttu-id="c66d8-124">Proprietà IMsRdpClient:: ExtendedDisconnectReason</span><span class="sxs-lookup"><span data-stu-id="c66d8-124">IMsRdpClient::ExtendedDisconnectReason property</span></span>

<span data-ttu-id="c66d8-125">Contiene informazioni estese sul motivo del controllo per la disconnessione.</span><span class="sxs-lookup"><span data-stu-id="c66d8-125">Contains extended information about the control's reason for disconnection.</span></span>

<span data-ttu-id="c66d8-126">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c66d8-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c66d8-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c66d8-127">Syntax</span></span>


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a><span data-ttu-id="c66d8-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c66d8-128">Property value</span></span>

<span data-ttu-id="c66d8-129">Puntatore al valore [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) che indica il motivo della disconnessione del client.</span><span class="sxs-lookup"><span data-stu-id="c66d8-129">Pointer to the [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) value indicating the reason for disconnection of the client.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c66d8-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c66d8-130">Error codes</span></span>

<span data-ttu-id="c66d8-131">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="c66d8-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="c66d8-132">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="c66d8-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c66d8-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="c66d8-133">Remarks</span></span>

<span data-ttu-id="c66d8-134">Questo metodo viene in genere chiamato nel gestore eventi [**IMsTscAxEvents:: disconnected**](imstscaxevents-ondisconnected.md) per recuperare informazioni aggiuntive sull'evento di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="c66d8-134">Typically this method is called in the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) event handler to retrieve additional information about the disconnection event.</span></span>

<span data-ttu-id="c66d8-135">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c66d8-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c66d8-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c66d8-136">Requirements</span></span>



| <span data-ttu-id="c66d8-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c66d8-137">Requirement</span></span> | <span data-ttu-id="c66d8-138">Valore</span><span class="sxs-lookup"><span data-stu-id="c66d8-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c66d8-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c66d8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c66d8-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c66d8-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c66d8-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c66d8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c66d8-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c66d8-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c66d8-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c66d8-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="c66d8-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c66d8-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c66d8-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c66d8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c66d8-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c66d8-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c66d8-147">IID</span><span class="sxs-lookup"><span data-stu-id="c66d8-147">IID</span></span><br/>                      | <span data-ttu-id="c66d8-148">IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="c66d8-148">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c66d8-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c66d8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c66d8-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="c66d8-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="c66d8-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="c66d8-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="c66d8-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="c66d8-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="c66d8-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="c66d8-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="c66d8-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="c66d8-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="c66d8-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="c66d8-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="c66d8-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="c66d8-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="c66d8-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c66d8-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c66d8-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c66d8-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c66d8-159">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="c66d8-159">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="c66d8-160">**IMsTscAxEvents:: disconnected**</span><span class="sxs-lookup"><span data-stu-id="c66d8-160">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





