---
title: Proprietà PublisherCertificateChain di IMsRdpClientNonScriptable4
description: Controlla la catena di certificati del server di pubblicazione. La catena è archiviata in una variante di tipo VT \_ ByRef che contiene un puntatore a una \_ struttura del contesto della catena di certificati \_ . Per informazioni sulle \_ strutture ByRef VT, vedere VARIANT e VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà PublisherCertificateChain
- Servizi Desktop remoto proprietà PublisherCertificateChain, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà PublisherCertificateChain
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874081"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a><span data-ttu-id="095ce-118">IMsRdpClientNonScriptable4::P proprietà ublisherCertificateChain</span><span class="sxs-lookup"><span data-stu-id="095ce-118">IMsRdpClientNonScriptable4::PublisherCertificateChain property</span></span>

<span data-ttu-id="095ce-119">Controlla la catena di certificati del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="095ce-119">Controls the publisher certificate chain.</span></span> <span data-ttu-id="095ce-120">La catena è archiviata in una variante di tipo **VT \_ ByRef** che contiene un puntatore a una struttura del [**\_ \_ contesto della catena di certificati**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .</span><span class="sxs-lookup"><span data-stu-id="095ce-120">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span> <span data-ttu-id="095ce-121">Per informazioni sulle **strutture \_ ByRef VT** , vedere [Variant e VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="095ce-121">For information about **VT\_BYREF** structures, see [VARIANT and VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="095ce-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="095ce-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="095ce-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="095ce-123">Syntax</span></span>


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a><span data-ttu-id="095ce-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="095ce-124">Property value</span></span>

<span data-ttu-id="095ce-125">Imposta la catena di certificati del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="095ce-125">Sets the publisher certificate chain.</span></span> <span data-ttu-id="095ce-126">La catena è archiviata in una variante di tipo **VT \_ ByRef** che contiene un puntatore a una struttura del [**\_ \_ contesto della catena di certificati**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .</span><span class="sxs-lookup"><span data-stu-id="095ce-126">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="095ce-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="095ce-127">Error codes</span></span>

<span data-ttu-id="095ce-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="095ce-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="095ce-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="095ce-129">Requirements</span></span>



| <span data-ttu-id="095ce-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="095ce-130">Requirement</span></span> | <span data-ttu-id="095ce-131">Valore</span><span class="sxs-lookup"><span data-stu-id="095ce-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="095ce-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="095ce-132">Minimum supported client</span></span><br/> | <span data-ttu-id="095ce-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="095ce-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="095ce-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="095ce-134">Minimum supported server</span></span><br/> | <span data-ttu-id="095ce-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="095ce-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="095ce-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="095ce-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="095ce-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="095ce-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="095ce-138">DLL</span><span class="sxs-lookup"><span data-stu-id="095ce-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="095ce-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="095ce-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="095ce-140">IID</span><span class="sxs-lookup"><span data-stu-id="095ce-140">IID</span></span><br/>                      | <span data-ttu-id="095ce-141">IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="095ce-141">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="095ce-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="095ce-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="095ce-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="095ce-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="095ce-144">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="095ce-144">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

