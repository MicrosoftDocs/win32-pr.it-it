---
title: Proprietà RedirectPOSDevices di IMsRdpClientAdvancedSettings5
description: Imposta o recupera la configurazione per il reindirizzamento del dispositivo del punto di servizio.
ms.assetid: 2614048e-244d-4dea-96fb-bb8c563a29f9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectPOSDevices
- Servizi Desktop remoto proprietà RedirectPOSDevices, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà RedirectPOSDevices
- Servizi Desktop remoto proprietà RedirectPOSDevices, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà RedirectPOSDevices
- Servizi Desktop remoto proprietà RedirectPOSDevices, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà RedirectPOSDevices
- Servizi Desktop remoto proprietà RedirectPOSDevices, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà RedirectPOSDevices
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.put_RedirectPOSDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5ceb0c1fb9751b137b5791ce9c8da1bd0cdbb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120402"
---
# <a name="imsrdpclientadvancedsettings5redirectposdevices-property"></a><span data-ttu-id="42b0f-112">Proprietà IMsRdpClientAdvancedSettings5:: RedirectPOSDevices</span><span class="sxs-lookup"><span data-stu-id="42b0f-112">IMsRdpClientAdvancedSettings5::RedirectPOSDevices property</span></span>

<span data-ttu-id="42b0f-113">Imposta o recupera la configurazione per il reindirizzamento del dispositivo del punto di servizio.</span><span class="sxs-lookup"><span data-stu-id="42b0f-113">Sets or retrieves the configuration for Point of Service device redirection.</span></span>

<span data-ttu-id="42b0f-114">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="42b0f-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b0f-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42b0f-115">Syntax</span></span>


```C++
HRESULT put_RedirectPOSDevices(
  [in]  VARIANT_BOOL fRedirectPOSDevices
);

HRESULT get_RedirectPOSDevices(
  [out] VARIANT_BOOL *pfRedirectPOSDevices
);
```



## <a name="property-value"></a><span data-ttu-id="42b0f-116">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="42b0f-116">Property value</span></span>

<span data-ttu-id="42b0f-117">Imposta la modalità di reindirizzamento del dispositivo punto di servizio su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="42b0f-117">Sets Point of Service device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="42b0f-118">Se impostato su **true**, la modalità di reindirizzamento del dispositivo del punto di servizio è abilitata.</span><span class="sxs-lookup"><span data-stu-id="42b0f-118">If set to **TRUE**, Point of Service device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="42b0f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42b0f-119">Requirements</span></span>



| <span data-ttu-id="42b0f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="42b0f-120">Requirement</span></span> | <span data-ttu-id="42b0f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="42b0f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b0f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42b0f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="42b0f-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42b0f-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="42b0f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42b0f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="42b0f-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42b0f-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="42b0f-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="42b0f-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="42b0f-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42b0f-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="42b0f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="42b0f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42b0f-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42b0f-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="42b0f-130">IID</span><span class="sxs-lookup"><span data-stu-id="42b0f-130">IID</span></span><br/>                      | <span data-ttu-id="42b0f-131">IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="42b0f-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42b0f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42b0f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b0f-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="42b0f-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="42b0f-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="42b0f-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="42b0f-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="42b0f-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="42b0f-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="42b0f-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





