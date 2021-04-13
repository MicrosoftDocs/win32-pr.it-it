---
title: Proprietà VerticalScrollBarVisible di IMsTscAx
description: Indica se il controllo Visualizza una barra di scorrimento verticale.
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
- Servizi Desktop remoto proprietà VerticalScrollBarVisible, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà VerticalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1365a0ab6d4a1411d78496cf157f3bc49fe5db15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475778"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a><span data-ttu-id="3b928-124">Proprietà IMsTscAx:: VerticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="3b928-124">IMsTscAx::VerticalScrollBarVisible property</span></span>

<span data-ttu-id="3b928-125">Indica se il controllo Visualizza una barra di scorrimento verticale.</span><span class="sxs-lookup"><span data-stu-id="3b928-125">Indicates whether the control displays a vertical scroll bar.</span></span>

<span data-ttu-id="3b928-126">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3b928-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b928-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b928-127">Syntax</span></span>


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="3b928-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3b928-128">Property value</span></span>

<span data-ttu-id="3b928-129">Il valore di questo parametro è **true** se la barra di scorrimento verticale è visibile e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3b928-129">The value of this parameter is **TRUE** if the vertical scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3b928-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="3b928-130">Error codes</span></span>

<span data-ttu-id="3b928-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="3b928-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b928-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b928-132">Remarks</span></span>

<span data-ttu-id="3b928-133">Il controllo Visualizza automaticamente una barra di scorrimento verticale se l'altezza del controllo corrente è minore dell'altezza del desktop.</span><span class="sxs-lookup"><span data-stu-id="3b928-133">The control automatically displays a vertical scroll bar if the height of the current control is less than the height of the desktop.</span></span>

<span data-ttu-id="3b928-134">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3b928-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b928-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b928-135">Requirements</span></span>



| <span data-ttu-id="3b928-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b928-136">Requirement</span></span> | <span data-ttu-id="3b928-137">Valore</span><span class="sxs-lookup"><span data-stu-id="3b928-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b928-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b928-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3b928-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b928-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3b928-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b928-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3b928-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b928-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3b928-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3b928-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b928-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b928-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b928-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3b928-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b928-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b928-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b928-146">IID</span><span class="sxs-lookup"><span data-stu-id="3b928-146">IID</span></span><br/>                      | <span data-ttu-id="3b928-147">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="3b928-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="3b928-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b928-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b928-149">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="3b928-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="3b928-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="3b928-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="3b928-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="3b928-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="3b928-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="3b928-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="3b928-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="3b928-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="3b928-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="3b928-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="3b928-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="3b928-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="3b928-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="3b928-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="3b928-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="3b928-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="3b928-158">**HorizontalScrollBarVisible**</span><span class="sxs-lookup"><span data-stu-id="3b928-158">**HorizontalScrollBarVisible**</span></span>](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[<span data-ttu-id="3b928-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="3b928-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





