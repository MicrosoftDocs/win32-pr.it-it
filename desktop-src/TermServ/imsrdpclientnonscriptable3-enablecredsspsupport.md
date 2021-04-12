---
title: Proprietà EnableCredSspSupport di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se il provider del servizio di sicurezza delle credenziali (CredSSP) è abilitato per la connessione.
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà EnableCredSspSupport
- Servizi Desktop remoto proprietà EnableCredSspSupport, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2330b800d15f95a7b59a01735de971dd4b212d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119639"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a><span data-ttu-id="0e7e5-120">Proprietà IMsRdpClientNonScriptable3:: EnableCredSspSupport</span><span class="sxs-lookup"><span data-stu-id="0e7e5-120">IMsRdpClientNonScriptable3::EnableCredSspSupport property</span></span>

<span data-ttu-id="0e7e5-121">Specifica o recupera un valore che indica se il provider del servizio di sicurezza delle credenziali (CredSSP) è abilitato per la connessione.</span><span class="sxs-lookup"><span data-stu-id="0e7e5-121">Specifies or retrieves whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="0e7e5-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="0e7e5-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e7e5-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e7e5-123">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="0e7e5-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0e7e5-124">Property value</span></span>

<span data-ttu-id="0e7e5-125">Specifica se CredSSP è abilitato per questa connessione.</span><span class="sxs-lookup"><span data-stu-id="0e7e5-125">Specifies whether CredSSP is enabled for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e7e5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e7e5-126">Requirements</span></span>



| <span data-ttu-id="0e7e5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e7e5-127">Requirement</span></span> | <span data-ttu-id="0e7e5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0e7e5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e7e5-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e7e5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0e7e5-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e7e5-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="0e7e5-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e7e5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0e7e5-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e7e5-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="0e7e5-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0e7e5-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e7e5-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e7e5-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="0e7e5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0e7e5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e7e5-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e7e5-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="0e7e5-137">IID</span><span class="sxs-lookup"><span data-stu-id="0e7e5-137">IID</span></span><br/>                      | <span data-ttu-id="0e7e5-138">IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="0e7e5-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e7e5-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e7e5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e7e5-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="0e7e5-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="0e7e5-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="0e7e5-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="0e7e5-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="0e7e5-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





