---
title: Proprietà AdvancedSettings8 di IMsRdpClient7
description: Recupera un oggetto che supporta l'interfaccia IMsRdpClientAdvancedSettings7.
ms.assetid: e3bb3b74-52db-4ec2-999c-9d12c24f65be
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings8
- Servizi Desktop remoto proprietà AdvancedSettings8, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà AdvancedSettings8
- Servizi Desktop remoto proprietà AdvancedSettings8, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings8
- Servizi Desktop remoto proprietà AdvancedSettings8, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings8
- Servizi Desktop remoto proprietà AdvancedSettings8, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà AdvancedSettings8
topic_type:
- apiref
api_name:
- IMsRdpClient7.AdvancedSettings8
- IMsRdpClient7.get_AdvancedSettings8
- IMsRdpClient8.AdvancedSettings8
- IMsRdpClient8.get_AdvancedSettings8
- IMsRdpClient9.AdvancedSettings8
- IMsRdpClient9.get_AdvancedSettings8
- IMsRdpClient10.AdvancedSettings8
- IMsRdpClient10.get_AdvancedSettings8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 887306216682ba1555739a4258b8337694fabe0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119195"
---
# <a name="imsrdpclient7advancedsettings8-property"></a><span data-ttu-id="1cb55-112">Proprietà IMsRdpClient7:: AdvancedSettings8</span><span class="sxs-lookup"><span data-stu-id="1cb55-112">IMsRdpClient7::AdvancedSettings8 property</span></span>

<span data-ttu-id="1cb55-113">Recupera un oggetto che supporta l'interfaccia [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .</span><span class="sxs-lookup"><span data-stu-id="1cb55-113">Retrieves an object that supports the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface.</span></span>

<span data-ttu-id="1cb55-114">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1cb55-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cb55-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cb55-115">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings8(
  [out, retval] IMsRdpClientAdvancedSettings7 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="1cb55-116">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1cb55-116">Property value</span></span>

<span data-ttu-id="1cb55-117">Indirizzo di un puntatore a interfaccia [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) che riceve l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1cb55-117">The address of an [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cb55-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cb55-118">Requirements</span></span>



| <span data-ttu-id="1cb55-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cb55-119">Requirement</span></span> | <span data-ttu-id="1cb55-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1cb55-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb55-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cb55-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1cb55-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1cb55-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="1cb55-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1cb55-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1cb55-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1cb55-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="1cb55-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1cb55-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="1cb55-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cb55-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1cb55-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1cb55-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cb55-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cb55-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1cb55-129">IID</span><span class="sxs-lookup"><span data-stu-id="1cb55-129">IID</span></span><br/>                      | <span data-ttu-id="1cb55-130">IID \_ IMsRdpClient7 è definito come b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="1cb55-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1cb55-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cb55-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb55-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="1cb55-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="1cb55-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="1cb55-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="1cb55-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="1cb55-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="1cb55-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="1cb55-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





