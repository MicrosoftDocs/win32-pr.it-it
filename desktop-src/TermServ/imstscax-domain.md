---
title: Proprietà di dominio IMsTscAx
description: Specifica il dominio a cui l'utente corrente esegue l'accesso.
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà di dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà del dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà del dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà del dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà del dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà del dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà del dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà del dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà del dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà del dominio
- Servizi Desktop remoto di proprietà del dominio, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà del dominio
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf95c02de10fe8db38a53b75d4d20cf796020f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964815"
---
# <a name="imstscaxdomain-property"></a><span data-ttu-id="40d0c-124">IMsTscAx::D Proprietà ominio</span><span class="sxs-lookup"><span data-stu-id="40d0c-124">IMsTscAx::Domain property</span></span>

<span data-ttu-id="40d0c-125">Specifica il dominio a cui l'utente corrente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="40d0c-125">Specifies the domain to which the current user logs on.</span></span>

<span data-ttu-id="40d0c-126">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="40d0c-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d0c-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40d0c-127">Syntax</span></span>


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a><span data-ttu-id="40d0c-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="40d0c-128">Property value</span></span>

<span data-ttu-id="40d0c-129">Nuovo nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="40d0c-129">The new domain name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="40d0c-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="40d0c-130">Error codes</span></span>

<span data-ttu-id="40d0c-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="40d0c-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="40d0c-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="40d0c-132">Remarks</span></span>

<span data-ttu-id="40d0c-133">L'impostazione della proprietà del **dominio** è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="40d0c-133">Setting the **Domain** property is optional.</span></span> <span data-ttu-id="40d0c-134">Se non è impostata, l'utente può scegliere un dominio quando viene visualizzata la finestra di dialogo di accesso di Windows durante la connessione.</span><span class="sxs-lookup"><span data-stu-id="40d0c-134">If it is not set, the user can choose a domain when the Windows Logon dialog box appears during the connection.</span></span>

<span data-ttu-id="40d0c-135">Il metodo **get \_ Domain** alloca la memoria necessaria per il buffer a cui punta il parametro *pDomain* .</span><span class="sxs-lookup"><span data-stu-id="40d0c-135">The **get\_Domain** method allocates the memory required for the buffer pointed to by the *pDomain* parameter.</span></span> <span data-ttu-id="40d0c-136">La chiamata di applicazioni C/C++ deve liberare la memoria con una chiamata alla funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="40d0c-136">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="40d0c-137">Questa operazione non è necessaria per Visual Basic e client di scripting.</span><span class="sxs-lookup"><span data-stu-id="40d0c-137">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="40d0c-138">Questa proprietà può essere impostata solo se il controllo non è nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="40d0c-138">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="40d0c-139">Restituisce **e ha \_ esito negativo** se viene chiamato quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="40d0c-139">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="40d0c-140">È possibile verificare se il controllo è connesso rispondendo agli eventi di connessione in [**IMsTscAxEvents**](imstscaxevents-interface.md) o esaminando la proprietà [**connessa**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="40d0c-140">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="40d0c-141">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="40d0c-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40d0c-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40d0c-142">Requirements</span></span>



| <span data-ttu-id="40d0c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="40d0c-143">Requirement</span></span> | <span data-ttu-id="40d0c-144">Valore</span><span class="sxs-lookup"><span data-stu-id="40d0c-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40d0c-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40d0c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="40d0c-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40d0c-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="40d0c-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40d0c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="40d0c-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40d0c-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="40d0c-149">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="40d0c-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="40d0c-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d0c-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="40d0c-151">DLL</span><span class="sxs-lookup"><span data-stu-id="40d0c-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40d0c-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d0c-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="40d0c-153">IID</span><span class="sxs-lookup"><span data-stu-id="40d0c-153">IID</span></span><br/>                      | <span data-ttu-id="40d0c-154">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="40d0c-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="40d0c-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40d0c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d0c-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="40d0c-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="40d0c-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="40d0c-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="40d0c-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="40d0c-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="40d0c-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="40d0c-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="40d0c-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="40d0c-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="40d0c-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="40d0c-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="40d0c-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="40d0c-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="40d0c-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="40d0c-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="40d0c-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="40d0c-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="40d0c-165">**Connesso**</span><span class="sxs-lookup"><span data-stu-id="40d0c-165">**Connected**</span></span>](imstscax-connected.md)
</dt> <dt>

[<span data-ttu-id="40d0c-166">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="40d0c-166">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="40d0c-167">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="40d0c-167">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

