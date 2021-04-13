---
title: Proprietà AdvancedSettings5 di IMsRdpClient4
description: Recupera un puntatore a un'interfaccia IMsRdpClientAdvancedSettings4.
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings5
- Servizi Desktop remoto proprietà AdvancedSettings5, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto, proprietà AdvancedSettings5
- Servizi Desktop remoto proprietà AdvancedSettings5, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà AdvancedSettings5
- Servizi Desktop remoto proprietà AdvancedSettings5, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà AdvancedSettings5
- Servizi Desktop remoto proprietà AdvancedSettings5, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà AdvancedSettings5
- Servizi Desktop remoto proprietà AdvancedSettings5, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings5
- Servizi Desktop remoto proprietà AdvancedSettings5, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings5
- Servizi Desktop remoto proprietà AdvancedSettings5, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà AdvancedSettings5
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad96588b2109375aed23c1024ef925936cb3368
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519018"
---
# <a name="imsrdpclient4advancedsettings5-property"></a><span data-ttu-id="e8238-118">Proprietà IMsRdpClient4:: AdvancedSettings5</span><span class="sxs-lookup"><span data-stu-id="e8238-118">IMsRdpClient4::AdvancedSettings5 property</span></span>

<span data-ttu-id="e8238-119">Recupera un puntatore a un'interfaccia [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="e8238-119">Retrieves a pointer to an [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="e8238-120">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e8238-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8238-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8238-121">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="e8238-122">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e8238-122">Property value</span></span>

<span data-ttu-id="e8238-123">Puntatore all'interfaccia [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="e8238-123">A pointer to the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span> <span data-ttu-id="e8238-124">L'interfaccia può essere utilizzata per impostare impostazioni avanzate per il controllo client.</span><span class="sxs-lookup"><span data-stu-id="e8238-124">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e8238-125">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e8238-125">Error codes</span></span>

<span data-ttu-id="e8238-126">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="e8238-126">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="e8238-127">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e8238-127">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8238-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8238-128">Remarks</span></span>

<span data-ttu-id="e8238-129">Impossibile impostare questa proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="e8238-129">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="e8238-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e8238-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8238-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8238-131">Requirements</span></span>



| <span data-ttu-id="e8238-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8238-132">Requirement</span></span> | <span data-ttu-id="e8238-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e8238-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8238-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8238-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e8238-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8238-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e8238-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8238-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e8238-137">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="e8238-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="e8238-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e8238-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8238-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8238-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e8238-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e8238-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8238-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8238-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e8238-142">IID</span><span class="sxs-lookup"><span data-stu-id="e8238-142">IID</span></span><br/>                      | <span data-ttu-id="e8238-143">IMsRdpClient4 è definito come 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span><span class="sxs-lookup"><span data-stu-id="e8238-143">IMsRdpClient4 is defined as 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e8238-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8238-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8238-145">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e8238-145">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e8238-146">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e8238-146">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e8238-147">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e8238-147">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e8238-148">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e8238-148">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e8238-149">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e8238-149">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e8238-150">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e8238-150">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e8238-151">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e8238-151">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





