---
title: Proprietà shutdownTimeout di IMsRdpClientAdvancedSettings
description: Specifica il tempo di attesa, in secondi, per la risposta del server a una richiesta di disconnessione.
ms.assetid: 3fa935dc-d4b0-433b-ab67-a644fcf09006
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà shutdownTimeout
- Servizi Desktop remoto proprietà shutdownTimeout, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà shutdownTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.shutdownTimeout
- IMsRdpClientAdvancedSettings.get_shutdownTimeout
- IMsRdpClientAdvancedSettings.put_shutdownTimeout
- IMsRdpClientAdvancedSettings2.shutdownTimeout
- IMsRdpClientAdvancedSettings2.get_shutdownTimeout
- IMsRdpClientAdvancedSettings2.put_shutdownTimeout
- IMsRdpClientAdvancedSettings3.shutdownTimeout
- IMsRdpClientAdvancedSettings3.get_shutdownTimeout
- IMsRdpClientAdvancedSettings3.put_shutdownTimeout
- IMsRdpClientAdvancedSettings4.shutdownTimeout
- IMsRdpClientAdvancedSettings4.get_shutdownTimeout
- IMsRdpClientAdvancedSettings4.put_shutdownTimeout
- IMsRdpClientAdvancedSettings5.shutdownTimeout
- IMsRdpClientAdvancedSettings5.get_shutdownTimeout
- IMsRdpClientAdvancedSettings5.put_shutdownTimeout
- IMsRdpClientAdvancedSettings6.shutdownTimeout
- IMsRdpClientAdvancedSettings6.get_shutdownTimeout
- IMsRdpClientAdvancedSettings6.put_shutdownTimeout
- IMsRdpClientAdvancedSettings7.shutdownTimeout
- IMsRdpClientAdvancedSettings7.get_shutdownTimeout
- IMsRdpClientAdvancedSettings7.put_shutdownTimeout
- IMsRdpClientAdvancedSettings8.shutdownTimeout
- IMsRdpClientAdvancedSettings8.get_shutdownTimeout
- IMsRdpClientAdvancedSettings8.put_shutdownTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a011a0ce484f5bb2dd7d1ec610f4e3a436898
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400242"
---
# <a name="imsrdpclientadvancedsettingsshutdowntimeout-property"></a><span data-ttu-id="723b4-120">Proprietà IMsRdpClientAdvancedSettings:: shutdownTimeout</span><span class="sxs-lookup"><span data-stu-id="723b4-120">IMsRdpClientAdvancedSettings::shutdownTimeout property</span></span>

<span data-ttu-id="723b4-121">Specifica il tempo di attesa, in secondi, per la risposta del server a una richiesta di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="723b4-121">Specifies the length of time, in seconds, to wait for the server to respond to a disconnection request.</span></span>

<span data-ttu-id="723b4-122">Se il server non risponde entro il tempo specificato, il controllo client si disconnette.</span><span class="sxs-lookup"><span data-stu-id="723b4-122">If the server does not reply within the specified time, the client control disconnects.</span></span>

<span data-ttu-id="723b4-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="723b4-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="723b4-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="723b4-124">Syntax</span></span>


```C++
HRESULT put_shutdownTimeout(
  [in]  LONG shutdownTimeout
);

HRESULT get_shutdownTimeout(
  [out] LONG *pshutdownTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="723b4-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="723b4-125">Property value</span></span>

<span data-ttu-id="723b4-126">Nuova ora, in secondi.</span><span class="sxs-lookup"><span data-stu-id="723b4-126">The new time, in seconds.</span></span> <span data-ttu-id="723b4-127">Il valore predefinito della proprietà è 10.</span><span class="sxs-lookup"><span data-stu-id="723b4-127">The default value of the property is 10.</span></span> <span data-ttu-id="723b4-128">Il valore massimo è 600, che rappresenta 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="723b4-128">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="723b4-129">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="723b4-129">Error codes</span></span>

<span data-ttu-id="723b4-130">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="723b4-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="723b4-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="723b4-131">Remarks</span></span>

<span data-ttu-id="723b4-132">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="723b4-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="723b4-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="723b4-133">Requirements</span></span>



| <span data-ttu-id="723b4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="723b4-134">Requirement</span></span> | <span data-ttu-id="723b4-135">Valore</span><span class="sxs-lookup"><span data-stu-id="723b4-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="723b4-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="723b4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="723b4-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="723b4-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="723b4-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="723b4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="723b4-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="723b4-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="723b4-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="723b4-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="723b4-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="723b4-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="723b4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="723b4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="723b4-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="723b4-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="723b4-144">IID</span><span class="sxs-lookup"><span data-stu-id="723b4-144">IID</span></span><br/>                      | <span data-ttu-id="723b4-145">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="723b4-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="723b4-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="723b4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723b4-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="723b4-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="723b4-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="723b4-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="723b4-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="723b4-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="723b4-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="723b4-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="723b4-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="723b4-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="723b4-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="723b4-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="723b4-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="723b4-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="723b4-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="723b4-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





