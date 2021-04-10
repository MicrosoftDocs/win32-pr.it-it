---
title: Proprietà IMsRdpClient FullScreen
description: Determina se il controllo client è in modalità schermo intero.
ms.assetid: 64fe2835-c00e-4d21-812d-dcf160147d93
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà a schermo intero
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà FullScreen
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà FullScreen
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà FullScreen
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà FullScreen
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà FullScreen
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà FullScreen
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà FullScreen
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà FullScreen
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà FullScreen
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà FullScreen
topic_type:
- apiref
api_name:
- IMsRdpClient.FullScreen
- IMsRdpClient.get_FullScreen
- IMsRdpClient.put_FullScreen
- IMsRdpClient2.FullScreen
- IMsRdpClient2.get_FullScreen
- IMsRdpClient2.put_FullScreen
- IMsRdpClient3.FullScreen
- IMsRdpClient3.get_FullScreen
- IMsRdpClient3.put_FullScreen
- IMsRdpClient4.FullScreen
- IMsRdpClient4.get_FullScreen
- IMsRdpClient4.put_FullScreen
- IMsRdpClient5.FullScreen
- IMsRdpClient5.get_FullScreen
- IMsRdpClient5.put_FullScreen
- IMsRdpClient6.FullScreen
- IMsRdpClient6.get_FullScreen
- IMsRdpClient6.put_FullScreen
- IMsRdpClient7.FullScreen
- IMsRdpClient7.get_FullScreen
- IMsRdpClient7.put_FullScreen
- IMsRdpClient8.FullScreen
- IMsRdpClient8.get_FullScreen
- IMsRdpClient8.put_FullScreen
- IMsRdpClient9.FullScreen
- IMsRdpClient9.get_FullScreen
- IMsRdpClient9.put_FullScreen
- IMsRdpClient10.FullScreen
- IMsRdpClient10.get_FullScreen
- IMsRdpClient10.put_FullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adbc8e11d2cc4fb4a8071372777a01d81b5edad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121234"
---
# <a name="imsrdpclientfullscreen-property"></a><span data-ttu-id="67a58-124">Proprietà IMsRdpClient:: FullScreen</span><span class="sxs-lookup"><span data-stu-id="67a58-124">IMsRdpClient::FullScreen property</span></span>

<span data-ttu-id="67a58-125">Determina se il controllo client è in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="67a58-125">Determines whether the client control is in full-screen mode.</span></span>

<span data-ttu-id="67a58-126">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="67a58-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a58-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67a58-127">Syntax</span></span>


```C++
HRESULT put_FullScreen(
  [in]  VARIANT_BOOL fFullScreen
);

HRESULT get_FullScreen(
  [out] VARIANT_BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="67a58-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="67a58-128">Property value</span></span>

<span data-ttu-id="67a58-129">**True** per attivare la modalità schermo intero, **false** per uscire dalla modalità a schermo intero e tornare alla modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="67a58-129">**True** to enter full-screen mode, **False** to leave full-screen mode and return to window mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="67a58-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="67a58-130">Error codes</span></span>

<span data-ttu-id="67a58-131">Se i metodi hanno esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="67a58-131">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="67a58-132">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="67a58-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="67a58-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="67a58-133">Remarks</span></span>

<span data-ttu-id="67a58-134">È possibile impostare questa proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="67a58-134">You can set this property when the control is connected.</span></span>

<span data-ttu-id="67a58-135">È necessario chiamare il metodo [**IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) prima di chiamare il metodo [**IMsTscSecuredSettings::P UT \_ FullScreen**](imstscsecuredsettings-fullscreen.md) o **IMsRdpClient::p UT \_ FullScreen** .</span><span class="sxs-lookup"><span data-stu-id="67a58-135">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the **IMsRdpClient::put\_Fullscreen** method.</span></span>

<span data-ttu-id="67a58-136">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="67a58-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67a58-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67a58-137">Requirements</span></span>



| <span data-ttu-id="67a58-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="67a58-138">Requirement</span></span> | <span data-ttu-id="67a58-139">Valore</span><span class="sxs-lookup"><span data-stu-id="67a58-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67a58-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67a58-140">Minimum supported client</span></span><br/> | <span data-ttu-id="67a58-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67a58-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="67a58-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67a58-142">Minimum supported server</span></span><br/> | <span data-ttu-id="67a58-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67a58-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="67a58-144">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="67a58-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="67a58-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67a58-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="67a58-146">DLL</span><span class="sxs-lookup"><span data-stu-id="67a58-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67a58-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67a58-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="67a58-148">IID</span><span class="sxs-lookup"><span data-stu-id="67a58-148">IID</span></span><br/>                      | <span data-ttu-id="67a58-149">IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="67a58-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="67a58-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67a58-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a58-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="67a58-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="67a58-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="67a58-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="67a58-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="67a58-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="67a58-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="67a58-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="67a58-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="67a58-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="67a58-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="67a58-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="67a58-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="67a58-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="67a58-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="67a58-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="67a58-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="67a58-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="67a58-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="67a58-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





