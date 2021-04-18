---
title: Proprietà MaxReconnectAttempts di IMsRdpClientAdvancedSettings2
description: Specifica il numero di tentativi di riconnessione durante la riconnessione automatica.
ms.assetid: 24bfd3b6-d2de-4e46-8b5f-a4702c18a93c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà MaxReconnectAttempts
- Servizi Desktop remoto proprietà MaxReconnectAttempts, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà MaxReconnectAttempts
- Servizi Desktop remoto proprietà MaxReconnectAttempts, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà MaxReconnectAttempts
- Servizi Desktop remoto proprietà MaxReconnectAttempts, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà MaxReconnectAttempts
- Servizi Desktop remoto proprietà MaxReconnectAttempts, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà MaxReconnectAttempts
- Servizi Desktop remoto proprietà MaxReconnectAttempts, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà MaxReconnectAttempts
- Servizi Desktop remoto proprietà MaxReconnectAttempts, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà MaxReconnectAttempts
- Servizi Desktop remoto proprietà MaxReconnectAttempts, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà MaxReconnectAttempts
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.put_MaxReconnectAttempts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322796a2d6ca6a13476dad58af8c385b8bdfa1fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301992"
---
# <a name="imsrdpclientadvancedsettings2maxreconnectattempts-property"></a><span data-ttu-id="887fa-118">Proprietà IMsRdpClientAdvancedSettings2:: MaxReconnectAttempts</span><span class="sxs-lookup"><span data-stu-id="887fa-118">IMsRdpClientAdvancedSettings2::MaxReconnectAttempts property</span></span>

<span data-ttu-id="887fa-119">Specifica il numero di tentativi di riconnessione durante la riconnessione automatica.</span><span class="sxs-lookup"><span data-stu-id="887fa-119">Specifies the number of times to try to reconnect during automatic reconnection.</span></span>

<span data-ttu-id="887fa-120">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="887fa-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="887fa-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="887fa-121">Syntax</span></span>


```C++
HRESULT put_MaxReconnectAttempts(
  [in]  LONG MaxReconnectAttempts
);

HRESULT get_MaxReconnectAttempts(
  [out] LONG *pMaxReconnectAttempts
);
```



## <a name="property-value"></a><span data-ttu-id="887fa-122">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="887fa-122">Property value</span></span>

<span data-ttu-id="887fa-123">Nuovo numero di tentativi.</span><span class="sxs-lookup"><span data-stu-id="887fa-123">The new number of retries.</span></span> <span data-ttu-id="887fa-124">I valori validi sono compresi tra 0 e 200, inclusi.</span><span class="sxs-lookup"><span data-stu-id="887fa-124">The valid values are 0 to 200, inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="887fa-125">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="887fa-125">Error codes</span></span>

<span data-ttu-id="887fa-126">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="887fa-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="887fa-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="887fa-127">Remarks</span></span>

<span data-ttu-id="887fa-128">Impossibile impostare questa proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="887fa-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="887fa-129">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="887fa-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="887fa-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="887fa-130">Requirements</span></span>



| <span data-ttu-id="887fa-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="887fa-131">Requirement</span></span> | <span data-ttu-id="887fa-132">Valore</span><span class="sxs-lookup"><span data-stu-id="887fa-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="887fa-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="887fa-133">Minimum supported client</span></span><br/> | <span data-ttu-id="887fa-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="887fa-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="887fa-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="887fa-135">Minimum supported server</span></span><br/> | <span data-ttu-id="887fa-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="887fa-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="887fa-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="887fa-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="887fa-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="887fa-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="887fa-139">DLL</span><span class="sxs-lookup"><span data-stu-id="887fa-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="887fa-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="887fa-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="887fa-141">IID</span><span class="sxs-lookup"><span data-stu-id="887fa-141">IID</span></span><br/>                      | <span data-ttu-id="887fa-142">IID \_ IMsRdpClientAdvancedSettings2 è definito come 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="887fa-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="887fa-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="887fa-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887fa-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="887fa-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="887fa-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="887fa-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="887fa-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="887fa-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="887fa-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="887fa-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="887fa-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="887fa-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="887fa-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="887fa-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="887fa-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="887fa-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





