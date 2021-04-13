---
title: Proprietà di IMsRdpClientNonScriptable3 Drivecollection
description: Recupera la raccolta di oggetti unità da reindirizzare.
ms.assetid: 5aaac605-584b-442e-9d67-1cb8213a70b3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà di drivecollection
- Servizi Desktop remoto proprietà di drivecollection, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà Drivecollection
- Servizi Desktop remoto proprietà di drivecollection, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà Drivecollection
- Servizi Desktop remoto proprietà di drivecollection, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà Drivecollection
- Servizi Desktop remoto proprietà di drivecollection, oggetto MsRdpClient5
- Servizi Desktop remoto oggetto MsRdpClient5, proprietà Drivecollection
- Servizi Desktop remoto proprietà di drivecollection, oggetto MsRdpClient6
- Servizi Desktop remoto oggetto MsRdpClient6, proprietà Drivecollection
- Servizi Desktop remoto proprietà di drivecollection, oggetto MsRdpClient7
- Servizi Desktop remoto oggetto MsRdpClient7, proprietà Drivecollection
- Servizi Desktop remoto proprietà di drivecollection, oggetto MsRdpClient8
- Servizi Desktop remoto oggetto MsRdpClient8, proprietà Drivecollection
- Servizi Desktop remoto proprietà di drivecollection, oggetto MsRdpClient9
- Servizi Desktop remoto oggetto MsRdpClient9, proprietà Drivecollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DriveCollection
- IMsRdpClientNonScriptable3.get_DriveCollection
- IMsRdpClientNonScriptable4.DriveCollection
- IMsRdpClientNonScriptable4.get_DriveCollection
- IMsRdpClientNonScriptable5.DriveCollection
- IMsRdpClientNonScriptable5.get_DriveCollection
- MsRdpClient5.DriveCollection
- MsRdpClient6.DriveCollection
- MsRdpClient7.DriveCollection
- MsRdpClient8.DriveCollection
- MsRdpClient9.DriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37d4bfcaa52d483adc8b0d0885d8316f10ce01d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475784"
---
# <a name="imsrdpclientnonscriptable3drivecollection-property"></a><span data-ttu-id="21405-120">IMsRdpClientNonScriptable3::D Proprietà rivecollection</span><span class="sxs-lookup"><span data-stu-id="21405-120">IMsRdpClientNonScriptable3::DriveCollection property</span></span>

<span data-ttu-id="21405-121">Recupera la raccolta di oggetti unità da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="21405-121">Retrieves the collection of drive objects to be redirected.</span></span>

<span data-ttu-id="21405-122">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="21405-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="21405-123">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21405-123">Syntax</span></span>


```C++
HRESULT get_DriveCollection(
  [out] IMsRdpDriveCollection **ppDriveCollection
);
```



## <a name="property-value"></a><span data-ttu-id="21405-124">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="21405-124">Property value</span></span>

<span data-ttu-id="21405-125">Recupera la raccolta di oggetti unità di tipo [**IMSRdpDrive**](imsrdpdrive.md).</span><span class="sxs-lookup"><span data-stu-id="21405-125">Retrieves the collection of drive objects of type [**IMSRdpDrive**](imsrdpdrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="21405-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21405-126">Requirements</span></span>



| <span data-ttu-id="21405-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="21405-127">Requirement</span></span> | <span data-ttu-id="21405-128">Valore</span><span class="sxs-lookup"><span data-stu-id="21405-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="21405-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21405-129">Minimum supported client</span></span><br/> | <span data-ttu-id="21405-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21405-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="21405-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21405-131">Minimum supported server</span></span><br/> | <span data-ttu-id="21405-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21405-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="21405-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="21405-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="21405-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21405-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="21405-135">DLL</span><span class="sxs-lookup"><span data-stu-id="21405-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21405-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21405-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="21405-137">IID</span><span class="sxs-lookup"><span data-stu-id="21405-137">IID</span></span><br/>                      | <span data-ttu-id="21405-138">IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="21405-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="21405-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21405-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21405-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="21405-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="21405-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="21405-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="21405-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="21405-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





