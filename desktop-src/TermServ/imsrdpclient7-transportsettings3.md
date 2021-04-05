---
title: Proprietà TransportSettings3 di IMsRdpClient7
description: Recupera un oggetto che supporta l'interfaccia IMsRdpClientTransportSettings3.
ms.assetid: d11f0943-241e-44cd-a98c-595916ab0718
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà TransportSettings3
- Servizi Desktop remoto proprietà TransportSettings3, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà TransportSettings3
- Servizi Desktop remoto proprietà TransportSettings3, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà TransportSettings3
- Servizi Desktop remoto proprietà TransportSettings3, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà TransportSettings3
- Servizi Desktop remoto proprietà TransportSettings3, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà TransportSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.TransportSettings3
- IMsRdpClient7.get_TransportSettings3
- IMsRdpClient8.TransportSettings3
- IMsRdpClient8.get_TransportSettings3
- IMsRdpClient9.TransportSettings3
- IMsRdpClient9.get_TransportSettings3
- IMsRdpClient10.TransportSettings3
- IMsRdpClient10.get_TransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c60b58f8f2438de0d43f69ce0b3bb73607e7551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740562"
---
# <a name="imsrdpclient7transportsettings3-property"></a><span data-ttu-id="e40f2-112">Proprietà IMsRdpClient7:: TransportSettings3</span><span class="sxs-lookup"><span data-stu-id="e40f2-112">IMsRdpClient7::TransportSettings3 property</span></span>

<span data-ttu-id="e40f2-113">Recupera un oggetto che supporta l'interfaccia [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="e40f2-113">Retrieves an object that supports the [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface.</span></span>

<span data-ttu-id="e40f2-114">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e40f2-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e40f2-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e40f2-115">Syntax</span></span>


```C++
HRESULT get_TransportSettings3(
  [out, retval] IMsRdpClientTransportSettings3 **ppXportSet3
);
```



## <a name="property-value"></a><span data-ttu-id="e40f2-116">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e40f2-116">Property value</span></span>

<span data-ttu-id="e40f2-117">Indirizzo di un puntatore a interfaccia [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) che riceve l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e40f2-117">The address of an [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e40f2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e40f2-118">Requirements</span></span>



| <span data-ttu-id="e40f2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e40f2-119">Requirement</span></span> | <span data-ttu-id="e40f2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e40f2-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e40f2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e40f2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e40f2-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e40f2-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="e40f2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e40f2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e40f2-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e40f2-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="e40f2-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e40f2-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e40f2-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e40f2-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e40f2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e40f2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e40f2-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e40f2-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e40f2-129">IID</span><span class="sxs-lookup"><span data-stu-id="e40f2-129">IID</span></span><br/>                      | <span data-ttu-id="e40f2-130">IID \_ IMsRdpClient7 è definito come b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="e40f2-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e40f2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e40f2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e40f2-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e40f2-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e40f2-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e40f2-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e40f2-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e40f2-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e40f2-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e40f2-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





