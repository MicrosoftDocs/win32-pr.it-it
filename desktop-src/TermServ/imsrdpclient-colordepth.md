---
title: Proprietà ColorDepth di IMsRdpClient
description: Profondità di colore (in bit per pixel) per la connessione del controllo.
ms.assetid: 9ba4d8fe-20cd-40e9-a71a-0dce0ddd29fc
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ColorDepth
- Servizi Desktop remoto proprietà ColorDepth, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto, proprietà ColorDepth
- Servizi Desktop remoto proprietà ColorDepth, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto, proprietà ColorDepth
- Servizi Desktop remoto proprietà ColorDepth, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà ColorDepth
- Servizi Desktop remoto proprietà ColorDepth, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà ColorDepth
- Servizi Desktop remoto proprietà ColorDepth, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà ColorDepth
- Servizi Desktop remoto proprietà ColorDepth, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà ColorDepth
- Servizi Desktop remoto proprietà ColorDepth, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà ColorDepth
- Servizi Desktop remoto proprietà ColorDepth, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà ColorDepth
- Servizi Desktop remoto proprietà ColorDepth, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà ColorDepth
- Servizi Desktop remoto proprietà ColorDepth, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà ColorDepth
topic_type:
- apiref
api_name:
- IMsRdpClient.ColorDepth
- IMsRdpClient.get_ColorDepth
- IMsRdpClient.put_ColorDepth
- IMsRdpClient2.ColorDepth
- IMsRdpClient2.get_ColorDepth
- IMsRdpClient2.put_ColorDepth
- IMsRdpClient3.ColorDepth
- IMsRdpClient3.get_ColorDepth
- IMsRdpClient3.put_ColorDepth
- IMsRdpClient4.ColorDepth
- IMsRdpClient4.get_ColorDepth
- IMsRdpClient4.put_ColorDepth
- IMsRdpClient5.ColorDepth
- IMsRdpClient5.get_ColorDepth
- IMsRdpClient5.put_ColorDepth
- IMsRdpClient6.ColorDepth
- IMsRdpClient6.get_ColorDepth
- IMsRdpClient6.put_ColorDepth
- IMsRdpClient7.ColorDepth
- IMsRdpClient7.get_ColorDepth
- IMsRdpClient7.put_ColorDepth
- IMsRdpClient8.ColorDepth
- IMsRdpClient8.get_ColorDepth
- IMsRdpClient8.put_ColorDepth
- IMsRdpClient9.ColorDepth
- IMsRdpClient9.get_ColorDepth
- IMsRdpClient9.put_ColorDepth
- IMsRdpClient10.ColorDepth
- IMsRdpClient10.get_ColorDepth
- IMsRdpClient10.put_ColorDepth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5099deff3913d23173a466245cbf08fd5b95a6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121235"
---
# <a name="imsrdpclientcolordepth-property"></a><span data-ttu-id="9b418-124">Proprietà IMsRdpClient:: ColorDepth</span><span class="sxs-lookup"><span data-stu-id="9b418-124">IMsRdpClient::ColorDepth property</span></span>

<span data-ttu-id="9b418-125">Profondità di colore (in bit per pixel) per la connessione del controllo.</span><span class="sxs-lookup"><span data-stu-id="9b418-125">The color depth (in bits per pixel) for the control's connection.</span></span>

<span data-ttu-id="9b418-126">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9b418-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b418-127">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b418-127">Syntax</span></span>


```C++
HRESULT put_ColorDepth(
  [in]  LONG colorDepth
);

HRESULT get_ColorDepth(
  [out] LONG pcolorDepth
);
```



## <a name="property-value"></a><span data-ttu-id="9b418-128">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9b418-128">Property value</span></span>

<span data-ttu-id="9b418-129">Profondità del colore.</span><span class="sxs-lookup"><span data-stu-id="9b418-129">The color depth.</span></span> <span data-ttu-id="9b418-130">I valori includono 8, 15, 16, 24 e 32 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="9b418-130">Values include 8, 15, 16, 24, and 32 bits per pixel.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9b418-131">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="9b418-131">Error codes</span></span>

<span data-ttu-id="9b418-132">Se i metodi hanno esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="9b418-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="9b418-133">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="9b418-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b418-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="9b418-134">Remarks</span></span>

<span data-ttu-id="9b418-135">Impossibile impostare questa proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="9b418-135">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="9b418-136">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9b418-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b418-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b418-137">Requirements</span></span>



| <span data-ttu-id="9b418-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b418-138">Requirement</span></span> | <span data-ttu-id="9b418-139">Valore</span><span class="sxs-lookup"><span data-stu-id="9b418-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b418-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b418-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9b418-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b418-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9b418-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b418-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9b418-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b418-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9b418-144">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9b418-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="9b418-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b418-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b418-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9b418-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b418-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b418-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b418-148">IID</span><span class="sxs-lookup"><span data-stu-id="9b418-148">IID</span></span><br/>                      | <span data-ttu-id="9b418-149">IID \_ IMsRdpClient è definito come 92b4a539-7115-4B7C-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="9b418-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="9b418-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b418-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b418-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="9b418-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="9b418-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="9b418-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="9b418-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="9b418-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="9b418-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="9b418-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="9b418-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="9b418-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="9b418-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="9b418-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="9b418-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9b418-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9b418-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9b418-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9b418-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9b418-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9b418-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="9b418-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





