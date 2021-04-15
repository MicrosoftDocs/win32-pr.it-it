---
title: Proprietà RemoteProgram di IMsRdpClient5
description: Recupera un oggetto che supporta l'interfaccia ITSRemoteProgram.
ms.assetid: 013f613b-af7b-4cc5-be1f-d45833806e3b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RemoteProgram
- Servizi Desktop remoto proprietà RemoteProgram, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, proprietà RemoteProgram
- Servizi Desktop remoto proprietà RemoteProgram, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà RemoteProgram
- Servizi Desktop remoto proprietà RemoteProgram, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà RemoteProgram
- Servizi Desktop remoto proprietà RemoteProgram, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà RemoteProgram
- Servizi Desktop remoto proprietà RemoteProgram, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà RemoteProgram
- Servizi Desktop remoto proprietà RemoteProgram, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà RemoteProgram
topic_type:
- apiref
api_name:
- IMsRdpClient5.RemoteProgram
- IMsRdpClient5.get_RemoteProgram
- IMsRdpClient6.RemoteProgram
- IMsRdpClient6.get_RemoteProgram
- IMsRdpClient7.RemoteProgram
- IMsRdpClient7.get_RemoteProgram
- IMsRdpClient8.RemoteProgram
- IMsRdpClient8.get_RemoteProgram
- IMsRdpClient9.RemoteProgram
- IMsRdpClient9.get_RemoteProgram
- IMsRdpClient10.RemoteProgram
- IMsRdpClient10.get_RemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267e367af090a7fd70e9482406104fd0403d63f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475790"
---
# <a name="imsrdpclient5remoteprogram-property"></a><span data-ttu-id="54da8-116">Proprietà IMsRdpClient5:: RemoteProgram</span><span class="sxs-lookup"><span data-stu-id="54da8-116">IMsRdpClient5::RemoteProgram property</span></span>

<span data-ttu-id="54da8-117">Recupera un oggetto che supporta l'interfaccia [**ITSRemoteProgram**](itsremoteprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="54da8-117">Retrieves an object that supports the [**ITSRemoteProgram**](itsremoteprogram.md) interface.</span></span>

<span data-ttu-id="54da8-118">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="54da8-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="54da8-119">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54da8-119">Syntax</span></span>


```C++
HRESULT get_RemoteProgram(
  [out] ITSRemoteProgram **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="54da8-120">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="54da8-120">Property value</span></span>

<span data-ttu-id="54da8-121">Puntatore di interfaccia [**ITSRemoteProgram**](itsremoteprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="54da8-121">An [**ITSRemoteProgram**](itsremoteprogram.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="54da8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54da8-122">Requirements</span></span>



| <span data-ttu-id="54da8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="54da8-123">Requirement</span></span> | <span data-ttu-id="54da8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="54da8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54da8-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54da8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="54da8-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54da8-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="54da8-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54da8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="54da8-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54da8-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="54da8-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="54da8-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="54da8-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54da8-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="54da8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="54da8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54da8-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54da8-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="54da8-133">IID</span><span class="sxs-lookup"><span data-stu-id="54da8-133">IID</span></span><br/>                      | <span data-ttu-id="54da8-134">IID \_ IMsRdpClient5 è definito come 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="54da8-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="54da8-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54da8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54da8-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="54da8-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="54da8-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="54da8-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="54da8-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="54da8-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="54da8-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="54da8-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="54da8-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="54da8-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="54da8-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="54da8-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





