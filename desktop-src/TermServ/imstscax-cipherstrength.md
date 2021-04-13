---
title: Proprietà CipherStrength di IMsTscAx
description: Recupera l'attendibilità massima della crittografia del controllo corrente.
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà CipherStrength
- Servizi Desktop remoto proprietà CipherStrength, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà CipherStrength
- Servizi Desktop remoto proprietà CipherStrength, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà CipherStrength
- Servizi Desktop remoto proprietà CipherStrength, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà CipherStrength
- Servizi Desktop remoto proprietà CipherStrength, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà CipherStrength
- Servizi Desktop remoto proprietà CipherStrength, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà CipherStrength
- Servizi Desktop remoto proprietà CipherStrength, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà CipherStrength
- Servizi Desktop remoto proprietà CipherStrength, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà CipherStrength
- Servizi Desktop remoto proprietà CipherStrength, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà CipherStrength
- Servizi Desktop remoto proprietà CipherStrength, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà CipherStrength
- Servizi Desktop remoto proprietà CipherStrength, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà CipherStrength
topic_type:
- apiref
api_name:
- IMsTscAx.CipherStrength
- IMsTscAx.get_CipherStrength
- IMsRdpClient.CipherStrength
- IMsRdpClient.get_CipherStrength
- IMsRdpClient2.CipherStrength
- IMsRdpClient2.get_CipherStrength
- IMsRdpClient3.CipherStrength
- IMsRdpClient3.get_CipherStrength
- IMsRdpClient4.CipherStrength
- IMsRdpClient4.get_CipherStrength
- IMsRdpClient5.CipherStrength
- IMsRdpClient5.get_CipherStrength
- IMsRdpClient6.CipherStrength
- IMsRdpClient6.get_CipherStrength
- IMsRdpClient7.CipherStrength
- IMsRdpClient7.get_CipherStrength
- IMsRdpClient8.CipherStrength
- IMsRdpClient8.get_CipherStrength
- IMsRdpClient9.CipherStrength
- IMsRdpClient9.get_CipherStrength
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401cf3796d349aaa6764eae46a371a9d485f763c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400311"
---
# <a name="imstscaxcipherstrength-property"></a><span data-ttu-id="3e18a-124">Proprietà IMsTscAx:: CipherStrength</span><span class="sxs-lookup"><span data-stu-id="3e18a-124">IMsTscAx::CipherStrength property</span></span>

<span data-ttu-id="3e18a-125">Recupera l'attendibilità massima della crittografia del controllo corrente.</span><span class="sxs-lookup"><span data-stu-id="3e18a-125">Retrieves the maximum encryption strength of the current control.</span></span>

<span data-ttu-id="3e18a-126">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3e18a-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e18a-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e18a-127">Syntax</span></span>


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a><span data-ttu-id="3e18a-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3e18a-128">Property value</span></span>

<span data-ttu-id="3e18a-129">Livello di crittografia.</span><span class="sxs-lookup"><span data-stu-id="3e18a-129">The encryption strength.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e18a-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="3e18a-130">Error codes</span></span>

<span data-ttu-id="3e18a-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="3e18a-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e18a-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e18a-132">Remarks</span></span>

<span data-ttu-id="3e18a-133">Per Connessione Web Desktop remoto, il livello di codifica è sempre 128 perché il controllo ActiveX Desktop remoto supporta la crittografia fino a 128 bit compresi.</span><span class="sxs-lookup"><span data-stu-id="3e18a-133">For Remote Desktop Web Connection, the cipher strength is always 128 because the Remote Desktop ActiveX control supports encryption up to and including 128 bits.</span></span> <span data-ttu-id="3e18a-134">Il controllo a 128 bit può comunque connettersi 56 ai server host sessione Desktop remoto crittografia di bit (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="3e18a-134">The 128-bit control can still connect to 56 bit encryption Remote Desktop Session Host (RD Session Host) servers.</span></span>

<span data-ttu-id="3e18a-135">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3e18a-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e18a-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e18a-136">Requirements</span></span>



| <span data-ttu-id="3e18a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e18a-137">Requirement</span></span> | <span data-ttu-id="3e18a-138">Valore</span><span class="sxs-lookup"><span data-stu-id="3e18a-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e18a-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e18a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3e18a-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e18a-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3e18a-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e18a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3e18a-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e18a-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3e18a-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3e18a-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e18a-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e18a-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e18a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3e18a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e18a-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e18a-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e18a-147">IID</span><span class="sxs-lookup"><span data-stu-id="3e18a-147">IID</span></span><br/>                      | <span data-ttu-id="3e18a-148">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="3e18a-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="3e18a-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e18a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e18a-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="3e18a-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="3e18a-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="3e18a-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="3e18a-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="3e18a-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="3e18a-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="3e18a-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="3e18a-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="3e18a-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="3e18a-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="3e18a-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="3e18a-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="3e18a-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="3e18a-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="3e18a-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="3e18a-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="3e18a-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="3e18a-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="3e18a-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





