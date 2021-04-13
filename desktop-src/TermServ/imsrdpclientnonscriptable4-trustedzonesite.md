---
title: Proprietà TrustedZoneSite di IMsRdpClientNonScriptable4
description: Specifica se il sito Web da cui l'utente ha avviato la connessione si trova nell'elenco dei siti attendibili del computer client dell'utente.
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà TrustedZoneSite
- Servizi Desktop remoto proprietà TrustedZoneSite, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà TrustedZoneSite
- Servizi Desktop remoto proprietà TrustedZoneSite, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà TrustedZoneSite
- Servizi Desktop remoto proprietà TrustedZoneSite, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà TrustedZoneSite
- Servizi Desktop remoto proprietà TrustedZoneSite, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà TrustedZoneSite
- Servizi Desktop remoto proprietà TrustedZoneSite, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà TrustedZoneSite
- Servizi Desktop remoto proprietà TrustedZoneSite, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà TrustedZoneSite
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400741"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a><span data-ttu-id="14678-116">Proprietà IMsRdpClientNonScriptable4:: TrustedZoneSite</span><span class="sxs-lookup"><span data-stu-id="14678-116">IMsRdpClientNonScriptable4::TrustedZoneSite property</span></span>

<span data-ttu-id="14678-117">Specifica se il sito Web da cui l'utente ha avviato la connessione si trova nell'elenco dei siti attendibili del computer client dell'utente.</span><span class="sxs-lookup"><span data-stu-id="14678-117">Specifies whether the website from which the user launched the connection is in the trusted sites list of the user's client computer.</span></span>

<span data-ttu-id="14678-118">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="14678-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="14678-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14678-119">Syntax</span></span>


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a><span data-ttu-id="14678-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="14678-120">Property value</span></span>

<span data-ttu-id="14678-121">Imposta la proprietà TrustedZoneSite.</span><span class="sxs-lookup"><span data-stu-id="14678-121">Sets the TrustedZoneSite property.</span></span> <span data-ttu-id="14678-122">Questo metodo non ha alcun effetto sul fatto che il sito Web da cui l'utente ha avviato la connessione si trovi nell'elenco dei siti attendibili del computer client.</span><span class="sxs-lookup"><span data-stu-id="14678-122">This method has no effect on whether the website from which the user launched the connection is in the trusted sites list of the client computer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="14678-123">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="14678-123">Error codes</span></span>

<span data-ttu-id="14678-124">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="14678-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="14678-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14678-125">Requirements</span></span>



| <span data-ttu-id="14678-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="14678-126">Requirement</span></span> | <span data-ttu-id="14678-127">Valore</span><span class="sxs-lookup"><span data-stu-id="14678-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="14678-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14678-128">Minimum supported client</span></span><br/> | <span data-ttu-id="14678-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14678-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="14678-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14678-130">Minimum supported server</span></span><br/> | <span data-ttu-id="14678-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14678-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="14678-132">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="14678-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="14678-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14678-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="14678-134">DLL</span><span class="sxs-lookup"><span data-stu-id="14678-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14678-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14678-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="14678-136">IID</span><span class="sxs-lookup"><span data-stu-id="14678-136">IID</span></span><br/>                      | <span data-ttu-id="14678-137">IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="14678-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14678-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14678-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14678-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="14678-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="14678-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="14678-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





