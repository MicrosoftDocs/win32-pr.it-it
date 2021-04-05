---
title: Proprietà CanAutoReconnect di IMsRdpClientAdvancedSettings2
description: Specifica se il controllo client è in grado di riconnettersi automaticamente alla sessione corrente in caso di disconnessione di rete.
ms.assetid: 0a7ecf90-832b-4ec1-990b-7fe26ff134b1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà CanAutoReconnect
- Servizi Desktop remoto proprietà CanAutoReconnect, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà CanAutoReconnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.CanAutoReconnect
- IMsRdpClientAdvancedSettings2.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings3.CanAutoReconnect
- IMsRdpClientAdvancedSettings3.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings4.CanAutoReconnect
- IMsRdpClientAdvancedSettings4.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings5.CanAutoReconnect
- IMsRdpClientAdvancedSettings5.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings6.CanAutoReconnect
- IMsRdpClientAdvancedSettings6.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings7.CanAutoReconnect
- IMsRdpClientAdvancedSettings7.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings8.CanAutoReconnect
- IMsRdpClientAdvancedSettings8.get_CanAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8c8f4113c39b79783978252136c50d2111ed0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873337"
---
# <a name="imsrdpclientadvancedsettings2canautoreconnect-property"></a><span data-ttu-id="c8916-118">Proprietà IMsRdpClientAdvancedSettings2:: CanAutoReconnect</span><span class="sxs-lookup"><span data-stu-id="c8916-118">IMsRdpClientAdvancedSettings2::CanAutoReconnect property</span></span>

<span data-ttu-id="c8916-119">Specifica se il controllo client è in grado di riconnettersi automaticamente alla sessione corrente in caso di disconnessione di rete.</span><span class="sxs-lookup"><span data-stu-id="c8916-119">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span>

<span data-ttu-id="c8916-120">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c8916-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8916-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8916-121">Syntax</span></span>


```C++
HRESULT get_CanAutoReconnect(
  [out] VARIANT_BOOL *pfCanAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="c8916-122">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c8916-122">Property value</span></span>

<span data-ttu-id="c8916-123">Riceve la **variante \_ true** se il controllo è in grado di riconnettersi automaticamente e **Variant \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c8916-123">Receives **VARIANT\_TRUE** if the control is able to automatically reconnect, and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8916-124">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c8916-124">Error codes</span></span>

<span data-ttu-id="c8916-125">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="c8916-125">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8916-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8916-126">Remarks</span></span>

<span data-ttu-id="c8916-127">Le situazioni in cui la riconnessione automatica potrebbe non essere abilitata includono quelle in cui un amministratore usa i criteri di gruppo per disabilitare autoreconnection e gli ambienti legacy che non supportano la riconnessione automatica.</span><span class="sxs-lookup"><span data-stu-id="c8916-127">Situations in which automatic reconnection might not be enabled include those in which an administrator uses group policy to disable autoreconnection, and legacy environments that do not support automatic reconnection.</span></span>

<span data-ttu-id="c8916-128">Impossibile impostare questa proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="c8916-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="c8916-129">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c8916-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8916-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8916-130">Requirements</span></span>



| <span data-ttu-id="c8916-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8916-131">Requirement</span></span> | <span data-ttu-id="c8916-132">Valore</span><span class="sxs-lookup"><span data-stu-id="c8916-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8916-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8916-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c8916-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8916-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="c8916-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8916-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c8916-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8916-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="c8916-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c8916-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="c8916-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8916-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c8916-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c8916-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8916-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8916-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c8916-141">IID</span><span class="sxs-lookup"><span data-stu-id="c8916-141">IID</span></span><br/>                      | <span data-ttu-id="c8916-142">IID \_ IMsRdpClientAdvancedSettings2 è definito come 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="c8916-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8916-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8916-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8916-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c8916-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c8916-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c8916-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c8916-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c8916-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c8916-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c8916-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c8916-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c8916-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c8916-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c8916-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c8916-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c8916-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





