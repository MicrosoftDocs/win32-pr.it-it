---
title: Proprietà PortableSalt di IMsTscNonScriptable
description: Questa proprietà non è più supportata.
ms.assetid: 1f123ec8-27b6-4637-9c57-fe32a224be8a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PortableSalt
- Servizi Desktop remoto proprietà PortableSalt, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto, proprietà PortableSalt
- Servizi Desktop remoto proprietà PortableSalt, oggetto MsTscAx
- Oggetto MsTscAx Servizi Desktop remoto, proprietà PortableSalt
- Servizi Desktop remoto proprietà PortableSalt, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto, proprietà PortableSalt
- Servizi Desktop remoto proprietà PortableSalt, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, proprietà PortableSalt
- Servizi Desktop remoto proprietà PortableSalt, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà PortableSalt
- Servizi Desktop remoto proprietà PortableSalt, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà PortableSalt
- Servizi Desktop remoto proprietà PortableSalt, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà PortableSalt
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortableSalt
- IMsTscNonScriptable.get_PortableSalt
- IMsTscNonScriptable.put_PortableSalt
- MsTscAx.PortableSalt
- IMsRdpClientNonScriptable.PortableSalt
- IMsRdpClientNonScriptable.get_PortableSalt
- IMsRdpClientNonScriptable.put_PortableSalt
- IMsRdpClientNonScriptable2.PortableSalt
- IMsRdpClientNonScriptable2.get_PortableSalt
- IMsRdpClientNonScriptable2.put_PortableSalt
- IMsRdpClientNonScriptable3.PortableSalt
- IMsRdpClientNonScriptable3.get_PortableSalt
- IMsRdpClientNonScriptable3.put_PortableSalt
- IMsRdpClientNonScriptable4.PortableSalt
- IMsRdpClientNonScriptable4.get_PortableSalt
- IMsRdpClientNonScriptable4.put_PortableSalt
- IMsRdpClientNonScriptable5.PortableSalt
- IMsRdpClientNonScriptable5.get_PortableSalt
- IMsRdpClientNonScriptable5.put_PortableSalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0162073b8361cc89f7ab2e33f60406c0db935bdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742386"
---
# <a name="imstscnonscriptableportablesalt-property"></a><span data-ttu-id="a6ba6-118">IMsTscNonScriptable::P proprietà ortableSalt</span><span class="sxs-lookup"><span data-stu-id="a6ba6-118">IMsTscNonScriptable::PortableSalt property</span></span>

<span data-ttu-id="a6ba6-119">Questa proprietà non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="a6ba6-119">This property is no longer supported.</span></span>

<span data-ttu-id="a6ba6-120">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a6ba6-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ba6-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6ba6-121">Syntax</span></span>


```C++
HRESULT put_PortableSalt(
  [in]  BSTR newPortableSalt
);

HRESULT get_PortableSalt(
  [out] BSTR *pPortableSalt
);
```



## <a name="property-value"></a><span data-ttu-id="a6ba6-122">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a6ba6-122">Property value</span></span>

<span data-ttu-id="a6ba6-123">Nuova parte del Salt portatile per una password con codifica portatile.</span><span class="sxs-lookup"><span data-stu-id="a6ba6-123">The new portable salt part for a portable encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a6ba6-124">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a6ba6-124">Error codes</span></span>

<span data-ttu-id="a6ba6-125">Restituisce **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="a6ba6-125">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ba6-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6ba6-126">Requirements</span></span>



| <span data-ttu-id="a6ba6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6ba6-127">Requirement</span></span> | <span data-ttu-id="a6ba6-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a6ba6-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ba6-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6ba6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ba6-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a6ba6-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a6ba6-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6ba6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ba6-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a6ba6-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a6ba6-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a6ba6-133">End of client support</span></span><br/>    | <span data-ttu-id="a6ba6-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a6ba6-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a6ba6-135">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a6ba6-135">End of server support</span></span><br/>    | <span data-ttu-id="a6ba6-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a6ba6-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a6ba6-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a6ba6-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="a6ba6-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6ba6-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a6ba6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a6ba6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6ba6-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6ba6-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a6ba6-141">IID</span><span class="sxs-lookup"><span data-stu-id="a6ba6-141">IID</span></span><br/>                      | <span data-ttu-id="a6ba6-142">IID \_ IMsTscNonScriptable è definito come c1e6743a-41C1-4a74-832a-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="a6ba6-142">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a6ba6-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6ba6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ba6-144">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="a6ba6-144">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="a6ba6-145">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="a6ba6-145">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="a6ba6-146">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="a6ba6-146">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="a6ba6-147">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="a6ba6-147">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="a6ba6-148">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a6ba6-148">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="a6ba6-149">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="a6ba6-149">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="a6ba6-150">**PortablePassword**</span><span class="sxs-lookup"><span data-stu-id="a6ba6-150">**PortablePassword**</span></span>](imstscnonscriptable-portablepassword.md)
</dt> </dl>

 

 





