---
title: Proprietà EnableAutoReconnect di IMsRdpClientAdvancedSettings2
description: Specifica se abilitare il controllo client per la riconnessione automatica a una sessione in caso di disconnessione di rete.
ms.assetid: 9d820f78-bf7f-479a-ae6f-be0f0abe549c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà EnableAutoReconnect
- Servizi Desktop remoto proprietà EnableAutoReconnect, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà EnableAutoReconnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.put_EnableAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f8d4a1345395b5b5843872df256fe7a113094e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301993"
---
# <a name="imsrdpclientadvancedsettings2enableautoreconnect-property"></a><span data-ttu-id="08a87-118">Proprietà IMsRdpClientAdvancedSettings2:: EnableAutoReconnect</span><span class="sxs-lookup"><span data-stu-id="08a87-118">IMsRdpClientAdvancedSettings2::EnableAutoReconnect property</span></span>

<span data-ttu-id="08a87-119">Specifica se abilitare il controllo client per la riconnessione automatica a una sessione in caso di disconnessione di rete.</span><span class="sxs-lookup"><span data-stu-id="08a87-119">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span>

<span data-ttu-id="08a87-120">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="08a87-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a87-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08a87-121">Syntax</span></span>


```C++
HRESULT put_EnableAutoReconnect(
  [in]  VARIANT_BOOL fEnableAutoReconnect
);

HRESULT get_EnableAutoReconnect(
  [out] VARIANT_BOOL *pfEnableAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="08a87-122">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="08a87-122">Property value</span></span>

<span data-ttu-id="08a87-123">Impostare su **Variant \_ true** per abilitare la riconnessione automatica e su **Variant \_ false** per disabilitarla.</span><span class="sxs-lookup"><span data-stu-id="08a87-123">Set to **VARIANT\_TRUE** to enable automatic reconnection, and to **VARIANT\_FALSE** to disable it.</span></span> <span data-ttu-id="08a87-124">Il valore predefinito è **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="08a87-124">The default is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="08a87-125">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="08a87-125">Error codes</span></span>

<span data-ttu-id="08a87-126">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="08a87-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a87-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="08a87-127">Remarks</span></span>

<span data-ttu-id="08a87-128">Impossibile impostare questa proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="08a87-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="08a87-129">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="08a87-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="08a87-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08a87-130">Requirements</span></span>



| <span data-ttu-id="08a87-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="08a87-131">Requirement</span></span> | <span data-ttu-id="08a87-132">Valore</span><span class="sxs-lookup"><span data-stu-id="08a87-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a87-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08a87-133">Minimum supported client</span></span><br/> | <span data-ttu-id="08a87-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08a87-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="08a87-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08a87-135">Minimum supported server</span></span><br/> | <span data-ttu-id="08a87-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08a87-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="08a87-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="08a87-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="08a87-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a87-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="08a87-139">DLL</span><span class="sxs-lookup"><span data-stu-id="08a87-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08a87-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a87-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="08a87-141">IID</span><span class="sxs-lookup"><span data-stu-id="08a87-141">IID</span></span><br/>                      | <span data-ttu-id="08a87-142">IID \_ IMsRdpClientAdvancedSettings2 è definito come 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="08a87-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08a87-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08a87-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a87-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="08a87-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="08a87-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="08a87-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="08a87-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="08a87-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="08a87-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="08a87-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="08a87-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="08a87-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="08a87-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="08a87-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="08a87-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="08a87-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





