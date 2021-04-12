---
title: Proprietà MarkRdpSettingsSecure di IMsRdpClientNonScriptable4
description: Specifica se le impostazioni di Remote Desktop Protocol (RDP) sono contrassegnate come sicure.
ms.assetid: 04b419ed-821e-43e0-ac76-b8d6f6dfcc30
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà MarkRdpSettingsSecure
- Servizi Desktop remoto proprietà MarkRdpSettingsSecure, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà MarkRdpSettingsSecure
- Servizi Desktop remoto proprietà MarkRdpSettingsSecure, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà MarkRdpSettingsSecure
- Servizi Desktop remoto proprietà MarkRdpSettingsSecure, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà MarkRdpSettingsSecure
- Servizi Desktop remoto proprietà MarkRdpSettingsSecure, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà MarkRdpSettingsSecure
- Servizi Desktop remoto proprietà MarkRdpSettingsSecure, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà MarkRdpSettingsSecure
- Servizi Desktop remoto proprietà MarkRdpSettingsSecure, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà MarkRdpSettingsSecure
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.put_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.put_MarkRdpSettingsSecure
- MsRdpClient6.MarkRdpSettingsSecure
- MsRdpClient7.MarkRdpSettingsSecure
- MsRdpClient8.MarkRdpSettingsSecure
- MsRdpClient9.MarkRdpSettingsSecure
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b551e043432b6f6e66efbbe5a6e0f9095024a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518064"
---
# <a name="imsrdpclientnonscriptable4markrdpsettingssecure-property"></a><span data-ttu-id="597e0-116">Proprietà IMsRdpClientNonScriptable4:: MarkRdpSettingsSecure</span><span class="sxs-lookup"><span data-stu-id="597e0-116">IMsRdpClientNonScriptable4::MarkRdpSettingsSecure property</span></span>

<span data-ttu-id="597e0-117">Specifica se le impostazioni di [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) sono contrassegnate come sicure.</span><span class="sxs-lookup"><span data-stu-id="597e0-117">Specifies whether [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) settings are marked as secure.</span></span> <span data-ttu-id="597e0-118">Ciò indica che le impostazioni applicate al controllo sono state firmate da un autore attendibile o di terze parti.</span><span class="sxs-lookup"><span data-stu-id="597e0-118">This indicates that the settings applied to the control have been signed by a third-party or trusted publisher.</span></span>

<span data-ttu-id="597e0-119">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="597e0-119">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="597e0-120">Sintassi</span><span class="sxs-lookup"><span data-stu-id="597e0-120">Syntax</span></span>


```C++
HRESULT put_MarkRdpSettingsSecure(
  [in]  VARIANT_BOOL fRdpSecure
);

HRESULT get_MarkRdpSettingsSecure(
  [out] VARIANT_BOOL *pfRdpSecure
);
```



## <a name="property-value"></a><span data-ttu-id="597e0-121">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="597e0-121">Property value</span></span>

<span data-ttu-id="597e0-122">Consente di specificare se le impostazioni RDP sono contrassegnate come sicure.</span><span class="sxs-lookup"><span data-stu-id="597e0-122">Sets whether RDP settings are marked as secure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="597e0-123">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="597e0-123">Error codes</span></span>

<span data-ttu-id="597e0-124">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="597e0-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="597e0-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="597e0-125">Requirements</span></span>



| <span data-ttu-id="597e0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="597e0-126">Requirement</span></span> | <span data-ttu-id="597e0-127">Valore</span><span class="sxs-lookup"><span data-stu-id="597e0-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="597e0-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="597e0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="597e0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="597e0-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="597e0-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="597e0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="597e0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="597e0-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="597e0-132">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="597e0-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="597e0-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="597e0-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="597e0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="597e0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="597e0-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="597e0-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="597e0-136">IID</span><span class="sxs-lookup"><span data-stu-id="597e0-136">IID</span></span><br/>                      | <span data-ttu-id="597e0-137">IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="597e0-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="597e0-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="597e0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="597e0-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="597e0-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="597e0-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="597e0-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





