---
title: Proprietà SecuredSettings3 di IMsRdpClient7
description: Recupera un oggetto che supporta l'interfaccia IMsRdpClientSecuredSettings2.
ms.assetid: 500ce7ed-bd86-434c-baf8-f30dd667dca3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SecuredSettings3
- Servizi Desktop remoto proprietà SecuredSettings3, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, proprietà SecuredSettings3
- Servizi Desktop remoto proprietà SecuredSettings3, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà SecuredSettings3
- Servizi Desktop remoto proprietà SecuredSettings3, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà SecuredSettings3
- Servizi Desktop remoto proprietà SecuredSettings3, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà SecuredSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.SecuredSettings3
- IMsRdpClient7.get_SecuredSettings3
- IMsRdpClient8.SecuredSettings3
- IMsRdpClient8.get_SecuredSettings3
- IMsRdpClient9.SecuredSettings3
- IMsRdpClient9.get_SecuredSettings3
- IMsRdpClient10.SecuredSettings3
- IMsRdpClient10.get_SecuredSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 219e3373a6ecb2f5b963a82800f4415f7de64534
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400390"
---
# <a name="imsrdpclient7securedsettings3-property"></a><span data-ttu-id="609f8-112">Proprietà IMsRdpClient7:: SecuredSettings3</span><span class="sxs-lookup"><span data-stu-id="609f8-112">IMsRdpClient7::SecuredSettings3 property</span></span>

<span data-ttu-id="609f8-113">Recupera un oggetto che supporta l'interfaccia [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="609f8-113">Retrieves an object that supports the [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface.</span></span>

<span data-ttu-id="609f8-114">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="609f8-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="609f8-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="609f8-115">Syntax</span></span>


```C++
HRESULT get_SecuredSettings3(
  [out] IMsRdpClientSecuredSettings2 **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="609f8-116">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="609f8-116">Property value</span></span>

<span data-ttu-id="609f8-117">Indirizzo di un puntatore a interfaccia [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) che riceve l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="609f8-117">The address of an [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="609f8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="609f8-118">Requirements</span></span>



| <span data-ttu-id="609f8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="609f8-119">Requirement</span></span> | <span data-ttu-id="609f8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="609f8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="609f8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="609f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="609f8-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="609f8-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="609f8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="609f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="609f8-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="609f8-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="609f8-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="609f8-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="609f8-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="609f8-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="609f8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="609f8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="609f8-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="609f8-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="609f8-129">IID</span><span class="sxs-lookup"><span data-stu-id="609f8-129">IID</span></span><br/>                      | <span data-ttu-id="609f8-130">IID \_ IMsRdpClient7 è definito come b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="609f8-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="609f8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="609f8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="609f8-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="609f8-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="609f8-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="609f8-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="609f8-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="609f8-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="609f8-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="609f8-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





