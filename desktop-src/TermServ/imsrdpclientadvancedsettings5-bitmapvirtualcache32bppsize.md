---
title: Proprietà BitmapVirtualCache32BppSize di IMsRdpClientAdvancedSettings5
description: Imposta o recupera le dimensioni del file della cache virtuale per le bitmap di 32 bit per pixel (BPP).
ms.assetid: 7084293a-ae75-4711-a8d8-f813117333e7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà BitmapVirtualCache32BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache32BppSize, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà BitmapVirtualCache32BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache32BppSize, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà BitmapVirtualCache32BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache32BppSize, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà BitmapVirtualCache32BppSize
- Servizi Desktop remoto proprietà BitmapVirtualCache32BppSize, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà BitmapVirtualCache32BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache32BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d43de82b97e16fa36f83a5edde43712b2a9cbbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400444"
---
# <a name="imsrdpclientadvancedsettings5bitmapvirtualcache32bppsize-property"></a><span data-ttu-id="f6131-112">Proprietà IMsRdpClientAdvancedSettings5:: BitmapVirtualCache32BppSize</span><span class="sxs-lookup"><span data-stu-id="f6131-112">IMsRdpClientAdvancedSettings5::BitmapVirtualCache32BppSize property</span></span>

<span data-ttu-id="f6131-113">Imposta o recupera le dimensioni del file della cache virtuale per le bitmap di 32 bit per pixel (BPP).</span><span class="sxs-lookup"><span data-stu-id="f6131-113">Sets or retrieves the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span>

<span data-ttu-id="f6131-114">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f6131-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6131-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6131-115">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache32BppSize(
  [in]  LONG bitmapVirtualCache32BppSize
);

HRESULT get_BitmapVirtualCache32BppSize(
  [out] LONG *pbitmapVirtualCache32BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="f6131-116">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f6131-116">Property value</span></span>

<span data-ttu-id="f6131-117">Imposta la dimensione del file di cache virtuale per le bitmap di 32 BPP, in megabyte (MB).</span><span class="sxs-lookup"><span data-stu-id="f6131-117">Sets the size of the virtual cache file for 32 bpp bitmaps, in megabytes (MB).</span></span> <span data-ttu-id="f6131-118">Il valore massimo è 48 MB.</span><span class="sxs-lookup"><span data-stu-id="f6131-118">The maximum value is 48 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6131-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6131-119">Requirements</span></span>



| <span data-ttu-id="f6131-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6131-120">Requirement</span></span> | <span data-ttu-id="f6131-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f6131-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6131-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6131-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6131-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6131-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="f6131-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6131-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6131-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6131-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="f6131-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f6131-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="f6131-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6131-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="f6131-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f6131-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6131-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6131-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="f6131-130">IID</span><span class="sxs-lookup"><span data-stu-id="f6131-130">IID</span></span><br/>                      | <span data-ttu-id="f6131-131">IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="f6131-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6131-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6131-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6131-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f6131-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f6131-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f6131-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f6131-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f6131-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f6131-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f6131-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





