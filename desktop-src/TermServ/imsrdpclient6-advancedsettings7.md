---
title: Proprietà AdvancedSettings7 di IMsRdpClient6
description: Recupera l'interfaccia IMsRdpClientAdvancedSettings6.
ms.assetid: 64b05c66-ac6a-4190-9df8-4a88dbc46c3f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings7
- Servizi Desktop remoto proprietà AdvancedSettings7, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà AdvancedSettings7
- Servizi Desktop remoto proprietà AdvancedSettings7, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà AdvancedSettings7
- Servizi Desktop remoto proprietà AdvancedSettings7, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings7
- Servizi Desktop remoto proprietà AdvancedSettings7, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings7
- Servizi Desktop remoto proprietà AdvancedSettings7, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà AdvancedSettings7
- Servizi Desktop remoto proprietà AdvancedSettings7, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà AdvancedSettings7
topic_type:
- apiref
api_name:
- IMsRdpClient6.AdvancedSettings7
- IMsRdpClient6.get_AdvancedSettings7
- IMsRdpClient7.AdvancedSettings7
- IMsRdpClient7.get_AdvancedSettings7
- IMsRdpClient8.AdvancedSettings7
- IMsRdpClient8.get_AdvancedSettings7
- IMsRdpClient9.AdvancedSettings7
- IMsRdpClient9.get_AdvancedSettings7
- IMsRdpClient10.AdvancedSettings7
- IMsRdpClient10.get_AdvancedSettings7
- MsRdpClient6.AdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51d364c14be3311272455e040d55f277f3fb136
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400391"
---
# <a name="imsrdpclient6advancedsettings7-property"></a><span data-ttu-id="405b0-116">Proprietà IMsRdpClient6:: AdvancedSettings7</span><span class="sxs-lookup"><span data-stu-id="405b0-116">IMsRdpClient6::AdvancedSettings7 property</span></span>

<span data-ttu-id="405b0-117">Recupera l'interfaccia [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="405b0-117">Retrieves the [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="405b0-118">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="405b0-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="405b0-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="405b0-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings7(
  [out] IMsRdpClientAdvancedSettings6 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="405b0-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="405b0-120">Property value</span></span>

<span data-ttu-id="405b0-121">Puntatore di interfaccia [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md) .</span><span class="sxs-lookup"><span data-stu-id="405b0-121">An [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="405b0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="405b0-122">Requirements</span></span>



| <span data-ttu-id="405b0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="405b0-123">Requirement</span></span> | <span data-ttu-id="405b0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="405b0-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="405b0-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="405b0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="405b0-126">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="405b0-126">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="405b0-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="405b0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="405b0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="405b0-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="405b0-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="405b0-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="405b0-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="405b0-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="405b0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="405b0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="405b0-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="405b0-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="405b0-133">IID</span><span class="sxs-lookup"><span data-stu-id="405b0-133">IID</span></span><br/>                      | <span data-ttu-id="405b0-134">IID \_ IMsRdpClient6 è definito come d43b7d80-8517-4B6D-9EAC-96ad6800d7f2</span><span class="sxs-lookup"><span data-stu-id="405b0-134">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="405b0-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="405b0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="405b0-136">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="405b0-136">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="405b0-137">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="405b0-137">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="405b0-138">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="405b0-138">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="405b0-139">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="405b0-139">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="405b0-140">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="405b0-140">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





