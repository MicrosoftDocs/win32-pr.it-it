---
title: Proprietà NegotiateSecurityLayer di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se il livello di sicurezza della negoziazione è abilitato per la connessione.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
- Servizi Desktop remoto proprietà NegotiateSecurityLayer, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà NegotiateSecurityLayer
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301628"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a><span data-ttu-id="2f2c1-120">Proprietà IMsRdpClientNonScriptable3:: NegotiateSecurityLayer</span><span class="sxs-lookup"><span data-stu-id="2f2c1-120">IMsRdpClientNonScriptable3::NegotiateSecurityLayer property</span></span>

<span data-ttu-id="2f2c1-121">Specifica o recupera un valore che indica se il livello di sicurezza della negoziazione è abilitato per la connessione.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-121">Specifies or retrieves whether the negotiation security layer is enabled for the connection.</span></span>

<span data-ttu-id="2f2c1-122">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2c1-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f2c1-123">Syntax</span></span>


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a><span data-ttu-id="2f2c1-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2f2c1-124">Property value</span></span>

<span data-ttu-id="2f2c1-125">Specifica se abilitare la negoziazione del livello di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-125">Specifies whether to enable negotiation of the security layer.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f2c1-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f2c1-126">Remarks</span></span>

<span data-ttu-id="2f2c1-127">Se questa proprietà è impostata su **Variant \_ FALSE** e autenticazione a livello di rete (NLA) è abilitata nel sistema operativo client, il client non negozierà il livello di sicurezza e utilizzerà invece NLA per proteggere la connessione RDP.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-127">If this property is set to **VARIANT\_FALSE** and Network Level Authentication (NLA) is enabled on the client operating system, the client will not negotiate the security layer and instead, it will use NLA to secure the RDP connection.</span></span> <span data-ttu-id="2f2c1-128">Se questa proprietà è impostata su **Variant \_ true**, il client effettuerà la negoziazione tra NLA e la sicurezza RDP di base.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-128">If this property is set to **VARIANT\_TRUE**, then the client will negotiate between NLA and basic RDP security.</span></span>

> [!Note]  
> <span data-ttu-id="2f2c1-129">La disabilitazione della negoziazione del livello di sicurezza è possibile solo quando ci si connette a un server di host sessione Desktop remoto (host sessione Desktop remoto) che esegue Windows Vista o sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-129">Disabling security layer negotiation is only possible when connecting to a Remote Desktop Session Host (RD Session Host) server running Windows Vista or later operating systems.</span></span> <span data-ttu-id="2f2c1-130">Se questa proprietà è abilitata e il client tenta di connettersi a un server Host sessione Desktop remoto che esegue un sistema operativo precedente, la connessione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2f2c1-130">If this property is enabled and the client attempts to connect to an RD Session Host server running an earlier operating system, the connection will fail.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2f2c1-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f2c1-131">Requirements</span></span>



| <span data-ttu-id="2f2c1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f2c1-132">Requirement</span></span> | <span data-ttu-id="2f2c1-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2f2c1-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2c1-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f2c1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2f2c1-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f2c1-135">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="2f2c1-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f2c1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2f2c1-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f2c1-137">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="2f2c1-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2f2c1-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f2c1-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f2c1-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="2f2c1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2f2c1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f2c1-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f2c1-141"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="2f2c1-142">IID</span><span class="sxs-lookup"><span data-stu-id="2f2c1-142">IID</span></span><br/>                      | <span data-ttu-id="2f2c1-143">IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="2f2c1-143">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f2c1-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f2c1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2c1-145">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="2f2c1-145">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="2f2c1-146">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="2f2c1-146">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="2f2c1-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="2f2c1-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





