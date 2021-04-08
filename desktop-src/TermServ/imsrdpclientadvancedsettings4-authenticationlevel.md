---
title: Proprietà AuthenticationLevel di IMsRdpClientAdvancedSettings4
description: Specifica il livello di autenticazione da utilizzare per la connessione.
ms.assetid: 09ff1508-f13d-4bb0-8458-6f5a5e099bae
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AuthenticationLevel
- Servizi Desktop remoto proprietà AuthenticationLevel, interfaccia IMsRdpClientAdvancedSettings4
- Interfaccia IMsRdpClientAdvancedSettings4 Servizi Desktop remoto, proprietà AuthenticationLevel
- Servizi Desktop remoto proprietà AuthenticationLevel, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà AuthenticationLevel
- Servizi Desktop remoto proprietà AuthenticationLevel, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà AuthenticationLevel
- Servizi Desktop remoto proprietà AuthenticationLevel, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà AuthenticationLevel
- Servizi Desktop remoto proprietà AuthenticationLevel, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà AuthenticationLevel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4.AuthenticationLevel
- IMsRdpClientAdvancedSettings4.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings4.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.AuthenticationLevel
- IMsRdpClientAdvancedSettings5.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.AuthenticationLevel
- IMsRdpClientAdvancedSettings6.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.AuthenticationLevel
- IMsRdpClientAdvancedSettings7.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.AuthenticationLevel
- IMsRdpClientAdvancedSettings8.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.put_AuthenticationLevel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c748416650ec7e6ec3d26fe6236a254eb012d67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873697"
---
# <a name="imsrdpclientadvancedsettings4authenticationlevel-property"></a><span data-ttu-id="b062e-114">Proprietà IMsRdpClientAdvancedSettings4:: AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="b062e-114">IMsRdpClientAdvancedSettings4::AuthenticationLevel property</span></span>

<span data-ttu-id="b062e-115">Specifica il livello di autenticazione da utilizzare per la connessione.</span><span class="sxs-lookup"><span data-stu-id="b062e-115">Specifies the authentication level to use for the connection.</span></span>

<span data-ttu-id="b062e-116">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b062e-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b062e-117">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b062e-117">Syntax</span></span>


```C++
HRESULT put_AuthenticationLevel(
  [in]  UINT uiAuthLevel
);

HRESULT get_AuthenticationLevel(
  [out] UINT *puiAuthLevel
);
```



## <a name="property-value"></a><span data-ttu-id="b062e-118">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b062e-118">Property value</span></span>

<span data-ttu-id="b062e-119">Valore della proprietà **AuthenticationLevel** .</span><span class="sxs-lookup"><span data-stu-id="b062e-119">The value of the **AuthenticationLevel** property.</span></span>

<dt>

<span data-ttu-id="b062e-120">0</span><span class="sxs-lookup"><span data-stu-id="b062e-120">0</span></span>
</dt> <dd>

<span data-ttu-id="b062e-121">Nessuna autenticazione del server.</span><span class="sxs-lookup"><span data-stu-id="b062e-121">No authentication of the server.</span></span>

</dd> <dt>

<span data-ttu-id="b062e-122">1</span><span class="sxs-lookup"><span data-stu-id="b062e-122">1</span></span>
</dt> <dd>

<span data-ttu-id="b062e-123">L'autenticazione server è obbligatoria e deve essere completata correttamente affinché la connessione continui.</span><span class="sxs-lookup"><span data-stu-id="b062e-123">Server authentication is required and must complete successfully for the connection to proceed.</span></span>

</dd> <dt>

<span data-ttu-id="b062e-124">2</span><span class="sxs-lookup"><span data-stu-id="b062e-124">2</span></span>
</dt> <dd>

<span data-ttu-id="b062e-125">Tentativo di autenticazione del server.</span><span class="sxs-lookup"><span data-stu-id="b062e-125">Attempt authentication of the server.</span></span> <span data-ttu-id="b062e-126">Se l'autenticazione non riesce, all'utente verrà richiesto di annullare la connessione o di procedere senza l'autenticazione del server.</span><span class="sxs-lookup"><span data-stu-id="b062e-126">If authentication fails, the user will be prompted with the option to cancel the connection or to proceed without server authentication.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="b062e-127">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b062e-127">Error codes</span></span>

<span data-ttu-id="b062e-128">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b062e-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b062e-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="b062e-129">Remarks</span></span>

<span data-ttu-id="b062e-130">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b062e-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b062e-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b062e-131">Requirements</span></span>



| <span data-ttu-id="b062e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b062e-132">Requirement</span></span> | <span data-ttu-id="b062e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b062e-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b062e-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b062e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b062e-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b062e-135">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="b062e-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b062e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b062e-137">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="b062e-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="b062e-138">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b062e-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="b062e-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b062e-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b062e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="b062e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b062e-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b062e-141"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b062e-142">IID</span><span class="sxs-lookup"><span data-stu-id="b062e-142">IID</span></span><br/>                      | <span data-ttu-id="b062e-143">IID \_ IMsRdpClientAdvancedSettings4 è definito come FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="b062e-143">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b062e-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b062e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b062e-145">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b062e-145">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b062e-146">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b062e-146">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b062e-147">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b062e-147">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b062e-148">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b062e-148">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b062e-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b062e-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> </dl>

 

 





