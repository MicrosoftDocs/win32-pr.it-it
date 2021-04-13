---
title: Proprietà IMsRdpClientNonScriptable3 PromptForCredentials (wuapi. h)
description: Specifica o recupera se la finestra di dialogo Richiedi credenziali è abilitata per la connessione.
ms.assetid: 252ec5bd-bd52-40d4-ae48-b2c00c0720c0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PromptForCredentials
- Servizi Desktop remoto proprietà PromptForCredentials, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà PromptForCredentials
- Servizi Desktop remoto proprietà PromptForCredentials, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà PromptForCredentials
- Servizi Desktop remoto proprietà PromptForCredentials, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà PromptForCredentials
- Servizi Desktop remoto proprietà PromptForCredentials, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà PromptForCredentials
- Servizi Desktop remoto proprietà PromptForCredentials, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà PromptForCredentials
- Servizi Desktop remoto proprietà PromptForCredentials, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà PromptForCredentials
- Servizi Desktop remoto proprietà PromptForCredentials, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà PromptForCredentials
- Servizi Desktop remoto proprietà PromptForCredentials, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà PromptForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.PromptForCredentials
- IMsRdpClientNonScriptable3.get_PromptForCredentials
- IMsRdpClientNonScriptable3.put_PromptForCredentials
- IMsRdpClientNonScriptable4.PromptForCredentials
- IMsRdpClientNonScriptable4.get_PromptForCredentials
- IMsRdpClientNonScriptable4.put_PromptForCredentials
- IMsRdpClientNonScriptable5.PromptForCredentials
- IMsRdpClientNonScriptable5.get_PromptForCredentials
- IMsRdpClientNonScriptable5.put_PromptForCredentials
- MsRdpClient5.PromptForCredentials
- MsRdpClient6.PromptForCredentials
- MsRdpClient7.PromptForCredentials
- MsRdpClient8.PromptForCredentials
- MsRdpClient9.PromptForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f913937c9a2ff01d4aabeaba48dcbdc8ddb21d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340372"
---
# <a name="imsrdpclientnonscriptable3promptforcredentials-property"></a><span data-ttu-id="f821b-120">IMsRdpClientNonScriptable3::P proprietà romptForCredentials</span><span class="sxs-lookup"><span data-stu-id="f821b-120">IMsRdpClientNonScriptable3::PromptForCredentials property</span></span>

<span data-ttu-id="f821b-121">Specifica o recupera se la finestra di dialogo Richiedi credenziali è abilitata per la connessione.</span><span class="sxs-lookup"><span data-stu-id="f821b-121">Specifies or retrieves whether the prompt for credentials dialog is enabled for the connection.</span></span>

<span data-ttu-id="f821b-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f821b-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f821b-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f821b-123">Syntax</span></span>


```C++
HRESULT put_PromptForCredentials(
  [in]  VARIANT_BOOL fPrompt
);

HRESULT get_PromptForCredentials(
  [out] VARIANT_BOOL *pfPrompt
);
```



## <a name="property-value"></a><span data-ttu-id="f821b-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f821b-124">Property value</span></span>

<span data-ttu-id="f821b-125">Specifica se la finestra di dialogo Richiedi credenziali è abilitata per la connessione.</span><span class="sxs-lookup"><span data-stu-id="f821b-125">Specifies whether the prompt for credentials dialog is enabled for the connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f821b-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f821b-126">Error codes</span></span>

## <a name="requirements"></a><span data-ttu-id="f821b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f821b-127">Requirements</span></span>



| <span data-ttu-id="f821b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f821b-128">Requirement</span></span> | <span data-ttu-id="f821b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f821b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f821b-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f821b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f821b-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f821b-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="f821b-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f821b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f821b-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f821b-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="f821b-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f821b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f821b-135"><dt>Wuapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f821b-135"><dt>Wuapi.h</dt></span></span> </dl>            |
| <span data-ttu-id="f821b-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f821b-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="f821b-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f821b-137"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="f821b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f821b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f821b-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f821b-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="f821b-140">IID</span><span class="sxs-lookup"><span data-stu-id="f821b-140">IID</span></span><br/>                      | <span data-ttu-id="f821b-141">IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="f821b-141">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f821b-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f821b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f821b-143">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="f821b-143">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="f821b-144">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="f821b-144">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="f821b-145">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="f821b-145">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





