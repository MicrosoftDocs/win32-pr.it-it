---
title: Proprietà PortablePassword di IMsTscNonScriptable
description: Questa proprietà non è più disponibile per l'utilizzo. | Proprietà PortablePassword di IMsTscNonScriptable
ms.assetid: 8d831ed3-1f4a-41a9-b283-507c5d9eea22
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PortablePassword
- Servizi Desktop remoto proprietà PortablePassword, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto, proprietà PortablePassword
- Servizi Desktop remoto proprietà PortablePassword, oggetto MsTscAx
- Oggetto MsTscAx Servizi Desktop remoto, proprietà PortablePassword
- Servizi Desktop remoto proprietà PortablePassword, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto, proprietà PortablePassword
- Servizi Desktop remoto proprietà PortablePassword, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, proprietà PortablePassword
- Servizi Desktop remoto proprietà PortablePassword, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà PortablePassword
- Servizi Desktop remoto proprietà PortablePassword, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà PortablePassword
- Servizi Desktop remoto proprietà PortablePassword, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà PortablePassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortablePassword
- IMsTscNonScriptable.get_PortablePassword
- IMsTscNonScriptable.put_PortablePassword
- MsTscAx.PortablePassword
- IMsRdpClientNonScriptable.PortablePassword
- IMsRdpClientNonScriptable.get_PortablePassword
- IMsRdpClientNonScriptable.put_PortablePassword
- IMsRdpClientNonScriptable2.PortablePassword
- IMsRdpClientNonScriptable2.get_PortablePassword
- IMsRdpClientNonScriptable2.put_PortablePassword
- IMsRdpClientNonScriptable3.PortablePassword
- IMsRdpClientNonScriptable3.get_PortablePassword
- IMsRdpClientNonScriptable3.put_PortablePassword
- IMsRdpClientNonScriptable4.PortablePassword
- IMsRdpClientNonScriptable4.get_PortablePassword
- IMsRdpClientNonScriptable4.put_PortablePassword
- IMsRdpClientNonScriptable5.PortablePassword
- IMsRdpClientNonScriptable5.get_PortablePassword
- IMsRdpClientNonScriptable5.put_PortablePassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5259e83087287395e6114bb8ffe3eb7e859ab52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321462"
---
# <a name="imstscnonscriptableportablepassword-property"></a><span data-ttu-id="845d4-119">IMsTscNonScriptable::P proprietà ortablePassword</span><span class="sxs-lookup"><span data-stu-id="845d4-119">IMsTscNonScriptable::PortablePassword property</span></span>

<span data-ttu-id="845d4-120">Questa proprietà non è più disponibile per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="845d4-120">This property is no longer available for use.</span></span>

<span data-ttu-id="845d4-121">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="845d4-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="845d4-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="845d4-122">Syntax</span></span>


```C++
HRESULT put_PortablePassword(
  [in]  BSTR newPortablePassVal
);

HRESULT get_PortablePassword(
  [out] BSTR *pPortablePass
);
```



## <a name="property-value"></a><span data-ttu-id="845d4-123">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="845d4-123">Property value</span></span>

<span data-ttu-id="845d4-124">Nuova parte della password, in formato con codifica portatile.</span><span class="sxs-lookup"><span data-stu-id="845d4-124">The new password part, in portable encoded format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="845d4-125">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="845d4-125">Error codes</span></span>

<span data-ttu-id="845d4-126">Restituisce **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="845d4-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="845d4-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="845d4-127">Requirements</span></span>



| <span data-ttu-id="845d4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="845d4-128">Requirement</span></span> | <span data-ttu-id="845d4-129">Valore</span><span class="sxs-lookup"><span data-stu-id="845d4-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="845d4-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="845d4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="845d4-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="845d4-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="845d4-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="845d4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="845d4-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="845d4-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="845d4-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="845d4-134">End of client support</span></span><br/>    | <span data-ttu-id="845d4-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="845d4-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="845d4-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="845d4-136">End of server support</span></span><br/>    | <span data-ttu-id="845d4-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="845d4-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="845d4-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="845d4-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="845d4-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="845d4-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="845d4-140">DLL</span><span class="sxs-lookup"><span data-stu-id="845d4-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="845d4-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="845d4-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="845d4-142">IID</span><span class="sxs-lookup"><span data-stu-id="845d4-142">IID</span></span><br/>                      | <span data-ttu-id="845d4-143">IID \_ IMsTscNonScriptable è definito come c1e6743a-41C1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="845d4-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="845d4-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="845d4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="845d4-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="845d4-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="845d4-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="845d4-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="845d4-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="845d4-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="845d4-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="845d4-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="845d4-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="845d4-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="845d4-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="845d4-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





