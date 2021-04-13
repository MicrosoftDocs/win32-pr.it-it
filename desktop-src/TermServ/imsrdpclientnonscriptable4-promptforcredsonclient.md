---
title: Proprietà PromptForCredsOnClient di IMsRdpClientNonScriptable4
description: Specifica se il controllo client visualizza una finestra di dialogo in cui vengono richieste le credenziali.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà PromptForCredsOnClient
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400742"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a><span data-ttu-id="123c3-116">IMsRdpClientNonScriptable4::P proprietà romptForCredsOnClient</span><span class="sxs-lookup"><span data-stu-id="123c3-116">IMsRdpClientNonScriptable4::PromptForCredsOnClient property</span></span>

<span data-ttu-id="123c3-117">Specifica se il controllo client visualizza una finestra di dialogo in cui vengono richieste le credenziali.</span><span class="sxs-lookup"><span data-stu-id="123c3-117">Specifies whether the client control displays a dialog box that prompts for credentials.</span></span>

<span data-ttu-id="123c3-118">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="123c3-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="123c3-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="123c3-119">Syntax</span></span>


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a><span data-ttu-id="123c3-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="123c3-120">Property value</span></span>

<span data-ttu-id="123c3-121">Imposta un valore che indica se il controllo client visualizza una finestra di dialogo in cui vengono richieste le credenziali.</span><span class="sxs-lookup"><span data-stu-id="123c3-121">Sets whether the client control displays a dialog box that prompts for credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="123c3-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="123c3-122">Error codes</span></span>

<span data-ttu-id="123c3-123">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="123c3-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="123c3-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="123c3-124">Requirements</span></span>



| <span data-ttu-id="123c3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="123c3-125">Requirement</span></span> | <span data-ttu-id="123c3-126">Valore</span><span class="sxs-lookup"><span data-stu-id="123c3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="123c3-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="123c3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="123c3-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="123c3-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="123c3-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="123c3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="123c3-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="123c3-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="123c3-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="123c3-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="123c3-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="123c3-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="123c3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="123c3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="123c3-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="123c3-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="123c3-135">IID</span><span class="sxs-lookup"><span data-stu-id="123c3-135">IID</span></span><br/>                      | <span data-ttu-id="123c3-136">IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="123c3-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="123c3-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="123c3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123c3-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="123c3-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="123c3-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="123c3-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





