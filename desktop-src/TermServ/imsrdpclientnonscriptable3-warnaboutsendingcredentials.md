---
title: Proprietà WarnAboutSendingCredentials di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se nella finestra di dialogo avviso di sicurezza deve essere incluso un avviso relativo all'invio di credenziali al server remoto prima di avviare una sessione.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301302"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a><span data-ttu-id="56f4b-120">Proprietà IMsRdpClientNonScriptable3:: WarnAboutSendingCredentials</span><span class="sxs-lookup"><span data-stu-id="56f4b-120">IMsRdpClientNonScriptable3::WarnAboutSendingCredentials property</span></span>

<span data-ttu-id="56f4b-121">Specifica o recupera un valore che indica se nella finestra di dialogo avviso di sicurezza deve essere incluso un avviso relativo all'invio di credenziali al server remoto prima di avviare una sessione.</span><span class="sxs-lookup"><span data-stu-id="56f4b-121">Specifies or retrieves whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

<span data-ttu-id="56f4b-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="56f4b-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="56f4b-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56f4b-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="56f4b-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="56f4b-124">Property value</span></span>

<span data-ttu-id="56f4b-125">Specifica se la finestra di dialogo avviso di sicurezza deve includere un avviso sull'invio di credenziali al server remoto prima di avviare una sessione.</span><span class="sxs-lookup"><span data-stu-id="56f4b-125">Specifies whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="56f4b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56f4b-126">Requirements</span></span>



| <span data-ttu-id="56f4b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="56f4b-127">Requirement</span></span> | <span data-ttu-id="56f4b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="56f4b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="56f4b-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56f4b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="56f4b-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56f4b-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="56f4b-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56f4b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="56f4b-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56f4b-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="56f4b-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="56f4b-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="56f4b-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56f4b-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="56f4b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="56f4b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56f4b-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56f4b-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="56f4b-137">IID</span><span class="sxs-lookup"><span data-stu-id="56f4b-137">IID</span></span><br/>                      | <span data-ttu-id="56f4b-138">IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="56f4b-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56f4b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56f4b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56f4b-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="56f4b-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="56f4b-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="56f4b-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="56f4b-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="56f4b-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





