---
title: Proprietà RedirectDevices di IMsRdpClientAdvancedSettings5
description: Imposta o recupera la configurazione per il reindirizzamento del dispositivo.
ms.assetid: bf989ca0-5c79-4a73-a32b-51ef97ca0dff
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectDevices
- Servizi Desktop remoto proprietà RedirectDevices, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà RedirectDevices
- Servizi Desktop remoto proprietà RedirectDevices, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà RedirectDevices
- Servizi Desktop remoto proprietà RedirectDevices, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà RedirectDevices
- Servizi Desktop remoto proprietà RedirectDevices, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà RedirectDevices
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectDevices
- IMsRdpClientAdvancedSettings5.get_RedirectDevices
- IMsRdpClientAdvancedSettings5.put_RedirectDevices
- IMsRdpClientAdvancedSettings6.RedirectDevices
- IMsRdpClientAdvancedSettings6.get_RedirectDevices
- IMsRdpClientAdvancedSettings6.put_RedirectDevices
- IMsRdpClientAdvancedSettings7.RedirectDevices
- IMsRdpClientAdvancedSettings7.get_RedirectDevices
- IMsRdpClientAdvancedSettings7.put_RedirectDevices
- IMsRdpClientAdvancedSettings8.RedirectDevices
- IMsRdpClientAdvancedSettings8.get_RedirectDevices
- IMsRdpClientAdvancedSettings8.put_RedirectDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab1eec96b5d4fde20add891cc742c76c14ebe7ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301303"
---
# <a name="imsrdpclientadvancedsettings5redirectdevices-property"></a><span data-ttu-id="99e1e-112">Proprietà IMsRdpClientAdvancedSettings5:: RedirectDevices</span><span class="sxs-lookup"><span data-stu-id="99e1e-112">IMsRdpClientAdvancedSettings5::RedirectDevices property</span></span>

<span data-ttu-id="99e1e-113">Imposta o recupera la configurazione per il reindirizzamento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99e1e-113">Sets or retrieves the configuration for device redirection.</span></span>

<span data-ttu-id="99e1e-114">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="99e1e-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e1e-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99e1e-115">Syntax</span></span>


```C++
HRESULT put_RedirectDevices(
  [in]  VARIANT_BOOL fRedirectPnPDevices
);

HRESULT get_RedirectDevices(
  [out] VARIANT_BOOL *pfRedirectPnPDevices
);
```



## <a name="property-value"></a><span data-ttu-id="99e1e-116">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="99e1e-116">Property value</span></span>

<span data-ttu-id="99e1e-117">Imposta la modalità di reindirizzamento del dispositivo su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="99e1e-117">Sets the device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="99e1e-118">Se è impostato su **true**, la modalità di reindirizzamento del dispositivo è abilitata.</span><span class="sxs-lookup"><span data-stu-id="99e1e-118">If set to **TRUE**, device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="99e1e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99e1e-119">Requirements</span></span>



| <span data-ttu-id="99e1e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="99e1e-120">Requirement</span></span> | <span data-ttu-id="99e1e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="99e1e-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99e1e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99e1e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="99e1e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99e1e-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="99e1e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99e1e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="99e1e-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99e1e-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="99e1e-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="99e1e-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="99e1e-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99e1e-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="99e1e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="99e1e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99e1e-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99e1e-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="99e1e-130">IID</span><span class="sxs-lookup"><span data-stu-id="99e1e-130">IID</span></span><br/>                      | <span data-ttu-id="99e1e-131">IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="99e1e-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99e1e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99e1e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e1e-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="99e1e-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="99e1e-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="99e1e-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="99e1e-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="99e1e-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="99e1e-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="99e1e-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





