---
title: Proprietà AllowCredentialSaving di IMsRdpClientNonScriptable4
description: Specifica se nella finestra di dialogo credenziali viene visualizzata una casella di controllo che consente di salvare le credenziali.
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AllowCredentialSaving
- Servizi Desktop remoto proprietà AllowCredentialSaving, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà AllowCredentialSaving
- Servizi Desktop remoto proprietà AllowCredentialSaving, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà AllowCredentialSaving
- Servizi Desktop remoto proprietà AllowCredentialSaving, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà AllowCredentialSaving
- Servizi Desktop remoto proprietà AllowCredentialSaving, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà AllowCredentialSaving
- Servizi Desktop remoto proprietà AllowCredentialSaving, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà AllowCredentialSaving
- Servizi Desktop remoto proprietà AllowCredentialSaving, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà AllowCredentialSaving
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240e2eb8e80209ee5c90d63f2996231cf84bb2dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301890"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a><span data-ttu-id="30290-116">Proprietà IMsRdpClientNonScriptable4:: AllowCredentialSaving</span><span class="sxs-lookup"><span data-stu-id="30290-116">IMsRdpClientNonScriptable4::AllowCredentialSaving property</span></span>

<span data-ttu-id="30290-117">Specifica se nella finestra di dialogo credenziali viene visualizzata una casella di controllo che consente di salvare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="30290-117">Specifies whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

<span data-ttu-id="30290-118">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="30290-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="30290-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30290-119">Syntax</span></span>


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a><span data-ttu-id="30290-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="30290-120">Property value</span></span>

<span data-ttu-id="30290-121">Imposta un valore che indica se nella finestra di dialogo credenziali viene visualizzata una casella di controllo che consente di salvare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="30290-121">Sets whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="30290-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="30290-122">Error codes</span></span>

<span data-ttu-id="30290-123">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="30290-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="30290-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30290-124">Requirements</span></span>



| <span data-ttu-id="30290-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="30290-125">Requirement</span></span> | <span data-ttu-id="30290-126">Valore</span><span class="sxs-lookup"><span data-stu-id="30290-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30290-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30290-127">Minimum supported client</span></span><br/> | <span data-ttu-id="30290-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30290-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="30290-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30290-129">Minimum supported server</span></span><br/> | <span data-ttu-id="30290-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30290-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="30290-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="30290-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="30290-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30290-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="30290-133">DLL</span><span class="sxs-lookup"><span data-stu-id="30290-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30290-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30290-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="30290-135">IID</span><span class="sxs-lookup"><span data-stu-id="30290-135">IID</span></span><br/>                      | <span data-ttu-id="30290-136">IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="30290-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="30290-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30290-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30290-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="30290-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="30290-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="30290-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





