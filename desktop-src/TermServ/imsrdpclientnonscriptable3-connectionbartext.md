---
title: Proprietà ConnectionBarText di IMsRdpClientNonScriptable3
description: Imposta o Recupera il testo per aggiornare la barra di connessione.
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ConnectionBarText
- Servizi Desktop remoto proprietà ConnectionBarText, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà ConnectionBarText
- Servizi Desktop remoto proprietà ConnectionBarText, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà ConnectionBarText
- Servizi Desktop remoto proprietà ConnectionBarText, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà ConnectionBarText
- Servizi Desktop remoto proprietà ConnectionBarText, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà ConnectionBarText
- Servizi Desktop remoto proprietà ConnectionBarText, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà ConnectionBarText
- Servizi Desktop remoto proprietà ConnectionBarText, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà ConnectionBarText
- Servizi Desktop remoto proprietà ConnectionBarText, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà ConnectionBarText
- Servizi Desktop remoto proprietà ConnectionBarText, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà ConnectionBarText
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ConnectionBarText
- IMsRdpClientNonScriptable3.get_ConnectionBarText
- IMsRdpClientNonScriptable3.put_ConnectionBarText
- IMsRdpClientNonScriptable4.ConnectionBarText
- IMsRdpClientNonScriptable4.get_ConnectionBarText
- IMsRdpClientNonScriptable4.put_ConnectionBarText
- IMsRdpClientNonScriptable5.ConnectionBarText
- IMsRdpClientNonScriptable5.get_ConnectionBarText
- IMsRdpClientNonScriptable5.put_ConnectionBarText
- MsRdpClient5.ConnectionBarText
- MsRdpClient6.ConnectionBarText
- MsRdpClient7.ConnectionBarText
- MsRdpClient8.ConnectionBarText
- MsRdpClient9.ConnectionBarText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76819dd28ffd8b2ee5e2dfb30017e341dd49db5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743295"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a><span data-ttu-id="91181-120">Proprietà IMsRdpClientNonScriptable3:: ConnectionBarText</span><span class="sxs-lookup"><span data-stu-id="91181-120">IMsRdpClientNonScriptable3::ConnectionBarText property</span></span>

<span data-ttu-id="91181-121">Imposta o Recupera il testo per aggiornare la barra di connessione.</span><span class="sxs-lookup"><span data-stu-id="91181-121">Sets or retrieves the text to update the connection bar.</span></span>

<span data-ttu-id="91181-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="91181-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="91181-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91181-123">Syntax</span></span>


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a><span data-ttu-id="91181-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="91181-124">Property value</span></span>

<span data-ttu-id="91181-125">Imposta la stringa di testo da visualizzare sulla barra di connessione.</span><span class="sxs-lookup"><span data-stu-id="91181-125">Sets the text string to display on the connection bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="91181-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="91181-126">Remarks</span></span>

<span data-ttu-id="91181-127">È necessario chiamare il metodo **IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText** prima di chiamare il metodo [**IMsTscSecuredSettings::P UT \_ FullScreen**](imstscsecuredsettings-fullscreen.md) o [**IMsRdpClient::p UT \_ FullScreen**](imsrdpclient-fullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="91181-127">You must call the **IMsRdpClientNonScriptable3::put\_ConnectionBarText** method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="91181-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91181-128">Requirements</span></span>



| <span data-ttu-id="91181-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="91181-129">Requirement</span></span> | <span data-ttu-id="91181-130">Valore</span><span class="sxs-lookup"><span data-stu-id="91181-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91181-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91181-131">Minimum supported client</span></span><br/> | <span data-ttu-id="91181-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91181-132">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="91181-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91181-133">Minimum supported server</span></span><br/> | <span data-ttu-id="91181-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91181-134">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="91181-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="91181-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="91181-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91181-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="91181-137">DLL</span><span class="sxs-lookup"><span data-stu-id="91181-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91181-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91181-138"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="91181-139">IID</span><span class="sxs-lookup"><span data-stu-id="91181-139">IID</span></span><br/>                      | <span data-ttu-id="91181-140">IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="91181-140">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91181-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91181-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91181-142">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="91181-142">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="91181-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="91181-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="91181-144">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="91181-144">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





