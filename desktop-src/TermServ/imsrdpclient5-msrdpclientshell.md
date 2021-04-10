---
title: Proprietà MsRdpClientShell di IMsRdpClient5
description: Recupera l'interfaccia IMsRdpClientShell dell'impostazione del client configurabile tramite script.
ms.assetid: cc56cec4-779d-4b51-8e94-ae0dd9bae997
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà MsRdpClientShell
- Servizi Desktop remoto proprietà MsRdpClientShell, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà MsRdpClientShell
- Servizi Desktop remoto proprietà MsRdpClientShell, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà MsRdpClientShell
- Servizi Desktop remoto proprietà MsRdpClientShell, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà MsRdpClientShell
- Servizi Desktop remoto proprietà MsRdpClientShell, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà MsRdpClientShell
- Servizi Desktop remoto proprietà MsRdpClientShell, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà MsRdpClientShell
- Servizi Desktop remoto proprietà MsRdpClientShell, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà MsRdpClientShell
topic_type:
- apiref
api_name:
- IMsRdpClient5.MsRdpClientShell
- IMsRdpClient5.get_MsRdpClientShell
- IMsRdpClient6.MsRdpClientShell
- IMsRdpClient6.get_MsRdpClientShell
- IMsRdpClient7.MsRdpClientShell
- IMsRdpClient7.get_MsRdpClientShell
- IMsRdpClient8.MsRdpClientShell
- IMsRdpClient8.get_MsRdpClientShell
- IMsRdpClient9.MsRdpClientShell
- IMsRdpClient9.get_MsRdpClientShell
- IMsRdpClient10.MsRdpClientShell
- IMsRdpClient10.get_MsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46129dc4736b50e8b6a650cc7a59f9b238da56e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121435"
---
# <a name="imsrdpclient5msrdpclientshell-property"></a><span data-ttu-id="9eb3d-116">Proprietà IMsRdpClient5:: MsRdpClientShell</span><span class="sxs-lookup"><span data-stu-id="9eb3d-116">IMsRdpClient5::MsRdpClientShell property</span></span>

<span data-ttu-id="9eb3d-117">Recupera l'interfaccia [**IMsRdpClientShell**](imsrdpclientshell.md)dell'impostazione del client configurabile tramite script.</span><span class="sxs-lookup"><span data-stu-id="9eb3d-117">Retrieves the scriptable client setting interface [**IMsRdpClientShell**](imsrdpclientshell.md).</span></span>

<span data-ttu-id="9eb3d-118">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9eb3d-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb3d-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eb3d-119">Syntax</span></span>


```C++
HRESULT get_MsRdpClientShell(
  [out] IMsRdpClientShell **ppLauncher
);
```



## <a name="property-value"></a><span data-ttu-id="9eb3d-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9eb3d-120">Property value</span></span>

<span data-ttu-id="9eb3d-121">Puntatore di interfaccia [**IMsRdpClientShell**](imsrdpclientshell.md) .</span><span class="sxs-lookup"><span data-stu-id="9eb3d-121">An [**IMsRdpClientShell**](imsrdpclientshell.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb3d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eb3d-122">Requirements</span></span>



| <span data-ttu-id="9eb3d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb3d-123">Requirement</span></span> | <span data-ttu-id="9eb3d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9eb3d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb3d-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb3d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb3d-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9eb3d-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9eb3d-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb3d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb3d-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9eb3d-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9eb3d-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9eb3d-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="9eb3d-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb3d-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9eb3d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9eb3d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eb3d-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb3d-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9eb3d-133">IID</span><span class="sxs-lookup"><span data-stu-id="9eb3d-133">IID</span></span><br/>                      | <span data-ttu-id="9eb3d-134">IID \_ IMsRdpClient5 è definito come 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="9eb3d-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9eb3d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9eb3d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb3d-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="9eb3d-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="9eb3d-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="9eb3d-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="9eb3d-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9eb3d-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9eb3d-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9eb3d-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9eb3d-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9eb3d-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9eb3d-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="9eb3d-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





