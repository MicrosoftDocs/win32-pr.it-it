---
title: Proprietà keepAliveInterval di IMsRdpClientAdvancedSettings
description: Specifica un intervallo, in millisecondi, in cui il client invia messaggi keep-alive al server.
ms.assetid: 0d1b7d8f-f81c-4591-bb08-adab307e87fe
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà keepAliveInterval
- Servizi Desktop remoto proprietà keepAliveInterval, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà keepAliveInterval
- Servizi Desktop remoto proprietà keepAliveInterval, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà keepAliveInterval
- Servizi Desktop remoto proprietà keepAliveInterval, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà keepAliveInterval
- Servizi Desktop remoto proprietà keepAliveInterval, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà keepAliveInterval
- Servizi Desktop remoto proprietà keepAliveInterval, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà keepAliveInterval
- Servizi Desktop remoto proprietà keepAliveInterval, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà keepAliveInterval
- Servizi Desktop remoto proprietà keepAliveInterval, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà keepAliveInterval
- Servizi Desktop remoto proprietà keepAliveInterval, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà keepAliveInterval
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.keepAliveInterval
- IMsRdpClientAdvancedSettings.get_keepAliveInterval
- IMsRdpClientAdvancedSettings.put_keepAliveInterval
- IMsRdpClientAdvancedSettings2.keepAliveInterval
- IMsRdpClientAdvancedSettings2.get_keepAliveInterval
- IMsRdpClientAdvancedSettings2.put_keepAliveInterval
- IMsRdpClientAdvancedSettings3.keepAliveInterval
- IMsRdpClientAdvancedSettings3.get_keepAliveInterval
- IMsRdpClientAdvancedSettings3.put_keepAliveInterval
- IMsRdpClientAdvancedSettings4.keepAliveInterval
- IMsRdpClientAdvancedSettings4.get_keepAliveInterval
- IMsRdpClientAdvancedSettings4.put_keepAliveInterval
- IMsRdpClientAdvancedSettings5.keepAliveInterval
- IMsRdpClientAdvancedSettings5.get_keepAliveInterval
- IMsRdpClientAdvancedSettings5.put_keepAliveInterval
- IMsRdpClientAdvancedSettings6.keepAliveInterval
- IMsRdpClientAdvancedSettings6.get_keepAliveInterval
- IMsRdpClientAdvancedSettings6.put_keepAliveInterval
- IMsRdpClientAdvancedSettings7.keepAliveInterval
- IMsRdpClientAdvancedSettings7.get_keepAliveInterval
- IMsRdpClientAdvancedSettings7.put_keepAliveInterval
- IMsRdpClientAdvancedSettings8.keepAliveInterval
- IMsRdpClientAdvancedSettings8.get_keepAliveInterval
- IMsRdpClientAdvancedSettings8.put_keepAliveInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d15412b5b1803aadcffa08a8617742e0c90b1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400450"
---
# <a name="imsrdpclientadvancedsettingskeepaliveinterval-property"></a><span data-ttu-id="65057-120">Proprietà IMsRdpClientAdvancedSettings:: keepAliveInterval</span><span class="sxs-lookup"><span data-stu-id="65057-120">IMsRdpClientAdvancedSettings::keepAliveInterval property</span></span>

<span data-ttu-id="65057-121">Specifica un intervallo, in millisecondi, in cui il client invia messaggi keep-alive al server.</span><span class="sxs-lookup"><span data-stu-id="65057-121">Specifies an interval, in milliseconds, at which the client sends keep-alive messages to the server.</span></span>

<span data-ttu-id="65057-122">Impostazione di criteri di gruppo che specifica se le connessioni client permanenti al server sono consentite e possono eseguire l'override di questa impostazione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="65057-122">A group policy setting that specifies whether persistent client connections to the server are allowed can override this property setting.</span></span>

<span data-ttu-id="65057-123">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="65057-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65057-124">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65057-124">Syntax</span></span>


```C++
HRESULT put_keepAliveInterval(
  [in]  LONG keepAliveInterval
);

HRESULT get_keepAliveInterval(
  [out] LONG *pkeepAliveInterval
);
```



## <a name="property-value"></a><span data-ttu-id="65057-125">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="65057-125">Property value</span></span>

<span data-ttu-id="65057-126">Nuovo intervallo, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="65057-126">The new interval, in milliseconds.</span></span> <span data-ttu-id="65057-127">Il valore predefinito della proprietà è zero, che Disabilita i messaggi keep-alive.</span><span class="sxs-lookup"><span data-stu-id="65057-127">The default value of the property is zero, which disables keep-alive messages.</span></span> <span data-ttu-id="65057-128">Il valore minimo valido di questa proprietà è 10.000, che rappresenta 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="65057-128">The minimum valid value of this property is 10,000, which represents 10 seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="65057-129">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="65057-129">Error codes</span></span>

<span data-ttu-id="65057-130">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="65057-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="65057-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="65057-131">Remarks</span></span>

<span data-ttu-id="65057-132">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="65057-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65057-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65057-133">Requirements</span></span>



| <span data-ttu-id="65057-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="65057-134">Requirement</span></span> | <span data-ttu-id="65057-135">Valore</span><span class="sxs-lookup"><span data-stu-id="65057-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65057-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65057-136">Minimum supported client</span></span><br/> | <span data-ttu-id="65057-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65057-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="65057-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65057-138">Minimum supported server</span></span><br/> | <span data-ttu-id="65057-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65057-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="65057-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="65057-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="65057-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65057-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="65057-142">DLL</span><span class="sxs-lookup"><span data-stu-id="65057-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65057-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65057-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="65057-144">IID</span><span class="sxs-lookup"><span data-stu-id="65057-144">IID</span></span><br/>                      | <span data-ttu-id="65057-145">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="65057-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65057-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65057-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65057-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="65057-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="65057-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="65057-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="65057-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="65057-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="65057-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="65057-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="65057-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="65057-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="65057-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="65057-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="65057-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="65057-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="65057-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="65057-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





