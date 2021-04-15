---
title: Proprietà Devicecollection IMsRdpClientNonScriptable3
description: Recupera la raccolta di oggetti dispositivo Plug and Play (PnP) da reindirizzare.
ms.assetid: dd5fe4c7-58bf-4e7a-b066-59278419ea6f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà devicecollection
- Servizi Desktop remoto proprietà devicecollection, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà Devicecollection
- Servizi Desktop remoto proprietà devicecollection, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà Devicecollection
- Servizi Desktop remoto proprietà devicecollection, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà Devicecollection
- Servizi Desktop remoto proprietà devicecollection, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà Devicecollection
- Servizi Desktop remoto proprietà devicecollection, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà Devicecollection
- Servizi Desktop remoto proprietà devicecollection, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà Devicecollection
- Servizi Desktop remoto proprietà devicecollection, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà Devicecollection
- Servizi Desktop remoto proprietà devicecollection, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà Devicecollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DeviceCollection
- IMsRdpClientNonScriptable3.get_DeviceCollection
- IMsRdpClientNonScriptable4.DeviceCollection
- IMsRdpClientNonScriptable4.get_DeviceCollection
- IMsRdpClientNonScriptable5.DeviceCollection
- IMsRdpClientNonScriptable5.get_DeviceCollection
- MsRdpClient5.DeviceCollection
- MsRdpClient6.DeviceCollection
- MsRdpClient7.DeviceCollection
- MsRdpClient8.DeviceCollection
- MsRdpClient9.DeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a545d2f4aaae2af68c14dd6531a2c57cf73711dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400384"
---
# <a name="imsrdpclientnonscriptable3devicecollection-property"></a><span data-ttu-id="ff29f-120">IMsRdpClientNonScriptable3::D Proprietà eviceCollection</span><span class="sxs-lookup"><span data-stu-id="ff29f-120">IMsRdpClientNonScriptable3::DeviceCollection property</span></span>

<span data-ttu-id="ff29f-121">Recupera la raccolta di oggetti dispositivo Plug and Play (PnP) da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="ff29f-121">Retrieves the collection of Plug and Play (PnP) device objects to be redirected.</span></span>

<span data-ttu-id="ff29f-122">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ff29f-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff29f-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff29f-123">Syntax</span></span>


```C++
HRESULT get_DeviceCollection(
  [out] IMSRdpDeviceCollection **ppDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="ff29f-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ff29f-124">Property value</span></span>

<span data-ttu-id="ff29f-125">Recupera la raccolta di oggetti dispositivo PnP di tipo [**IMSRdpDevice**](imsrdpdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ff29f-125">Retrieves the collection of PnP device objects of type [**IMSRdpDevice**](imsrdpdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff29f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff29f-126">Requirements</span></span>



| <span data-ttu-id="ff29f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff29f-127">Requirement</span></span> | <span data-ttu-id="ff29f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ff29f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff29f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff29f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ff29f-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff29f-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="ff29f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff29f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ff29f-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff29f-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="ff29f-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ff29f-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff29f-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff29f-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="ff29f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ff29f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff29f-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff29f-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="ff29f-137">IID</span><span class="sxs-lookup"><span data-stu-id="ff29f-137">IID</span></span><br/>                      | <span data-ttu-id="ff29f-138">IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="ff29f-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff29f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff29f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff29f-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="ff29f-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="ff29f-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="ff29f-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="ff29f-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="ff29f-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





