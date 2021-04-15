---
title: Proprietà della versione IMsTscAx
description: Specifica il numero di versione del controllo corrente.
ms.assetid: 91ddeb4c-9d61-41e7-af96-95b0c4884682
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà Version
- Servizi Desktop remoto della proprietà Version, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà Version
topic_type:
- apiref
api_name:
- IMsTscAx.Version
- IMsTscAx.get_Version
- IMsRdpClient.Version
- IMsRdpClient.get_Version
- IMsRdpClient2.Version
- IMsRdpClient2.get_Version
- IMsRdpClient3.Version
- IMsRdpClient3.get_Version
- IMsRdpClient4.Version
- IMsRdpClient4.get_Version
- IMsRdpClient5.Version
- IMsRdpClient5.get_Version
- IMsRdpClient6.Version
- IMsRdpClient6.get_Version
- IMsRdpClient7.Version
- IMsRdpClient7.get_Version
- IMsRdpClient8.Version
- IMsRdpClient8.get_Version
- IMsRdpClient9.Version
- IMsRdpClient9.get_Version
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff25f274d1f076c9c4119648ccb9cc6d82f43b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476738"
---
# <a name="imstscaxversion-property"></a><span data-ttu-id="68b29-124">Proprietà IMsTscAx:: Version</span><span class="sxs-lookup"><span data-stu-id="68b29-124">IMsTscAx::Version property</span></span>

<span data-ttu-id="68b29-125">Specifica il numero di versione del controllo corrente.</span><span class="sxs-lookup"><span data-stu-id="68b29-125">Specifies the version number of the current control.</span></span>

<span data-ttu-id="68b29-126">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="68b29-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b29-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68b29-127">Syntax</span></span>


```C++
HRESULT get_Version(
  [out] BSTR *pVersion
);
```



## <a name="property-value"></a><span data-ttu-id="68b29-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="68b29-128">Property value</span></span>

<span data-ttu-id="68b29-129">Numero di versione.</span><span class="sxs-lookup"><span data-stu-id="68b29-129">The version number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68b29-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="68b29-130">Error codes</span></span>

<span data-ttu-id="68b29-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="68b29-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="68b29-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="68b29-132">Remarks</span></span>

<span data-ttu-id="68b29-133">Questo metodo alloca la memoria necessaria per il buffer a cui punta il parametro *pVersion* .</span><span class="sxs-lookup"><span data-stu-id="68b29-133">This method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="68b29-134">La chiamata di applicazioni C/C++ deve liberare la memoria con una chiamata alla funzione [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="68b29-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="68b29-135">Questa operazione non è necessaria per Visual Basic e client di scripting.</span><span class="sxs-lookup"><span data-stu-id="68b29-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="68b29-136">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="68b29-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68b29-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68b29-137">Requirements</span></span>



| <span data-ttu-id="68b29-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b29-138">Requirement</span></span> | <span data-ttu-id="68b29-139">Valore</span><span class="sxs-lookup"><span data-stu-id="68b29-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68b29-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68b29-140">Minimum supported client</span></span><br/> | <span data-ttu-id="68b29-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68b29-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="68b29-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68b29-142">Minimum supported server</span></span><br/> | <span data-ttu-id="68b29-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68b29-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="68b29-144">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="68b29-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="68b29-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68b29-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68b29-146">DLL</span><span class="sxs-lookup"><span data-stu-id="68b29-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68b29-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68b29-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68b29-148">IID</span><span class="sxs-lookup"><span data-stu-id="68b29-148">IID</span></span><br/>                      | <span data-ttu-id="68b29-149">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="68b29-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="68b29-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68b29-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b29-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="68b29-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="68b29-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="68b29-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="68b29-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="68b29-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="68b29-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="68b29-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="68b29-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="68b29-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="68b29-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="68b29-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="68b29-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="68b29-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="68b29-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="68b29-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="68b29-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="68b29-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="68b29-160">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="68b29-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

