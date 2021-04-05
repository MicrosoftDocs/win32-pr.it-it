---
title: Proprietà AdvancedSettings6 di IMsRdpClient5
description: Recupera l'interfaccia IMsRdpClientAdvancedSettings5.
ms.assetid: b6a4efcf-87c3-438c-b6de-8a497ee5939d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings6
- Servizi Desktop remoto proprietà AdvancedSettings6, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà AdvancedSettings6
- Servizi Desktop remoto proprietà AdvancedSettings6, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà AdvancedSettings6
- Servizi Desktop remoto proprietà AdvancedSettings6, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà AdvancedSettings6
- Servizi Desktop remoto proprietà AdvancedSettings6, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings6
- Servizi Desktop remoto proprietà AdvancedSettings6, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings6
- Servizi Desktop remoto proprietà AdvancedSettings6, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà AdvancedSettings6
topic_type:
- apiref
api_name:
- IMsRdpClient5.AdvancedSettings6
- IMsRdpClient5.get_AdvancedSettings6
- IMsRdpClient6.AdvancedSettings6
- IMsRdpClient6.get_AdvancedSettings6
- IMsRdpClient7.AdvancedSettings6
- IMsRdpClient7.get_AdvancedSettings6
- IMsRdpClient8.AdvancedSettings6
- IMsRdpClient8.get_AdvancedSettings6
- IMsRdpClient9.AdvancedSettings6
- IMsRdpClient9.get_AdvancedSettings6
- IMsRdpClient10.AdvancedSettings6
- IMsRdpClient10.get_AdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b93d2395ec7e673e50023867f4602eea5c2d9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874538"
---
# <a name="imsrdpclient5advancedsettings6-property"></a><span data-ttu-id="6155e-116">Proprietà IMsRdpClient5:: AdvancedSettings6</span><span class="sxs-lookup"><span data-stu-id="6155e-116">IMsRdpClient5::AdvancedSettings6 property</span></span>

<span data-ttu-id="6155e-117">Recupera l'interfaccia [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="6155e-117">Retrieves the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="6155e-118">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6155e-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6155e-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6155e-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings6(
  [out] IMsRdpClientAdvancedSettings5 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="6155e-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6155e-120">Property value</span></span>

<span data-ttu-id="6155e-121">Puntatore di interfaccia [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="6155e-121">An [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6155e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6155e-122">Requirements</span></span>



| <span data-ttu-id="6155e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6155e-123">Requirement</span></span> | <span data-ttu-id="6155e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6155e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6155e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6155e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6155e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6155e-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6155e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6155e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6155e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6155e-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6155e-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6155e-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="6155e-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6155e-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6155e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6155e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6155e-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6155e-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6155e-133">IID</span><span class="sxs-lookup"><span data-stu-id="6155e-133">IID</span></span><br/>                      | <span data-ttu-id="6155e-134">IID \_ IMsRdpClient5 è definito come 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="6155e-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6155e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6155e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6155e-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="6155e-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="6155e-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="6155e-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="6155e-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="6155e-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="6155e-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="6155e-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="6155e-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="6155e-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="6155e-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="6155e-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





