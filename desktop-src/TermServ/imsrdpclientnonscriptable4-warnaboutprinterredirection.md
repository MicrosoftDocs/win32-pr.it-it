---
title: Proprietà WarnAboutPrinterRedirection di IMsRdpClientNonScriptable4
description: Controlla se la finestra di dialogo Reindirizzamento Visualizza un messaggio sul reindirizzamento della stampante prima di avviare una sessione.
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà WarnAboutPrinterRedirection
- Servizi Desktop remoto proprietà WarnAboutPrinterRedirection, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà WarnAboutPrinterRedirection
- Servizi Desktop remoto proprietà WarnAboutPrinterRedirection, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà WarnAboutPrinterRedirection
- Servizi Desktop remoto proprietà WarnAboutPrinterRedirection, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà WarnAboutPrinterRedirection
- Servizi Desktop remoto proprietà WarnAboutPrinterRedirection, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà WarnAboutPrinterRedirection
- Servizi Desktop remoto proprietà WarnAboutPrinterRedirection, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà WarnAboutPrinterRedirection
- Servizi Desktop remoto proprietà WarnAboutPrinterRedirection, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà WarnAboutPrinterRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutPrinterRedirection
- MsRdpClient6.WarnAboutPrinterRedirection
- MsRdpClient7.WarnAboutPrinterRedirection
- MsRdpClient8.WarnAboutPrinterRedirection
- MsRdpClient9.WarnAboutPrinterRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e2fa93995946e741caa76f1ee5b84be79d9c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340803"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a><span data-ttu-id="2e0d6-116">Proprietà IMsRdpClientNonScriptable4:: WarnAboutPrinterRedirection</span><span class="sxs-lookup"><span data-stu-id="2e0d6-116">IMsRdpClientNonScriptable4::WarnAboutPrinterRedirection property</span></span>

<span data-ttu-id="2e0d6-117">Controlla se la finestra di dialogo Reindirizzamento Visualizza un messaggio sul reindirizzamento della stampante prima di avviare una sessione.</span><span class="sxs-lookup"><span data-stu-id="2e0d6-117">Controls whether the redirection dialog box displays a message about printer redirection before starting a session.</span></span>

<span data-ttu-id="2e0d6-118">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2e0d6-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e0d6-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e0d6-119">Syntax</span></span>


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="2e0d6-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2e0d6-120">Property value</span></span>

<span data-ttu-id="2e0d6-121">Imposta un valore che indica se nella finestra di dialogo Reindirizzamento viene visualizzato un messaggio relativo al reindirizzamento delle stampanti.</span><span class="sxs-lookup"><span data-stu-id="2e0d6-121">Sets whether the redirection dialog box displays a message about printer redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2e0d6-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2e0d6-122">Error codes</span></span>

<span data-ttu-id="2e0d6-123">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2e0d6-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e0d6-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e0d6-124">Requirements</span></span>



| <span data-ttu-id="2e0d6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e0d6-125">Requirement</span></span> | <span data-ttu-id="2e0d6-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2e0d6-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0d6-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e0d6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2e0d6-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e0d6-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2e0d6-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e0d6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2e0d6-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e0d6-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2e0d6-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2e0d6-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e0d6-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e0d6-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="2e0d6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2e0d6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e0d6-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e0d6-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="2e0d6-135">IID</span><span class="sxs-lookup"><span data-stu-id="2e0d6-135">IID</span></span><br/>                      | <span data-ttu-id="2e0d6-136">IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="2e0d6-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e0d6-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e0d6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0d6-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="2e0d6-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="2e0d6-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="2e0d6-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





