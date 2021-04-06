---
title: Proprietà EnableWindowsKey di IMsRdpClientAdvancedSettings
description: Specifica se la chiave Windows può essere utilizzata nella sessione remota.
ms.assetid: fcf0460d-3cd1-4da4-8009-0b1256adf312
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà EnableWindowsKey
- Servizi Desktop remoto proprietà EnableWindowsKey, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà EnableWindowsKey
- Servizi Desktop remoto proprietà EnableWindowsKey, interfaccia IMsRdpClientAdvancedSettings2
- Interfaccia IMsRdpClientAdvancedSettings2 Servizi Desktop remoto, proprietà EnableWindowsKey
- Servizi Desktop remoto proprietà EnableWindowsKey, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà EnableWindowsKey
- Servizi Desktop remoto proprietà EnableWindowsKey, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà EnableWindowsKey
- Servizi Desktop remoto proprietà EnableWindowsKey, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà EnableWindowsKey
- Servizi Desktop remoto proprietà EnableWindowsKey, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà EnableWindowsKey
- Servizi Desktop remoto proprietà EnableWindowsKey, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà EnableWindowsKey
- Servizi Desktop remoto proprietà EnableWindowsKey, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà EnableWindowsKey
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableWindowsKey
- IMsRdpClientAdvancedSettings.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.EnableWindowsKey
- IMsRdpClientAdvancedSettings2.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.EnableWindowsKey
- IMsRdpClientAdvancedSettings3.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.EnableWindowsKey
- IMsRdpClientAdvancedSettings4.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.EnableWindowsKey
- IMsRdpClientAdvancedSettings5.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.EnableWindowsKey
- IMsRdpClientAdvancedSettings6.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.EnableWindowsKey
- IMsRdpClientAdvancedSettings7.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.EnableWindowsKey
- IMsRdpClientAdvancedSettings8.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.put_EnableWindowsKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e31571e44d6b391250c32268750b25a76105eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743298"
---
# <a name="imsrdpclientadvancedsettingsenablewindowskey-property"></a><span data-ttu-id="65b5b-120">Proprietà IMsRdpClientAdvancedSettings:: EnableWindowsKey</span><span class="sxs-lookup"><span data-stu-id="65b5b-120">IMsRdpClientAdvancedSettings::EnableWindowsKey property</span></span>

<span data-ttu-id="65b5b-121">Specifica se la chiave Windows può essere utilizzata nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="65b5b-121">Specifies if the Windows key can be used in the remote session.</span></span>

<span data-ttu-id="65b5b-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="65b5b-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65b5b-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65b5b-123">Syntax</span></span>


```C++
HRESULT put_EnableWindowsKey(
  [in]  LONG enableWindowsKey
);

HRESULT get_EnableWindowsKey(
  [out] LONG *penableWindowsKey
);
```



## <a name="property-value"></a><span data-ttu-id="65b5b-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="65b5b-124">Property value</span></span>

<span data-ttu-id="65b5b-125">Impostare questo parametro su 0 per disabilitare la funzionalità o un valore diverso da zero per abilitare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="65b5b-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="65b5b-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="65b5b-126">Error codes</span></span>

<span data-ttu-id="65b5b-127">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="65b5b-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="65b5b-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="65b5b-128">Remarks</span></span>

<span data-ttu-id="65b5b-129">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="65b5b-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65b5b-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65b5b-130">Requirements</span></span>



| <span data-ttu-id="65b5b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="65b5b-131">Requirement</span></span> | <span data-ttu-id="65b5b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="65b5b-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b5b-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65b5b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="65b5b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65b5b-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="65b5b-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65b5b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="65b5b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65b5b-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="65b5b-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="65b5b-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="65b5b-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65b5b-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="65b5b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="65b5b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65b5b-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65b5b-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="65b5b-141">IID</span><span class="sxs-lookup"><span data-stu-id="65b5b-141">IID</span></span><br/>                      | <span data-ttu-id="65b5b-142">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="65b5b-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65b5b-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65b5b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b5b-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="65b5b-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="65b5b-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="65b5b-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="65b5b-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="65b5b-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="65b5b-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="65b5b-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="65b5b-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="65b5b-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="65b5b-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="65b5b-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="65b5b-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="65b5b-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="65b5b-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="65b5b-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





