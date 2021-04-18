---
title: Proprietà AdvancedSettings9 di IMsRdpClient8
description: Contiene un oggetto che supporta l'interfaccia IMsRdpClientAdvancedSettings8.
ms.assetid: eb7bf118-15e7-4a11-91b1-e48f18afb436
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AdvancedSettings9
- Servizi Desktop remoto proprietà AdvancedSettings9, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, proprietà AdvancedSettings9
- Servizi Desktop remoto proprietà AdvancedSettings9, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, proprietà AdvancedSettings9
- Servizi Desktop remoto proprietà AdvancedSettings9, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, proprietà AdvancedSettings9
topic_type:
- apiref
api_name:
- IMsRdpClient8.AdvancedSettings9
- IMsRdpClient8.get_AdvancedSettings9
- IMsRdpClient9.AdvancedSettings9
- IMsRdpClient9.get_AdvancedSettings9
- IMsRdpClient10.AdvancedSettings9
- IMsRdpClient10.get_AdvancedSettings9
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fce4c6f07b0c6c798d613e5312b3ae2b258c9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302744"
---
# <a name="imsrdpclient8advancedsettings9-property"></a><span data-ttu-id="f207a-110">Proprietà IMsRdpClient8:: AdvancedSettings9</span><span class="sxs-lookup"><span data-stu-id="f207a-110">IMsRdpClient8::AdvancedSettings9 property</span></span>

<span data-ttu-id="f207a-111">Contiene un oggetto che supporta l'interfaccia [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) .</span><span class="sxs-lookup"><span data-stu-id="f207a-111">Contains an object that supports the [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface.</span></span>

<span data-ttu-id="f207a-112">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f207a-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f207a-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f207a-113">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings9(
  [out, retval] IMsRdpClientAdvancedSettings8 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="f207a-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f207a-114">Property value</span></span>

<span data-ttu-id="f207a-115">Interfaccia [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) che rappresenta l'oggetto Settings.</span><span class="sxs-lookup"><span data-stu-id="f207a-115">An [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface that represents the settings object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f207a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f207a-116">Requirements</span></span>



| <span data-ttu-id="f207a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f207a-117">Requirement</span></span> | <span data-ttu-id="f207a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f207a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f207a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f207a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f207a-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f207a-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="f207a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f207a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f207a-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f207a-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="f207a-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f207a-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="f207a-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f207a-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f207a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f207a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f207a-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f207a-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f207a-127">IID</span><span class="sxs-lookup"><span data-stu-id="f207a-127">IID</span></span><br/>                      | <span data-ttu-id="f207a-128">IID \_ IMsRdpClient8 è definito come 4247E044-9271-43a9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="f207a-128">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f207a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f207a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f207a-130">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f207a-130">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f207a-131">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f207a-131">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f207a-132">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="f207a-132">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





