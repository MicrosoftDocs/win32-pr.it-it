---
title: Proprietà ConnectionBarShowMinimizeButton di IMsRdpClientAdvancedSettings3
description: Specifica se visualizzare il pulsante Riduci a icona sulla barra delle connessioni.
ms.assetid: 3ad89f25-f1ff-4bfc-ae86-09603058c9b5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà ConnectionBarShowMinimizeButton
- Servizi Desktop remoto proprietà ConnectionBarShowMinimizeButton, interfaccia IMsRdpClientAdvancedSettings3
- Interfaccia IMsRdpClientAdvancedSettings3 Servizi Desktop remoto, proprietà ConnectionBarShowMinimizeButton
- Servizi Desktop remoto proprietà ConnectionBarShowMinimizeButton, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà ConnectionBarShowMinimizeButton
- Servizi Desktop remoto proprietà ConnectionBarShowMinimizeButton, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà ConnectionBarShowMinimizeButton
- Servizi Desktop remoto proprietà ConnectionBarShowMinimizeButton, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà ConnectionBarShowMinimizeButton
- Servizi Desktop remoto proprietà ConnectionBarShowMinimizeButton, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà ConnectionBarShowMinimizeButton
- Servizi Desktop remoto proprietà ConnectionBarShowMinimizeButton, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà ConnectionBarShowMinimizeButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowMinimizeButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3cb600a853e4bc2dea7c693e676f992db85f48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740010"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowminimizebutton-property"></a><span data-ttu-id="c4dc8-116">Proprietà IMsRdpClientAdvancedSettings3:: ConnectionBarShowMinimizeButton</span><span class="sxs-lookup"><span data-stu-id="c4dc8-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowMinimizeButton property</span></span>

<span data-ttu-id="c4dc8-117">Specifica se visualizzare il pulsante **Riduci a icona** sulla barra delle connessioni.</span><span class="sxs-lookup"><span data-stu-id="c4dc8-117">Specifies whether to display the **Minimize** button on the connection bar.</span></span>

<span data-ttu-id="c4dc8-118">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c4dc8-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4dc8-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4dc8-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowMinimizeButton(
  [in]  VARIANT_BOOL fShowMinimize
);

HRESULT get_ConnectionBarShowMinimizeButton(
  [out] VARIANT_BOOL *pfShowMinimize
);
```



## <a name="property-value"></a><span data-ttu-id="c4dc8-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c4dc8-120">Property value</span></span>

<span data-ttu-id="c4dc8-121">Impostare questo parametro su **Variant \_ true** per visualizzare il pulsante **Riduci a icona** e su **Variant \_ false** per disabilitare la visualizzazione del pulsante **Riduci a icona** .</span><span class="sxs-lookup"><span data-stu-id="c4dc8-121">Set this parameter to **VARIANT\_TRUE** to display the **Minimize** button, and to **VARIANT\_FALSE** to disable the display of the **Minimize** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c4dc8-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c4dc8-122">Error codes</span></span>

<span data-ttu-id="c4dc8-123">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c4dc8-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4dc8-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4dc8-124">Remarks</span></span>

<span data-ttu-id="c4dc8-125">Impossibile impostare questa proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="c4dc8-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="c4dc8-126">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c4dc8-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4dc8-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4dc8-127">Requirements</span></span>



| <span data-ttu-id="c4dc8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4dc8-128">Requirement</span></span> | <span data-ttu-id="c4dc8-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c4dc8-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4dc8-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4dc8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c4dc8-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4dc8-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="c4dc8-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4dc8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c4dc8-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4dc8-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="c4dc8-134">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c4dc8-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4dc8-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4dc8-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c4dc8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c4dc8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4dc8-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4dc8-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c4dc8-138">IID</span><span class="sxs-lookup"><span data-stu-id="c4dc8-138">IID</span></span><br/>                      | <span data-ttu-id="c4dc8-139">IID \_ IMsRdpClientAdvancedSettings3 è definito come 19cd856b-C542-4c53-Acee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="c4dc8-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c4dc8-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4dc8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4dc8-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c4dc8-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c4dc8-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c4dc8-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c4dc8-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c4dc8-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c4dc8-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c4dc8-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c4dc8-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c4dc8-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c4dc8-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c4dc8-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





