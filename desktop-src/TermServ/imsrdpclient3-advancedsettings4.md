---
title: Proprietà AdvancedSettings4 di IMsRdpClient3
description: Recupera un puntatore all'interfaccia IMsRdpClientAdvancedSettings3.
ms.assetid: 30935099-7f33-4745-8a31-f9a28ab78b63
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings4
- Servizi Desktop remoto proprietà AdvancedSettings4, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà AdvancedSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient3.AdvancedSettings4
- IMsRdpClient3.get_AdvancedSettings4
- IMsRdpClient4.AdvancedSettings4
- IMsRdpClient4.get_AdvancedSettings4
- IMsRdpClient5.AdvancedSettings4
- IMsRdpClient5.get_AdvancedSettings4
- IMsRdpClient6.AdvancedSettings4
- IMsRdpClient6.get_AdvancedSettings4
- IMsRdpClient7.AdvancedSettings4
- IMsRdpClient7.get_AdvancedSettings4
- IMsRdpClient8.AdvancedSettings4
- IMsRdpClient8.get_AdvancedSettings4
- IMsRdpClient9.AdvancedSettings4
- IMsRdpClient9.get_AdvancedSettings4
- IMsRdpClient10.AdvancedSettings4
- IMsRdpClient10.get_AdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a229c28b645e7920212a04cc44ca5a9ce42be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873449"
---
# <a name="imsrdpclient3advancedsettings4-property"></a><span data-ttu-id="f4c92-120">Proprietà IMsRdpClient3:: AdvancedSettings4</span><span class="sxs-lookup"><span data-stu-id="f4c92-120">IMsRdpClient3::AdvancedSettings4 property</span></span>

<span data-ttu-id="f4c92-121">Recupera un puntatore all'interfaccia [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="f4c92-121">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span>

<span data-ttu-id="f4c92-122">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f4c92-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c92-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4c92-123">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings4(
  [out] IMsRdpClientAdvancedSettings3 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="f4c92-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f4c92-124">Property value</span></span>

<span data-ttu-id="f4c92-125">Puntatore all'interfaccia [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="f4c92-125">Pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="f4c92-126">L'interfaccia può essere utilizzata per impostare impostazioni avanzate per il controllo client.</span><span class="sxs-lookup"><span data-stu-id="f4c92-126">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f4c92-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f4c92-127">Error codes</span></span>

<span data-ttu-id="f4c92-128">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="f4c92-128">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="f4c92-129">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="f4c92-129">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4c92-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4c92-130">Remarks</span></span>

<span data-ttu-id="f4c92-131">Impossibile impostare questa proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="f4c92-131">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="f4c92-132">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f4c92-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4c92-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4c92-133">Requirements</span></span>



| <span data-ttu-id="f4c92-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4c92-134">Requirement</span></span> | <span data-ttu-id="f4c92-135">Valore</span><span class="sxs-lookup"><span data-stu-id="f4c92-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c92-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4c92-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c92-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4c92-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f4c92-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4c92-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c92-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4c92-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f4c92-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f4c92-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="f4c92-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4c92-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f4c92-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f4c92-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4c92-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4c92-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f4c92-144">IID</span><span class="sxs-lookup"><span data-stu-id="f4c92-144">IID</span></span><br/>                      | <span data-ttu-id="f4c92-145">IID \_ IMsRdpClient3 è definito come 91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span><span class="sxs-lookup"><span data-stu-id="f4c92-145">IID\_IMsRdpClient3 is defined as 91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f4c92-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4c92-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c92-147">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="f4c92-147">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="f4c92-148">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="f4c92-148">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="f4c92-149">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="f4c92-149">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="f4c92-150">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f4c92-150">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f4c92-151">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f4c92-151">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f4c92-152">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f4c92-152">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f4c92-153">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f4c92-153">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f4c92-154">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="f4c92-154">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





