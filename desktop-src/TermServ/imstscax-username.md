---
title: Proprietà nome utente IMsTscAx
description: Specifica le credenziali di accesso al nome utente.
ms.assetid: 9be25003-b9aa-41bb-a5a9-512546175114
ms.tgt_platform: multiple
keywords:
- Proprietà UserName Servizi Desktop remoto
- Servizi Desktop remoto proprietà UserName, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà UserName
- Servizi Desktop remoto proprietà UserName, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà UserName
- Servizi Desktop remoto proprietà UserName, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà UserName
- Servizi Desktop remoto proprietà UserName, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà UserName
- Servizi Desktop remoto proprietà UserName, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà UserName
- Servizi Desktop remoto proprietà UserName, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà UserName
- Servizi Desktop remoto proprietà UserName, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà UserName
- Servizi Desktop remoto proprietà UserName, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà UserName
- Servizi Desktop remoto proprietà UserName, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà UserName
- Servizi Desktop remoto proprietà UserName, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà UserName
topic_type:
- apiref
api_name:
- IMsTscAx.UserName
- IMsTscAx.get_UserName
- IMsTscAx.put_UserName
- IMsRdpClient.UserName
- IMsRdpClient.get_UserName
- IMsRdpClient.put_UserName
- IMsRdpClient2.UserName
- IMsRdpClient2.get_UserName
- IMsRdpClient2.put_UserName
- IMsRdpClient3.UserName
- IMsRdpClient3.get_UserName
- IMsRdpClient3.put_UserName
- IMsRdpClient4.UserName
- IMsRdpClient4.get_UserName
- IMsRdpClient4.put_UserName
- IMsRdpClient5.UserName
- IMsRdpClient5.get_UserName
- IMsRdpClient5.put_UserName
- IMsRdpClient6.UserName
- IMsRdpClient6.get_UserName
- IMsRdpClient6.put_UserName
- IMsRdpClient7.UserName
- IMsRdpClient7.get_UserName
- IMsRdpClient7.put_UserName
- IMsRdpClient8.UserName
- IMsRdpClient8.get_UserName
- IMsRdpClient8.put_UserName
- IMsRdpClient9.UserName
- IMsRdpClient9.get_UserName
- IMsRdpClient9.put_UserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a94a7f7d9fe5d6532de55f36a50094205fe1d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479030"
---
# <a name="imstscaxusername-property"></a><span data-ttu-id="bf32d-124">Proprietà IMsTscAx:: UserName</span><span class="sxs-lookup"><span data-stu-id="bf32d-124">IMsTscAx::UserName property</span></span>

<span data-ttu-id="bf32d-125">Specifica le credenziali di accesso al nome utente.</span><span class="sxs-lookup"><span data-stu-id="bf32d-125">Specifies the user name logon credential.</span></span>

<span data-ttu-id="bf32d-126">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="bf32d-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf32d-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf32d-127">Syntax</span></span>


```C++
HRESULT put_UserName(
  [in]  BSTR newVal
);

HRESULT get_UserName(
  [out] BSTR *pUserName
);
```



## <a name="property-value"></a><span data-ttu-id="bf32d-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bf32d-128">Property value</span></span>

<span data-ttu-id="bf32d-129">Nuovo nome utente.</span><span class="sxs-lookup"><span data-stu-id="bf32d-129">The new user name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bf32d-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="bf32d-130">Error codes</span></span>

<span data-ttu-id="bf32d-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="bf32d-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf32d-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf32d-132">Remarks</span></span>

<span data-ttu-id="bf32d-133">L'impostazione della proprietà **username** è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="bf32d-133">Setting the **UserName** property is optional.</span></span> <span data-ttu-id="bf32d-134">Se non viene specificato, l'utente può specificare un nome utente quando viene visualizzata la finestra di dialogo di accesso di Windows durante la connessione.</span><span class="sxs-lookup"><span data-stu-id="bf32d-134">If it is not specified, the user can provide a user name when the Windows Logon dialog box appears during connection.</span></span>

<span data-ttu-id="bf32d-135">Questa proprietà può essere impostata solo se il controllo non è nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="bf32d-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="bf32d-136">Restituisce **e ha \_ esito negativo** se viene chiamato quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="bf32d-136">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="bf32d-137">È possibile verificare se il controllo è connesso rispondendo agli eventi di connessione in [**IMsTscAxEvents**](imstscaxevents-interface.md) o esaminando la proprietà [**connessa**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="bf32d-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="bf32d-138">Il metodo della proprietà **get \_ username** alloca la memoria necessaria per il buffer a cui punta il parametro *pVersion* .</span><span class="sxs-lookup"><span data-stu-id="bf32d-138">The **get\_UserName** property method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="bf32d-139">La chiamata di applicazioni C/C++ deve liberare la memoria con una chiamata alla funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="bf32d-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="bf32d-140">Questa operazione non è necessaria per Visual Basic e client di scripting.</span><span class="sxs-lookup"><span data-stu-id="bf32d-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="bf32d-141">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bf32d-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf32d-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf32d-142">Requirements</span></span>



| <span data-ttu-id="bf32d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf32d-143">Requirement</span></span> | <span data-ttu-id="bf32d-144">Valore</span><span class="sxs-lookup"><span data-stu-id="bf32d-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf32d-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf32d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bf32d-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf32d-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bf32d-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf32d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bf32d-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf32d-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bf32d-149">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bf32d-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf32d-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf32d-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf32d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="bf32d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf32d-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf32d-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf32d-153">IID</span><span class="sxs-lookup"><span data-stu-id="bf32d-153">IID</span></span><br/>                      | <span data-ttu-id="bf32d-154">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="bf32d-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bf32d-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf32d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf32d-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="bf32d-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="bf32d-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="bf32d-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="bf32d-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="bf32d-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="bf32d-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="bf32d-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="bf32d-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="bf32d-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="bf32d-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="bf32d-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="bf32d-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="bf32d-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="bf32d-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="bf32d-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="bf32d-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="bf32d-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="bf32d-165">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="bf32d-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

