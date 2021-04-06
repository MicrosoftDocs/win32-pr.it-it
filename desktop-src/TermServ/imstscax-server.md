---
title: Proprietà del server IMsTscAx (Asptlb. h)
description: Specifica il nome del server a cui è connesso il controllo corrente.
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà server
- Servizi Desktop remoto proprietà server, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà server
- Servizi Desktop remoto proprietà server, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà server
- Servizi Desktop remoto proprietà server, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà server
- Servizi Desktop remoto proprietà server, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà server
- Servizi Desktop remoto proprietà server, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà server
- Servizi Desktop remoto proprietà server, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà server
- Servizi Desktop remoto proprietà server, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà server
- Servizi Desktop remoto proprietà server, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà server
- Servizi Desktop remoto proprietà server, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà server
- Servizi Desktop remoto proprietà server, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà server
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7be04c149e2ac10c1a3e905678bd2b5f663cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963841"
---
# <a name="imstscaxserver-property"></a><span data-ttu-id="0dc36-124">Proprietà IMsTscAx:: Server</span><span class="sxs-lookup"><span data-stu-id="0dc36-124">IMsTscAx::Server property</span></span>

<span data-ttu-id="0dc36-125">Specifica il nome del server a cui è connesso il controllo corrente.</span><span class="sxs-lookup"><span data-stu-id="0dc36-125">Specifies the name of the server to which the current control is connected.</span></span>

<span data-ttu-id="0dc36-126">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0dc36-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc36-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0dc36-127">Syntax</span></span>


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a><span data-ttu-id="0dc36-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0dc36-128">Property value</span></span>

<span data-ttu-id="0dc36-129">Nome del nuovo server.</span><span class="sxs-lookup"><span data-stu-id="0dc36-129">The new server name.</span></span> <span data-ttu-id="0dc36-130">Questo parametro può essere un nome DNS o un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="0dc36-130">This parameter can be a DNS name or IP address.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0dc36-131">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0dc36-131">Error codes</span></span>

<span data-ttu-id="0dc36-132">Se i metodi hanno esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="0dc36-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="0dc36-133">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="0dc36-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc36-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="0dc36-134">Remarks</span></span>

<span data-ttu-id="0dc36-135">Questa proprietà deve essere impostata prima di chiamare il metodo [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0dc36-135">This property must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="0dc36-136">Si tratta dell'unica proprietà che è necessario impostare prima della connessione.</span><span class="sxs-lookup"><span data-stu-id="0dc36-136">It is the only property that must be set before connecting.</span></span>

<span data-ttu-id="0dc36-137">Questa proprietà può essere impostata solo se il controllo non è nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="0dc36-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="0dc36-138">Questa proprietà restituisce **E ha \_ esito negativo** se viene chiamata quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="0dc36-138">This property returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="0dc36-139">È possibile verificare lo stato connesso usando la proprietà [**connessa**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="0dc36-139">You can check for the connected state by using the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="0dc36-140">Questo metodo alloca la memoria necessaria per il buffer a cui punta il parametro *pServer* .</span><span class="sxs-lookup"><span data-stu-id="0dc36-140">This method allocates the memory required for the buffer pointed to by the *pServer* parameter.</span></span> <span data-ttu-id="0dc36-141">La chiamata di applicazioni C/C++ deve liberare la memoria con una chiamata alla funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="0dc36-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="0dc36-142">Questa operazione non è necessaria per Visual Basic e client di scripting.</span><span class="sxs-lookup"><span data-stu-id="0dc36-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="0dc36-143">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0dc36-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc36-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dc36-144">Requirements</span></span>



| <span data-ttu-id="0dc36-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dc36-145">Requirement</span></span> | <span data-ttu-id="0dc36-146">Valore</span><span class="sxs-lookup"><span data-stu-id="0dc36-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc36-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0dc36-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0dc36-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0dc36-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0dc36-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0dc36-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0dc36-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0dc36-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0dc36-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0dc36-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dc36-152"><dt>Asptlb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dc36-152"><dt>Asptlb.h</dt></span></span> </dl>    |
| <span data-ttu-id="0dc36-153">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0dc36-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="0dc36-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dc36-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0dc36-155">DLL</span><span class="sxs-lookup"><span data-stu-id="0dc36-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dc36-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dc36-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0dc36-157">IID</span><span class="sxs-lookup"><span data-stu-id="0dc36-157">IID</span></span><br/>                      | <span data-ttu-id="0dc36-158">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="0dc36-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0dc36-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dc36-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc36-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="0dc36-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0dc36-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0dc36-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0dc36-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0dc36-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0dc36-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0dc36-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0dc36-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0dc36-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0dc36-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0dc36-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0dc36-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0dc36-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0dc36-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0dc36-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0dc36-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0dc36-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0dc36-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="0dc36-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

