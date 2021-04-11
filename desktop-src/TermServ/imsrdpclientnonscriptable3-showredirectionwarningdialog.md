---
title: Proprietà ShowRedirectionWarningDialog di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se deve essere visualizzata la finestra di dialogo di avviso del reindirizzamento.
ms.assetid: 7ed37288-77c3-4551-a553-1ca679e1047a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ShowRedirectionWarningDialog
- Servizi Desktop remoto proprietà ShowRedirectionWarningDialog, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà ShowRedirectionWarningDialog
- Servizi Desktop remoto proprietà ShowRedirectionWarningDialog, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà ShowRedirectionWarningDialog
- Servizi Desktop remoto proprietà ShowRedirectionWarningDialog, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà ShowRedirectionWarningDialog
- Servizi Desktop remoto proprietà ShowRedirectionWarningDialog, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà ShowRedirectionWarningDialog
- Servizi Desktop remoto proprietà ShowRedirectionWarningDialog, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà ShowRedirectionWarningDialog
- Servizi Desktop remoto proprietà ShowRedirectionWarningDialog, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà ShowRedirectionWarningDialog
- Servizi Desktop remoto proprietà ShowRedirectionWarningDialog, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà ShowRedirectionWarningDialog
- Servizi Desktop remoto proprietà ShowRedirectionWarningDialog, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà ShowRedirectionWarningDialog
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.put_ShowRedirectionWarningDialog
- MsRdpClient5.ShowRedirectionWarningDialog
- MsRdpClient6.ShowRedirectionWarningDialog
- MsRdpClient7.ShowRedirectionWarningDialog
- MsRdpClient8.ShowRedirectionWarningDialog
- MsRdpClient9.ShowRedirectionWarningDialog
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468e1721de3395067ca570c2051f3906df626071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048086"
---
# <a name="imsrdpclientnonscriptable3showredirectionwarningdialog-property"></a><span data-ttu-id="e3b09-120">Proprietà IMsRdpClientNonScriptable3:: ShowRedirectionWarningDialog</span><span class="sxs-lookup"><span data-stu-id="e3b09-120">IMsRdpClientNonScriptable3::ShowRedirectionWarningDialog property</span></span>

<span data-ttu-id="e3b09-121">Specifica o recupera un valore che indica se deve essere visualizzata la finestra di dialogo di avviso del reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="e3b09-121">Specifies or retrieves whether the redirection warning dialog box should be shown.</span></span>

<span data-ttu-id="e3b09-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e3b09-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b09-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3b09-123">Syntax</span></span>


```C++
HRESULT put_ShowRedirectionWarningDialog(
  [in]  VARIANT_BOOL fShowRdrDlg
);

HRESULT get_ShowRedirectionWarningDialog(
  [out] VARIANT_BOOL *pfShowRdrDlg
);
```



## <a name="property-value"></a><span data-ttu-id="e3b09-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e3b09-124">Property value</span></span>

<span data-ttu-id="e3b09-125">Specifica se deve essere visualizzata la finestra di dialogo di avviso del reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="e3b09-125">Specifies whether the redirection warning dialog box should be shown.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b09-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3b09-126">Requirements</span></span>



| <span data-ttu-id="e3b09-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b09-127">Requirement</span></span> | <span data-ttu-id="e3b09-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e3b09-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b09-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3b09-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e3b09-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3b09-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="e3b09-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3b09-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e3b09-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3b09-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="e3b09-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e3b09-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3b09-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3b09-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e3b09-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e3b09-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3b09-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3b09-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e3b09-137">IID</span><span class="sxs-lookup"><span data-stu-id="e3b09-137">IID</span></span><br/>                      | <span data-ttu-id="e3b09-138">IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="e3b09-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3b09-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3b09-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b09-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="e3b09-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="e3b09-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="e3b09-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="e3b09-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="e3b09-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





