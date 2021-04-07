---
title: Proprietà RemoteProgram2 di IMsRdpClient7
description: Recupera un oggetto che supporta l'interfaccia ITSRemoteProgram2.
ms.assetid: fabdc933-c941-487f-9e49-c20a39e0c86e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RemoteProgram2
- Servizi Desktop remoto proprietà RemoteProgram2, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà RemoteProgram2
- Servizi Desktop remoto proprietà RemoteProgram2, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà RemoteProgram2
- Servizi Desktop remoto proprietà RemoteProgram2, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà RemoteProgram2
- Servizi Desktop remoto proprietà RemoteProgram2, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà RemoteProgram2
topic_type:
- apiref
api_name:
- IMsRdpClient7.RemoteProgram2
- IMsRdpClient7.get_RemoteProgram2
- IMsRdpClient8.RemoteProgram2
- IMsRdpClient8.get_RemoteProgram2
- IMsRdpClient9.RemoteProgram2
- IMsRdpClient9.get_RemoteProgram2
- IMsRdpClient10.RemoteProgram2
- IMsRdpClient10.get_RemoteProgram2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1572aada1384a7edfe88b198826050927ae3cff5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963907"
---
# <a name="imsrdpclient7remoteprogram2-property"></a><span data-ttu-id="f05c7-112">Proprietà IMsRdpClient7:: RemoteProgram2</span><span class="sxs-lookup"><span data-stu-id="f05c7-112">IMsRdpClient7::RemoteProgram2 property</span></span>

<span data-ttu-id="f05c7-113">Recupera un oggetto che supporta l'interfaccia [**ITSRemoteProgram2**](itsremoteprogram2.md) .</span><span class="sxs-lookup"><span data-stu-id="f05c7-113">Retrieves an object that supports the [**ITSRemoteProgram2**](itsremoteprogram2.md) interface.</span></span>

<span data-ttu-id="f05c7-114">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f05c7-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f05c7-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f05c7-115">Syntax</span></span>


```C++
HRESULT get_RemoteProgram2(
  [out, retval] ITSRemoteProgram2 **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="f05c7-116">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f05c7-116">Property value</span></span>

<span data-ttu-id="f05c7-117">Indirizzo di un puntatore a interfaccia [**ITSRemoteProgram2**](itsremoteprogram2.md) che riceve l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f05c7-117">The address of an [**ITSRemoteProgram2**](itsremoteprogram2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f05c7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f05c7-118">Requirements</span></span>



| <span data-ttu-id="f05c7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f05c7-119">Requirement</span></span> | <span data-ttu-id="f05c7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f05c7-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f05c7-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f05c7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f05c7-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f05c7-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="f05c7-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f05c7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f05c7-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f05c7-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="f05c7-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f05c7-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="f05c7-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f05c7-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f05c7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f05c7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f05c7-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f05c7-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f05c7-129">IID</span><span class="sxs-lookup"><span data-stu-id="f05c7-129">IID</span></span><br/>                      | <span data-ttu-id="f05c7-130">IID \_ IMsRdpClient7 è definito come b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="f05c7-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f05c7-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f05c7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f05c7-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f05c7-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f05c7-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f05c7-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f05c7-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f05c7-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f05c7-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="f05c7-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





