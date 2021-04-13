---
title: Proprietà ConnectionBarShowRestoreButton di IMsRdpClientAdvancedSettings3
description: Specifica se visualizzare il pulsante Ripristina sulla barra delle connessioni.
ms.assetid: a56c3c05-d253-404a-bf49-9c1d804802e0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ConnectionBarShowRestoreButton
- Servizi Desktop remoto proprietà ConnectionBarShowRestoreButton, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà ConnectionBarShowRestoreButton
- Servizi Desktop remoto proprietà ConnectionBarShowRestoreButton, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà ConnectionBarShowRestoreButton
- Servizi Desktop remoto proprietà ConnectionBarShowRestoreButton, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà ConnectionBarShowRestoreButton
- Servizi Desktop remoto proprietà ConnectionBarShowRestoreButton, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà ConnectionBarShowRestoreButton
- Servizi Desktop remoto proprietà ConnectionBarShowRestoreButton, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà ConnectionBarShowRestoreButton
- Servizi Desktop remoto proprietà ConnectionBarShowRestoreButton, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà ConnectionBarShowRestoreButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowRestoreButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83ecde31461eff9c553782b8bfa3ae760fb54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400314"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowrestorebutton-property"></a><span data-ttu-id="5cca4-116">Proprietà IMsRdpClientAdvancedSettings3:: ConnectionBarShowRestoreButton</span><span class="sxs-lookup"><span data-stu-id="5cca4-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowRestoreButton property</span></span>

<span data-ttu-id="5cca4-117">Specifica se visualizzare il pulsante **Ripristina** sulla barra delle connessioni.</span><span class="sxs-lookup"><span data-stu-id="5cca4-117">Specifies whether to display the **Restore** button on the connection bar.</span></span>

<span data-ttu-id="5cca4-118">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="5cca4-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cca4-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5cca4-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowRestoreButton(
  [in]  VARIANT_BOOL fShowRestore
);

HRESULT get_ConnectionBarShowRestoreButton(
  [out] VARIANT_BOOL *pfShowRestore
);
```



## <a name="property-value"></a><span data-ttu-id="5cca4-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5cca4-120">Property value</span></span>

<span data-ttu-id="5cca4-121">Impostare su **Variant \_ true** per visualizzare il pulsante **Ripristina** e su **Variant \_ false** per disabilitare la visualizzazione del pulsante **Ripristina** .</span><span class="sxs-lookup"><span data-stu-id="5cca4-121">Set to **VARIANT\_TRUE** to display the **Restore** button, and to **VARIANT\_FALSE** to disable the display of the **Restore** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5cca4-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5cca4-122">Error codes</span></span>

<span data-ttu-id="5cca4-123">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5cca4-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cca4-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cca4-124">Remarks</span></span>

<span data-ttu-id="5cca4-125">Impossibile impostare questa proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="5cca4-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="5cca4-126">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5cca4-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cca4-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cca4-127">Requirements</span></span>



| <span data-ttu-id="5cca4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cca4-128">Requirement</span></span> | <span data-ttu-id="5cca4-129">Valore</span><span class="sxs-lookup"><span data-stu-id="5cca4-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cca4-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cca4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5cca4-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5cca4-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="5cca4-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cca4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5cca4-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5cca4-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="5cca4-134">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5cca4-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="5cca4-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cca4-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5cca4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5cca4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cca4-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cca4-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5cca4-138">IID</span><span class="sxs-lookup"><span data-stu-id="5cca4-138">IID</span></span><br/>                      | <span data-ttu-id="5cca4-139">IID \_ IMsRdpClientAdvancedSettings3 è definito come 19cd856b-C542-4c53-Acee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="5cca4-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cca4-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cca4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cca4-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="5cca4-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="5cca4-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="5cca4-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="5cca4-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="5cca4-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="5cca4-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5cca4-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="5cca4-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="5cca4-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="5cca4-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="5cca4-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





