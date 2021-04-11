---
title: Proprietà LaunchedViaClientShellInterface di IMsRdpClientNonScriptable4
description: Specifica se l'utente ha avviato il controllo client utilizzando l'interfaccia Desktop remoto Accesso Web (RD Accesso Web).
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964424"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a><span data-ttu-id="2e8c8-118">Proprietà IMsRdpClientNonScriptable4:: LaunchedViaClientShellInterface</span><span class="sxs-lookup"><span data-stu-id="2e8c8-118">IMsRdpClientNonScriptable4::LaunchedViaClientShellInterface property</span></span>

<span data-ttu-id="2e8c8-119">Specifica se l'utente ha avviato il controllo client utilizzando l'interfaccia Desktop remoto Accesso Web (RD Accesso Web).</span><span class="sxs-lookup"><span data-stu-id="2e8c8-119">Specifies whether the user launched the client control by using the Remote Desktop Web Access (RD Web Access) interface.</span></span>

<span data-ttu-id="2e8c8-120">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2e8c8-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e8c8-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e8c8-121">Syntax</span></span>


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a><span data-ttu-id="2e8c8-122">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2e8c8-122">Property value</span></span>

<span data-ttu-id="2e8c8-123">Imposta la proprietà **LaunchedViaClientShellInterface** .</span><span class="sxs-lookup"><span data-stu-id="2e8c8-123">Sets the **LaunchedViaClientShellInterface** property.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2e8c8-124">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2e8c8-124">Error codes</span></span>

<span data-ttu-id="2e8c8-125">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2e8c8-125">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e8c8-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e8c8-126">Requirements</span></span>



| <span data-ttu-id="2e8c8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e8c8-127">Requirement</span></span> | <span data-ttu-id="2e8c8-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2e8c8-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e8c8-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e8c8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2e8c8-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e8c8-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2e8c8-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e8c8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2e8c8-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e8c8-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2e8c8-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2e8c8-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e8c8-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e8c8-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="2e8c8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2e8c8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e8c8-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e8c8-136"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="2e8c8-137">IID</span><span class="sxs-lookup"><span data-stu-id="2e8c8-137">IID</span></span><br/>                      | <span data-ttu-id="2e8c8-138">IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="2e8c8-138">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e8c8-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e8c8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e8c8-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="2e8c8-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="2e8c8-141">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="2e8c8-141">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





