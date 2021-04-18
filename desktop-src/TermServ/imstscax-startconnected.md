---
title: Proprietà StartConnected di IMsTscAx
description: Indica se il controllo stabilirà la connessione al server host sessione Desktop remoto (host sessione Desktop remoto) immediatamente all'avvio.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà StartConnected
- Servizi Desktop remoto proprietà StartConnected, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà StartConnected
- Servizi Desktop remoto proprietà StartConnected, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà StartConnected
- Servizi Desktop remoto proprietà StartConnected, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà StartConnected
- Servizi Desktop remoto proprietà StartConnected, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà StartConnected
- Servizi Desktop remoto proprietà StartConnected, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà StartConnected
- Servizi Desktop remoto proprietà StartConnected, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà StartConnected
- Servizi Desktop remoto proprietà StartConnected, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà StartConnected
- Servizi Desktop remoto proprietà StartConnected, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà StartConnected
- Servizi Desktop remoto proprietà StartConnected, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà StartConnected
- Servizi Desktop remoto proprietà StartConnected, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà StartConnected
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bda77a06723a6df63055374a3fc96cb80f7654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301108"
---
# <a name="imstscaxstartconnected-property"></a><span data-ttu-id="efbc7-124">Proprietà IMsTscAx:: StartConnected</span><span class="sxs-lookup"><span data-stu-id="efbc7-124">IMsTscAx::StartConnected property</span></span>

<span data-ttu-id="efbc7-125">Indica se il controllo stabilirà la connessione al server host sessione Desktop remoto (host sessione Desktop remoto) immediatamente all'avvio.</span><span class="sxs-lookup"><span data-stu-id="efbc7-125">Indicates whether the control will establish the Remote Desktop Session Host (RD Session Host) server connection immediately upon startup.</span></span>

<span data-ttu-id="efbc7-126">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="efbc7-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="efbc7-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efbc7-127">Syntax</span></span>


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a><span data-ttu-id="efbc7-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="efbc7-128">Property value</span></span>

<span data-ttu-id="efbc7-129">Impostare questo parametro su **true** se il controllo deve connettersi immediatamente all'avvio o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="efbc7-129">Set this parameter to **TRUE** if the control should connect immediately on startup, or **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="efbc7-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="efbc7-130">Error codes</span></span>

<span data-ttu-id="efbc7-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="efbc7-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="efbc7-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="efbc7-132">Remarks</span></span>

<span data-ttu-id="efbc7-133">Questa proprietà è particolarmente utile quando le proprietà del controllo sono impostate nell'elenco di parametri di un <OBJECT> tag, anziché tramite chiamate di script.</span><span class="sxs-lookup"><span data-stu-id="efbc7-133">This property is most useful when the control properties are set in the parameter list of an <OBJECT> tag, rather than through script calls.</span></span>

<span data-ttu-id="efbc7-134">Questa proprietà può essere utilizzata solo se il nome del server viene specificato anche utilizzando la proprietà server.</span><span class="sxs-lookup"><span data-stu-id="efbc7-134">This property can be used only if the server name is also specified using the server property.</span></span> <span data-ttu-id="efbc7-135">Questo parametro deve essere impostato prima che il controllo venga avviato, ad esempio, inserendolo nell'elenco di parametri di un <OBJECT> tag quando si usa il controllo da una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="efbc7-135">This parameter has to be set before the control starts up for example, by including it in the parameter list of an <OBJECT> tag when using the control from a webpage.</span></span>

<span data-ttu-id="efbc7-136">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="efbc7-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="efbc7-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efbc7-137">Requirements</span></span>



| <span data-ttu-id="efbc7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="efbc7-138">Requirement</span></span> | <span data-ttu-id="efbc7-139">Valore</span><span class="sxs-lookup"><span data-stu-id="efbc7-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efbc7-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efbc7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="efbc7-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efbc7-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="efbc7-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="efbc7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="efbc7-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efbc7-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="efbc7-144">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="efbc7-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="efbc7-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efbc7-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="efbc7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="efbc7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efbc7-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efbc7-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="efbc7-148">IID</span><span class="sxs-lookup"><span data-stu-id="efbc7-148">IID</span></span><br/>                      | <span data-ttu-id="efbc7-149">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="efbc7-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="efbc7-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efbc7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efbc7-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="efbc7-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="efbc7-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="efbc7-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="efbc7-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="efbc7-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="efbc7-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="efbc7-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="efbc7-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="efbc7-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="efbc7-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="efbc7-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="efbc7-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="efbc7-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="efbc7-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="efbc7-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="efbc7-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="efbc7-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="efbc7-160">Incorporamento del controllo ActiveX Desktop remoto in una pagina Web</span><span class="sxs-lookup"><span data-stu-id="efbc7-160">Embedding the Remote Desktop ActiveX Control in a Webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[<span data-ttu-id="efbc7-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="efbc7-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





