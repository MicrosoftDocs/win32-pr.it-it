---
title: Proprietà ClearTextPassword di IMsTscNonScriptable
description: Imposta la password del controllo ActiveX Desktop remoto in formato testo non crittografato.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà ClearTextPassword
- Servizi Desktop remoto proprietà ClearTextPassword, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà ClearTextPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743527"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a><span data-ttu-id="ebec6-124">Proprietà IMsTscNonScriptable:: ClearTextPassword</span><span class="sxs-lookup"><span data-stu-id="ebec6-124">IMsTscNonScriptable::ClearTextPassword property</span></span>

<span data-ttu-id="ebec6-125">Imposta la password del controllo ActiveX Desktop remoto in formato testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="ebec6-125">Sets the Remote Desktop ActiveX control password in plaintext format.</span></span>

<span data-ttu-id="ebec6-126">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="ebec6-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebec6-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebec6-127">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a><span data-ttu-id="ebec6-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ebec6-128">Property value</span></span>

<span data-ttu-id="ebec6-129">Password da utilizzare per la connessione, specificata in formato testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="ebec6-129">The password to be used to connect, specified in plaintext format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ebec6-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ebec6-130">Error codes</span></span>

<span data-ttu-id="ebec6-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="ebec6-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebec6-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebec6-132">Remarks</span></span>

<span data-ttu-id="ebec6-133">La password viene passata al server nel canale di comunicazione RDP crittografato in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="ebec6-133">The password is passed to the server in the safely encrypted RDP communications channel.</span></span> <span data-ttu-id="ebec6-134">Dopo aver impostato una password in testo non crittografato, non è possibile recuperarla in formato testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="ebec6-134">After a plaintext password is set, it cannot be retrieved in plaintext format.</span></span>

<span data-ttu-id="ebec6-135">La proprietà **ClearTextPassword** può essere impostata solo quando il controllo ActiveX Desktop remoto non è nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="ebec6-135">The **ClearTextPassword** property can only be set when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="ebec6-136">L'impostazione di questa proprietà ha esito negativo se il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="ebec6-136">Setting this property fails if the control is connected.</span></span> <span data-ttu-id="ebec6-137">Per verificare lo stato connesso, recuperare la proprietà [**IMsTscAx:: Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="ebec6-137">To check for the connected state, retrieve the [**IMsTscAx::Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="ebec6-138">È anche possibile chiamare questo metodo per impostare una password in testo non crittografato prima di convertirla in una password con codifica portatile o in una password con codifica binaria (non portabile).</span><span class="sxs-lookup"><span data-stu-id="ebec6-138">You can also call this method to set a plaintext password before converting it to either a portable encoded password or to a binary (nonportable) encoded password.</span></span> <span data-ttu-id="ebec6-139">Si noti tuttavia che le password codificate non devono essere considerate crittografate in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="ebec6-139">Note however that encoded passwords should not be considered securely encrypted.</span></span>

<span data-ttu-id="ebec6-140">Se si chiama per la prima volta questo metodo per impostare una password in formato testo non crittografato, è possibile convertire la password in formato codificato.</span><span class="sxs-lookup"><span data-stu-id="ebec6-140">If you first call this method to set a password in plaintext format, you can then convert the password to encoded format.</span></span>

<span data-ttu-id="ebec6-141">**Per convertire una password in testo non crittografato nel formato codificato**</span><span class="sxs-lookup"><span data-stu-id="ebec6-141">**To convert a plaintext password to encoded format**</span></span>

