---
title: Proprietà HorizontalScrollBarVisible di IMsTscAx
description: Indica se il controllo ha visualizzato una barra di scorrimento orizzontale.
ms.assetid: d3c22c5f-321f-476e-bcdb-224eb988a7bb
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà HorizontalScrollBarVisible
- Servizi Desktop remoto proprietà HorizontalScrollBarVisible, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto, proprietà HorizontalScrollBarVisible
- Servizi Desktop remoto proprietà HorizontalScrollBarVisible, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà HorizontalScrollBarVisible
- Servizi Desktop remoto proprietà HorizontalScrollBarVisible, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà HorizontalScrollBarVisible
- Servizi Desktop remoto proprietà HorizontalScrollBarVisible, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà HorizontalScrollBarVisible
- Servizi Desktop remoto proprietà HorizontalScrollBarVisible, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà HorizontalScrollBarVisible
- Servizi Desktop remoto proprietà HorizontalScrollBarVisible, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà HorizontalScrollBarVisible
- Servizi Desktop remoto proprietà HorizontalScrollBarVisible, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà HorizontalScrollBarVisible
- Servizi Desktop remoto proprietà HorizontalScrollBarVisible, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà HorizontalScrollBarVisible
- Servizi Desktop remoto proprietà HorizontalScrollBarVisible, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà HorizontalScrollBarVisible
- Servizi Desktop remoto proprietà HorizontalScrollBarVisible, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà HorizontalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.HorizontalScrollBarVisible
- IMsTscAx.get_HorizontalScrollBarVisible
- IMsRdpClient.HorizontalScrollBarVisible
- IMsRdpClient.get_HorizontalScrollBarVisible
- IMsRdpClient2.HorizontalScrollBarVisible
- IMsRdpClient2.get_HorizontalScrollBarVisible
- IMsRdpClient3.HorizontalScrollBarVisible
- IMsRdpClient3.get_HorizontalScrollBarVisible
- IMsRdpClient4.HorizontalScrollBarVisible
- IMsRdpClient4.get_HorizontalScrollBarVisible
- IMsRdpClient5.HorizontalScrollBarVisible
- IMsRdpClient5.get_HorizontalScrollBarVisible
- IMsRdpClient6.HorizontalScrollBarVisible
- IMsRdpClient6.get_HorizontalScrollBarVisible
- IMsRdpClient7.HorizontalScrollBarVisible
- IMsRdpClient7.get_HorizontalScrollBarVisible
- IMsRdpClient8.HorizontalScrollBarVisible
- IMsRdpClient8.get_HorizontalScrollBarVisible
- IMsRdpClient9.HorizontalScrollBarVisible
- IMsRdpClient9.get_HorizontalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08fa2abb97a28af013e5791bcbd643f3f479d5c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048290"
---
# <a name="imstscaxhorizontalscrollbarvisible-property"></a><span data-ttu-id="c40b2-124">Proprietà IMsTscAx:: HorizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="c40b2-124">IMsTscAx::HorizontalScrollBarVisible property</span></span>

<span data-ttu-id="c40b2-125">Indica se il controllo ha visualizzato una barra di scorrimento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="c40b2-125">Indicates whether the control has displayed a horizontal scroll bar.</span></span>

<span data-ttu-id="c40b2-126">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c40b2-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c40b2-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c40b2-127">Syntax</span></span>


```C++
HRESULT get_HorizontalScrollBarVisible(
  [out] BOOL *pfHScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="c40b2-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c40b2-128">Property value</span></span>

<span data-ttu-id="c40b2-129">Il valore di questo parametro è **true** se la barra di scorrimento orizzontale è visibile e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c40b2-129">The value of this parameter is **TRUE** if the horizontal scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c40b2-130">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c40b2-130">Error codes</span></span>

<span data-ttu-id="c40b2-131">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="c40b2-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c40b2-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="c40b2-132">Remarks</span></span>

<span data-ttu-id="c40b2-133">Il controllo Visualizza automaticamente una barra di scorrimento orizzontale se la larghezza del controllo è inferiore alla larghezza del desktop.</span><span class="sxs-lookup"><span data-stu-id="c40b2-133">The control automatically displays a horizontal scroll bar if the width of the control is less than the desktop width.</span></span>

<span data-ttu-id="c40b2-134">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c40b2-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c40b2-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c40b2-135">Requirements</span></span>



| <span data-ttu-id="c40b2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c40b2-136">Requirement</span></span> | <span data-ttu-id="c40b2-137">Valore</span><span class="sxs-lookup"><span data-stu-id="c40b2-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c40b2-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c40b2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c40b2-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c40b2-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c40b2-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c40b2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c40b2-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c40b2-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c40b2-142">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c40b2-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="c40b2-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c40b2-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c40b2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c40b2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c40b2-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c40b2-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c40b2-146">IID</span><span class="sxs-lookup"><span data-stu-id="c40b2-146">IID</span></span><br/>                      | <span data-ttu-id="c40b2-147">IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="c40b2-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c40b2-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c40b2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c40b2-149">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="c40b2-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="c40b2-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="c40b2-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="c40b2-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="c40b2-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="c40b2-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="c40b2-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="c40b2-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="c40b2-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="c40b2-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="c40b2-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="c40b2-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="c40b2-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="c40b2-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c40b2-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c40b2-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c40b2-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c40b2-158">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="c40b2-158">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="c40b2-159">**VerticalScrollBarVisible**</span><span class="sxs-lookup"><span data-stu-id="c40b2-159">**VerticalScrollBarVisible**</span></span>](imstscax-verticalscrollbarvisible.md)
</dt> </dl>

 

 





