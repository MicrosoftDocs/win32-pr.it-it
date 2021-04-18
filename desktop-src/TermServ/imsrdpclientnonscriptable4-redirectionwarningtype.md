---
title: Proprietà RedirectionWarningType di IMsRdpClientNonScriptable4
description: Controlla la presenza e l'aspetto della finestra di dialogo che informa l'utente del reindirizzamento.
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà RedirectionWarningType
- Servizi Desktop remoto proprietà RedirectionWarningType, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà RedirectionWarningType
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301888"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a><span data-ttu-id="7960b-116">Proprietà IMsRdpClientNonScriptable4:: RedirectionWarningType</span><span class="sxs-lookup"><span data-stu-id="7960b-116">IMsRdpClientNonScriptable4::RedirectionWarningType property</span></span>

<span data-ttu-id="7960b-117">Controlla la presenza e l'aspetto della finestra di dialogo che informa l'utente del reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="7960b-117">Controls the presence and appearance of the dialog box that notifies the user about redirection.</span></span>

<span data-ttu-id="7960b-118">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7960b-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7960b-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7960b-119">Syntax</span></span>


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a><span data-ttu-id="7960b-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7960b-120">Property value</span></span>

<span data-ttu-id="7960b-121">Imposta il tipo della finestra di dialogo che informa l'utente del reindirizzamento.</span><span class="sxs-lookup"><span data-stu-id="7960b-121">Sets the type of the dialog box that notifies the user of redirection.</span></span>

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span data-ttu-id="7960b-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)</span><span class="sxs-lookup"><span data-stu-id="7960b-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="7960b-123">La finestra di dialogo non è specifica del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="7960b-123">The dialog box is not publisher specific.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span data-ttu-id="7960b-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="7960b-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="7960b-125">La finestra di dialogo è per i file non firmati.</span><span class="sxs-lookup"><span data-stu-id="7960b-125">The dialog box is for unsigned files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span data-ttu-id="7960b-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="7960b-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="7960b-127">La finestra di dialogo è destinata a un server di pubblicazione sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="7960b-127">The dialog box is for an unknown publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span data-ttu-id="7960b-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)</span><span class="sxs-lookup"><span data-stu-id="7960b-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)</span></span>


</dt> <dd>

<span data-ttu-id="7960b-129">La finestra di dialogo è relativa ai file dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7960b-129">The dialog box is for the user's files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span data-ttu-id="7960b-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="7960b-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)</span></span>


</dt> <dd>

<span data-ttu-id="7960b-131">La finestra di dialogo viene visualizzata per i file firmati con certificazione di terze parti.</span><span class="sxs-lookup"><span data-stu-id="7960b-131">The dialog box is displayed for third-party-certified, signed files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span data-ttu-id="7960b-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="7960b-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="7960b-133">La finestra di dialogo non viene visualizzata perché l'applicazione è pubblicata da un autore attendibile.</span><span class="sxs-lookup"><span data-stu-id="7960b-133">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span data-ttu-id="7960b-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="7960b-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="7960b-135">La finestra di dialogo non viene visualizzata perché l'applicazione è pubblicata da un autore attendibile.</span><span class="sxs-lookup"><span data-stu-id="7960b-135">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="7960b-136">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7960b-136">Error codes</span></span>

<span data-ttu-id="7960b-137">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7960b-137">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7960b-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="7960b-138">Remarks</span></span>

<span data-ttu-id="7960b-139">Il valore **RedirectionWarningTypeDefault**, che corrisponde al valore predefinito di questa proprietà, non esercita alcun controllo sulla finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="7960b-139">The value **RedirectionWarningTypeDefault**, which is the default value of this property, exerts no control over the dialog box.</span></span> <span data-ttu-id="7960b-140">In questo caso la proprietà di controllo è [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) in [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span><span class="sxs-lookup"><span data-stu-id="7960b-140">The controlling property in this case is [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) in [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7960b-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7960b-141">Requirements</span></span>



| <span data-ttu-id="7960b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="7960b-142">Requirement</span></span> | <span data-ttu-id="7960b-143">Valore</span><span class="sxs-lookup"><span data-stu-id="7960b-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7960b-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7960b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="7960b-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7960b-145">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7960b-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7960b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="7960b-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7960b-147">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7960b-148">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7960b-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="7960b-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7960b-149"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="7960b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="7960b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7960b-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7960b-151"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="7960b-152">IID</span><span class="sxs-lookup"><span data-stu-id="7960b-152">IID</span></span><br/>                      | <span data-ttu-id="7960b-153">IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="7960b-153">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7960b-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7960b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7960b-155">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="7960b-155">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="7960b-156">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="7960b-156">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





