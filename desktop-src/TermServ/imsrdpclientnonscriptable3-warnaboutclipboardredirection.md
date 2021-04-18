---
title: Proprietà WarnAboutClipboardRedirection di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se deve essere visualizzata la finestra di dialogo avviso di sicurezza per avvisare gli utenti del reindirizzamento degli Appunti.
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà WarnAboutClipboardRedirection
- Servizi Desktop remoto proprietà WarnAboutClipboardRedirection, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà WarnAboutClipboardRedirection
- Servizi Desktop remoto proprietà WarnAboutClipboardRedirection, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà WarnAboutClipboardRedirection
- Servizi Desktop remoto proprietà WarnAboutClipboardRedirection, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà WarnAboutClipboardRedirection
- Servizi Desktop remoto proprietà WarnAboutClipboardRedirection, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà WarnAboutClipboardRedirection
- Servizi Desktop remoto proprietà WarnAboutClipboardRedirection, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà WarnAboutClipboardRedirection
- Servizi Desktop remoto proprietà WarnAboutClipboardRedirection, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà WarnAboutClipboardRedirection
- Servizi Desktop remoto proprietà WarnAboutClipboardRedirection, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà WarnAboutClipboardRedirection
- Servizi Desktop remoto proprietà WarnAboutClipboardRedirection, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà WarnAboutClipboardRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutClipboardRedirection
- MsRdpClient5.WarnAboutClipboardRedirection
- MsRdpClient6.WarnAboutClipboardRedirection
- MsRdpClient7.WarnAboutClipboardRedirection
- MsRdpClient8.WarnAboutClipboardRedirection
- MsRdpClient9.WarnAboutClipboardRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8da6fa2f7fb36a110666c8b14a818264813d816
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517547"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a><span data-ttu-id="c91c8-120">Proprietà IMsRdpClientNonScriptable3:: WarnAboutClipboardRedirection</span><span class="sxs-lookup"><span data-stu-id="c91c8-120">IMsRdpClientNonScriptable3::WarnAboutClipboardRedirection property</span></span>

<span data-ttu-id="c91c8-121">Specifica o recupera un valore che indica se deve essere visualizzata la finestra di dialogo avviso di sicurezza per avvisare gli utenti del reindirizzamento degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="c91c8-121">Specifies or retrieves whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

<span data-ttu-id="c91c8-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c91c8-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c91c8-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c91c8-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutClipboardRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutClipboardRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="c91c8-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c91c8-124">Property value</span></span>

<span data-ttu-id="c91c8-125">Specifica se deve essere visualizzata la finestra di dialogo avviso di sicurezza per avvisare gli utenti sul reindirizzamento degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="c91c8-125">Specifies whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c91c8-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c91c8-126">Requirements</span></span>



| <span data-ttu-id="c91c8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c91c8-127">Requirement</span></span> | <span data-ttu-id="c91c8-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c91c8-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c91c8-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c91c8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c91c8-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c91c8-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="c91c8-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c91c8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c91c8-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c91c8-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="c91c8-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c91c8-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="c91c8-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c91c8-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c91c8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c91c8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c91c8-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c91c8-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="c91c8-137">IID</span><span class="sxs-lookup"><span data-stu-id="c91c8-137">IID</span></span><br/>                      | <span data-ttu-id="c91c8-138">IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="c91c8-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c91c8-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c91c8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c91c8-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="c91c8-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="c91c8-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="c91c8-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="c91c8-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="c91c8-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





