---
title: Proprietà BinarySalt di IMsTscNonScriptable
description: Questa proprietà non è più disponibile per l'utilizzo. | Proprietà BinarySalt di IMsTscNonScriptable
ms.assetid: 7af2e5be-9ddb-46ab-947c-f79ab890d7bc
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BinarySalt
- Servizi Desktop remoto proprietà BinarySalt, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto, proprietà BinarySalt
- Servizi Desktop remoto proprietà BinarySalt, oggetto MsTscAx
- Oggetto MsTscAx Servizi Desktop remoto, proprietà BinarySalt
- Servizi Desktop remoto proprietà BinarySalt, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto, proprietà BinarySalt
- Servizi Desktop remoto proprietà BinarySalt, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, proprietà BinarySalt
- Servizi Desktop remoto proprietà BinarySalt, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà BinarySalt
- Servizi Desktop remoto proprietà BinarySalt, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà BinarySalt
- Servizi Desktop remoto proprietà BinarySalt, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà BinarySalt
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinarySalt
- IMsTscNonScriptable.get_BinarySalt
- IMsTscNonScriptable.put_BinarySalt
- MsTscAx.BinarySalt
- IMsRdpClientNonScriptable.BinarySalt
- IMsRdpClientNonScriptable.get_BinarySalt
- IMsRdpClientNonScriptable.put_BinarySalt
- IMsRdpClientNonScriptable2.BinarySalt
- IMsRdpClientNonScriptable2.get_BinarySalt
- IMsRdpClientNonScriptable2.put_BinarySalt
- IMsRdpClientNonScriptable3.BinarySalt
- IMsRdpClientNonScriptable3.get_BinarySalt
- IMsRdpClientNonScriptable3.put_BinarySalt
- IMsRdpClientNonScriptable4.BinarySalt
- IMsRdpClientNonScriptable4.get_BinarySalt
- IMsRdpClientNonScriptable4.put_BinarySalt
- IMsRdpClientNonScriptable5.BinarySalt
- IMsRdpClientNonScriptable5.get_BinarySalt
- IMsRdpClientNonScriptable5.put_BinarySalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb13ccb79a9cf2c309a32772a73b393756c7bdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321323"
---
# <a name="imstscnonscriptablebinarysalt-property"></a><span data-ttu-id="07ad1-119">Proprietà IMsTscNonScriptable:: BinarySalt</span><span class="sxs-lookup"><span data-stu-id="07ad1-119">IMsTscNonScriptable::BinarySalt property</span></span>

<span data-ttu-id="07ad1-120">Questa proprietà non è più disponibile per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="07ad1-120">This property is no longer available for use.</span></span>

<span data-ttu-id="07ad1-121">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="07ad1-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="07ad1-122">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07ad1-122">Syntax</span></span>


```C++
HRESULT put_BinarySalt(
  [in]  BSTR newSalt
);

HRESULT get_BinarySalt(
  [out] BSTR *pSalt
);
```



## <a name="property-value"></a><span data-ttu-id="07ad1-123">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="07ad1-123">Property value</span></span>

<span data-ttu-id="07ad1-124">Nuova parte del Salt binario per una password con codifica binaria.</span><span class="sxs-lookup"><span data-stu-id="07ad1-124">The new binary salt part for a binary encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="07ad1-125">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="07ad1-125">Error codes</span></span>

<span data-ttu-id="07ad1-126">Restituisce **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="07ad1-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="07ad1-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07ad1-127">Requirements</span></span>



| <span data-ttu-id="07ad1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="07ad1-128">Requirement</span></span> | <span data-ttu-id="07ad1-129">Valore</span><span class="sxs-lookup"><span data-stu-id="07ad1-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07ad1-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07ad1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="07ad1-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07ad1-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="07ad1-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07ad1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="07ad1-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07ad1-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="07ad1-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="07ad1-134">End of client support</span></span><br/>    | <span data-ttu-id="07ad1-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07ad1-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="07ad1-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="07ad1-136">End of server support</span></span><br/>    | <span data-ttu-id="07ad1-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07ad1-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="07ad1-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="07ad1-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="07ad1-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07ad1-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="07ad1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="07ad1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07ad1-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07ad1-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="07ad1-142">IID</span><span class="sxs-lookup"><span data-stu-id="07ad1-142">IID</span></span><br/>                      | <span data-ttu-id="07ad1-143">IID \_ IMsTscNonScriptable è definito come c1e6743a-41C1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="07ad1-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07ad1-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07ad1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ad1-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="07ad1-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="07ad1-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="07ad1-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="07ad1-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="07ad1-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="07ad1-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="07ad1-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="07ad1-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="07ad1-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="07ad1-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="07ad1-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





