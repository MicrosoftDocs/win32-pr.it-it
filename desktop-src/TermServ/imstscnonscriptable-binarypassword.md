---
title: Proprietà BinaryPassword di IMsTscNonScriptable
description: Questa proprietà non è più disponibile per l'utilizzo. | Proprietà BinaryPassword di IMsTscNonScriptable
ms.assetid: b3be7323-a75f-4ec2-9d58-e8ff3338d6ff
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, oggetto MsTscAx
- Oggetto MsTscAx Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà BinaryPassword
- Servizi Desktop remoto proprietà BinaryPassword, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà BinaryPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinaryPassword
- IMsTscNonScriptable.get_BinaryPassword
- IMsTscNonScriptable.put_BinaryPassword
- MsTscAx.BinaryPassword
- IMsRdpClientNonScriptable.BinaryPassword
- IMsRdpClientNonScriptable.get_BinaryPassword
- IMsRdpClientNonScriptable.put_BinaryPassword
- IMsRdpClientNonScriptable2.BinaryPassword
- IMsRdpClientNonScriptable2.get_BinaryPassword
- IMsRdpClientNonScriptable2.put_BinaryPassword
- IMsRdpClientNonScriptable3.BinaryPassword
- IMsRdpClientNonScriptable3.get_BinaryPassword
- IMsRdpClientNonScriptable3.put_BinaryPassword
- IMsRdpClientNonScriptable4.BinaryPassword
- IMsRdpClientNonScriptable4.get_BinaryPassword
- IMsRdpClientNonScriptable4.put_BinaryPassword
- IMsRdpClientNonScriptable5.BinaryPassword
- IMsRdpClientNonScriptable5.get_BinaryPassword
- IMsRdpClientNonScriptable5.put_BinaryPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d6eab2a3902968ef4d4c953a8da8b9c884a497
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321325"
---
# <a name="imstscnonscriptablebinarypassword-property"></a><span data-ttu-id="4f2f2-119">Proprietà IMsTscNonScriptable:: BinaryPassword</span><span class="sxs-lookup"><span data-stu-id="4f2f2-119">IMsTscNonScriptable::BinaryPassword property</span></span>

<span data-ttu-id="4f2f2-120">Questa proprietà non è più disponibile per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="4f2f2-120">This property is no longer available for use.</span></span>

<span data-ttu-id="4f2f2-121">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4f2f2-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f2f2-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f2f2-122">Syntax</span></span>


```C++
HRESULT put_BinaryPassword(
  [in]  BSTR newPassword
);

HRESULT get_BinaryPassword(
  [out] BSTR *pBinaryPassword
);
```



## <a name="property-value"></a><span data-ttu-id="4f2f2-123">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4f2f2-123">Property value</span></span>

<span data-ttu-id="4f2f2-124">Nuova parte della password, in formato con codifica binaria.</span><span class="sxs-lookup"><span data-stu-id="4f2f2-124">The new password part, in binary encoded format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f2f2-125">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4f2f2-125">Error codes</span></span>

<span data-ttu-id="4f2f2-126">Restituisce **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="4f2f2-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f2f2-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f2f2-127">Requirements</span></span>



| <span data-ttu-id="4f2f2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f2f2-128">Requirement</span></span> | <span data-ttu-id="4f2f2-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4f2f2-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f2f2-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f2f2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4f2f2-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4f2f2-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4f2f2-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f2f2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4f2f2-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4f2f2-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4f2f2-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4f2f2-134">End of client support</span></span><br/>    | <span data-ttu-id="4f2f2-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4f2f2-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4f2f2-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4f2f2-136">End of server support</span></span><br/>    | <span data-ttu-id="4f2f2-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4f2f2-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4f2f2-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4f2f2-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f2f2-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f2f2-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f2f2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4f2f2-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f2f2-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f2f2-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f2f2-142">IID</span><span class="sxs-lookup"><span data-stu-id="4f2f2-142">IID</span></span><br/>                      | <span data-ttu-id="4f2f2-143">IID \_ IMsTscNonScriptable è definito come c1e6743a-41C1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="4f2f2-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f2f2-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f2f2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f2f2-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="4f2f2-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="4f2f2-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="4f2f2-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="4f2f2-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="4f2f2-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="4f2f2-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="4f2f2-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="4f2f2-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="4f2f2-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="4f2f2-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="4f2f2-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





