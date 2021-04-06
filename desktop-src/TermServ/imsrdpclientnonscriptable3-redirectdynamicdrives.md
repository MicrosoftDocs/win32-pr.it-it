---
title: Proprietà RedirectDynamicDrives di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se le unità Plug and Play (PnP) associate in modo dinamico che vengono enumerate in una sessione sono disponibili per il reindirizzamento.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà RedirectDynamicDrives
- Servizi Desktop remoto proprietà RedirectDynamicDrives, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà RedirectDynamicDrives
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19c0e6e20f7f73481f6f2ecbc50ab0eda512ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743647"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a><span data-ttu-id="9fe3b-120">Proprietà IMsRdpClientNonScriptable3:: RedirectDynamicDrives</span><span class="sxs-lookup"><span data-stu-id="9fe3b-120">IMsRdpClientNonScriptable3::RedirectDynamicDrives property</span></span>

<span data-ttu-id="9fe3b-121">Specifica o recupera un valore che indica se le unità Plug and Play (PnP) associate in modo dinamico che vengono enumerate in una sessione sono disponibili per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="9fe3b-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) drives that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="9fe3b-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9fe3b-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe3b-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fe3b-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a><span data-ttu-id="9fe3b-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9fe3b-124">Property value</span></span>

<span data-ttu-id="9fe3b-125">Specifica se le unità PnP associate in modo dinamico enumerate in una sessione sono disponibili per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="9fe3b-125">Specifies whether dynamically attached PnP drives that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe3b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fe3b-126">Requirements</span></span>



| <span data-ttu-id="9fe3b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fe3b-127">Requirement</span></span> | <span data-ttu-id="9fe3b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9fe3b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe3b-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fe3b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9fe3b-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fe3b-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="9fe3b-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fe3b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9fe3b-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fe3b-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="9fe3b-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9fe3b-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="9fe3b-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fe3b-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="9fe3b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9fe3b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fe3b-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fe3b-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="9fe3b-137">IID</span><span class="sxs-lookup"><span data-stu-id="9fe3b-137">IID</span></span><br/>                      | <span data-ttu-id="9fe3b-138">IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="9fe3b-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9fe3b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fe3b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe3b-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="9fe3b-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="9fe3b-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="9fe3b-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="9fe3b-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="9fe3b-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