1.  <span data-ttu-id="ebec6-142">Impostare la password in formato testo non crittografato nella proprietà **ClearTextPassword** .</span><span class="sxs-lookup"><span data-stu-id="ebec6-142">Set the password in plaintext format in the **ClearTextPassword** property.</span></span>
2.  <span data-ttu-id="ebec6-143">Per recuperare la password in formato binario (non portabile), recuperare la proprietà [**BinaryPassword**](imstscnonscriptable-binarypassword.md) e le proprietà [**BinarySalt**](imstscnonscriptable-binarysalt.md) .</span><span class="sxs-lookup"><span data-stu-id="ebec6-143">To retrieve the password in binary (nonportable) encoded format, retrieve the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) property and the [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties.</span></span> <span data-ttu-id="ebec6-144">Sia la parte della password codificata che la parte Salt sono necessarie per impostare una password in formato con codifica binaria.</span><span class="sxs-lookup"><span data-stu-id="ebec6-144">Both the encoded password part and the salt part are required to set a password in binary encoded format.</span></span>
3.  <span data-ttu-id="ebec6-145">Per recuperare la password in formato con codifica portatile, recuperare il metodo [**PortablePassword**](imstscnonscriptable-portablepassword.md) e le proprietà [**PortableSalt**](imstscnonscriptable-portablesalt.md) .</span><span class="sxs-lookup"><span data-stu-id="ebec6-145">To retrieve the password in portable encoded format, retrieve the [**PortablePassword**](imstscnonscriptable-portablepassword.md) method and the [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="ebec6-146">Entrambe le parti sono necessarie per impostare una password in formato con codifica portatile.</span><span class="sxs-lookup"><span data-stu-id="ebec6-146">Both parts are required to set a password in portable encoded format.</span></span>

<span data-ttu-id="ebec6-147">Dopo aver seguito i tre passaggi precedenti, è possibile impostare la password in formato codificato impostando le proprietà [**BinaryPassword**](imstscnonscriptable-binarypassword.md) e [**BinarySalt**](imstscnonscriptable-binarysalt.md) o [**PortablePassword**](imstscnonscriptable-portablepassword.md) e [**PortableSalt**](imstscnonscriptable-portablesalt.md) .</span><span class="sxs-lookup"><span data-stu-id="ebec6-147">After following the preceding three steps, you can set the password in encoded format by setting the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) and [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties, or [**PortablePassword**](imstscnonscriptable-portablepassword.md) and [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="ebec6-148">Entrambe le parti sono obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="ebec6-148">Both parts are required.</span></span>

<span data-ttu-id="ebec6-149">Per abilitare l'accesso automatico, è necessario impostare anche il [**nome utente**](imstscax-username.md) e le proprietà del [**dominio**](imstscax-domain.md) .</span><span class="sxs-lookup"><span data-stu-id="ebec6-149">To enable automatic logon, you must also set the [**UserName**](imstscax-username.md) and [**Domain**](imstscax-domain.md) properties.</span></span> <span data-ttu-id="ebec6-150">Se la password non è in grado di autenticare l'utente, la finestra di dialogo di accesso di Windows viene visualizzata sul server per richiedere la password all'utente.</span><span class="sxs-lookup"><span data-stu-id="ebec6-150">If the password fails to authenticate the user, the Windows Logon dialog box is displayed at the server to prompt the user for the password.</span></span>

<span data-ttu-id="ebec6-151">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ebec6-151">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebec6-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebec6-152">Requirements</span></span>



| <span data-ttu-id="ebec6-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebec6-153">Requirement</span></span> | <span data-ttu-id="ebec6-154">Valore</span><span class="sxs-lookup"><span data-stu-id="ebec6-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebec6-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebec6-155">Minimum supported client</span></span><br/> | <span data-ttu-id="ebec6-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebec6-156">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ebec6-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebec6-157">Minimum supported server</span></span><br/> | <span data-ttu-id="ebec6-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebec6-158">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ebec6-159">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ebec6-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebec6-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebec6-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebec6-161">DLL</span><span class="sxs-lookup"><span data-stu-id="ebec6-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebec6-162"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebec6-162"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ebec6-163">IID</span><span class="sxs-lookup"><span data-stu-id="ebec6-163">IID</span></span><br/>                      | <span data-ttu-id="ebec6-164">IID \_ IMsTscNonScriptable è definito come c1e6743a-41C1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="ebec6-164">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebec6-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebec6-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebec6-166">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="ebec6-166">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="ebec6-167">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="ebec6-167">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="ebec6-168">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="ebec6-168">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="ebec6-169">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="ebec6-169">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="ebec6-170">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="ebec6-170">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="ebec6-171">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="ebec6-171">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





