---
title: Proprietà RedirectDynamicDevices di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se i dispositivi PnP (dynamicly Attached Plug and Play) enumerati in una sessione sono disponibili per il reindirizzamento.
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà RedirectDynamicDevices
- Servizi Desktop remoto proprietà RedirectDynamicDevices, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà RedirectDynamicDevices
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740399"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a><span data-ttu-id="66fa3-120">Proprietà IMsRdpClientNonScriptable3:: RedirectDynamicDevices</span><span class="sxs-lookup"><span data-stu-id="66fa3-120">IMsRdpClientNonScriptable3::RedirectDynamicDevices property</span></span>

<span data-ttu-id="66fa3-121">Specifica o recupera un valore che indica se i dispositivi PnP (dynamicly Attached Plug and Play) enumerati in una sessione sono disponibili per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="66fa3-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) devices that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="66fa3-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="66fa3-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="66fa3-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66fa3-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a><span data-ttu-id="66fa3-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="66fa3-124">Property value</span></span>

<span data-ttu-id="66fa3-125">Specifica se i dispositivi PnP collegati in modo dinamico enumerati durante una sessione sono disponibili per il reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="66fa3-125">Specifies whether dynamically attached PnP devices that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="66fa3-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66fa3-126">Requirements</span></span>



| <span data-ttu-id="66fa3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="66fa3-127">Requirement</span></span> | <span data-ttu-id="66fa3-128">Valore</span><span class="sxs-lookup"><span data-stu-id="66fa3-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="66fa3-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66fa3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="66fa3-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66fa3-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="66fa3-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66fa3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="66fa3-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66fa3-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="66fa3-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="66fa3-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="66fa3-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66fa3-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="66fa3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="66fa3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66fa3-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66fa3-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="66fa3-137">IID</span><span class="sxs-lookup"><span data-stu-id="66fa3-137">IID</span></span><br/>                      | <span data-ttu-id="66fa3-138">IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="66fa3-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66fa3-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66fa3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66fa3-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="66fa3-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="66fa3-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="66fa3-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="66fa3-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="66fa3-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





