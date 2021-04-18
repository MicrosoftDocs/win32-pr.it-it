---
title: Proprietà TransportSettings2 di IMsRdpClient6
description: Recupera l'interfaccia IMsRdpClientTransportSettings2.
ms.assetid: 5cd3c745-b360-43fb-b780-c526ed539db0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà TransportSettings2
- Servizi Desktop remoto proprietà TransportSettings2, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, proprietà TransportSettings2
- Servizi Desktop remoto proprietà TransportSettings2, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà TransportSettings2
- Servizi Desktop remoto proprietà TransportSettings2, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà TransportSettings2
- Servizi Desktop remoto proprietà TransportSettings2, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà TransportSettings2
- Servizi Desktop remoto proprietà TransportSettings2, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà TransportSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient6.TransportSettings2
- IMsRdpClient6.get_TransportSettings2
- IMsRdpClient7.TransportSettings2
- IMsRdpClient7.get_TransportSettings2
- IMsRdpClient8.TransportSettings2
- IMsRdpClient8.get_TransportSettings2
- IMsRdpClient9.TransportSettings2
- IMsRdpClient9.get_TransportSettings2
- IMsRdpClient10.TransportSettings2
- IMsRdpClient10.get_TransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ba11975e0e065e0cfcce91eb22402153acf236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301226"
---
# <a name="imsrdpclient6transportsettings2-property"></a><span data-ttu-id="d3d07-114">Proprietà IMsRdpClient6:: TransportSettings2</span><span class="sxs-lookup"><span data-stu-id="d3d07-114">IMsRdpClient6::TransportSettings2 property</span></span>

<span data-ttu-id="d3d07-115">Recupera l'interfaccia [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="d3d07-115">Retrieves the [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface.</span></span>

<span data-ttu-id="d3d07-116">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d3d07-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d07-117">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3d07-117">Syntax</span></span>


```C++
HRESULT get_TransportSettings2(
  [out] IMsRdpClientTransportSettings2 **ppXportSet2
);
```



## <a name="property-value"></a><span data-ttu-id="d3d07-118">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d3d07-118">Property value</span></span>

<span data-ttu-id="d3d07-119">Puntatore di interfaccia [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="d3d07-119">An [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d07-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3d07-120">Requirements</span></span>



| <span data-ttu-id="d3d07-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3d07-121">Requirement</span></span> | <span data-ttu-id="d3d07-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d3d07-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d07-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3d07-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d3d07-124">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="d3d07-124">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="d3d07-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3d07-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d3d07-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3d07-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d3d07-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d3d07-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="d3d07-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3d07-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d3d07-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d3d07-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3d07-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3d07-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d3d07-131">IID</span><span class="sxs-lookup"><span data-stu-id="d3d07-131">IID</span></span><br/>                      | <span data-ttu-id="d3d07-132">IID \_ IMsRdpClient6 è definito come d43b7d80-8517-4B6D-9EAC-96ad6800d7f2</span><span class="sxs-lookup"><span data-stu-id="d3d07-132">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d3d07-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3d07-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d07-134">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="d3d07-134">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="d3d07-135">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="d3d07-135">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="d3d07-136">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="d3d07-136">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="d3d07-137">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d3d07-137">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d3d07-138">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="d3d07-138">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





