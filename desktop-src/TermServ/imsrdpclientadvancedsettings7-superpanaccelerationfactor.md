---
title: Proprietà SuperPanAccelerationFactor di IMsRdpClientAdvancedSettings7
description: Specifica o recupera un valore che indica il fattore di accelerazione SuperPan. Il fattore di accelerazione SuperPan determina la rapidità con cui lo schermo esegue il Pan in modalità SuperPan.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SuperPanAccelerationFactor
- Servizi Desktop remoto proprietà SuperPanAccelerationFactor, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà SuperPanAccelerationFactor
- Servizi Desktop remoto proprietà SuperPanAccelerationFactor, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà SuperPanAccelerationFactor
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964979"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a><span data-ttu-id="fd164-109">Proprietà IMsRdpClientAdvancedSettings7:: SuperPanAccelerationFactor</span><span class="sxs-lookup"><span data-stu-id="fd164-109">IMsRdpClientAdvancedSettings7::SuperPanAccelerationFactor property</span></span>

<span data-ttu-id="fd164-110">Specifica o recupera un valore che indica il fattore di accelerazione SuperPan.</span><span class="sxs-lookup"><span data-stu-id="fd164-110">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span> <span data-ttu-id="fd164-111">Il fattore di accelerazione SuperPan determina la rapidità con cui lo schermo esegue il Pan in modalità SuperPan.</span><span class="sxs-lookup"><span data-stu-id="fd164-111">The SuperPan acceleration factor determines how quickly the screen pans when in SuperPan mode.</span></span> <span data-ttu-id="fd164-112">Il fattore di accelerazione è il numero di pixel che la visualizzazione schermo scorre in una determinata direzione per ogni pixel del movimento del mouse da parte del client.</span><span class="sxs-lookup"><span data-stu-id="fd164-112">The acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement by the client.</span></span>

<span data-ttu-id="fd164-113">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fd164-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd164-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd164-114">Syntax</span></span>


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a><span data-ttu-id="fd164-115">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fd164-115">Property value</span></span>

<span data-ttu-id="fd164-116">Fattore di accelerazione SuperPan da impostare.</span><span class="sxs-lookup"><span data-stu-id="fd164-116">The SuperPan acceleration factor to set.</span></span> <span data-ttu-id="fd164-117">Il fattore di accelerazione SuperPan è il numero di pixel che la visualizzazione schermo scorre in una determinata direzione per ogni pixel del movimento del mouse.</span><span class="sxs-lookup"><span data-stu-id="fd164-117">The SuperPan acceleration factor is the number of pixels that the screen view scrolls in a given direction for every pixel of mouse movement.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd164-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd164-118">Remarks</span></span>

<span data-ttu-id="fd164-119">Per ulteriori informazioni su SuperPan, vedere [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span><span class="sxs-lookup"><span data-stu-id="fd164-119">For more information about SuperPan, see [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd164-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd164-120">Requirements</span></span>



| <span data-ttu-id="fd164-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd164-121">Requirement</span></span> | <span data-ttu-id="fd164-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fd164-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd164-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd164-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fd164-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd164-124">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="fd164-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd164-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fd164-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fd164-126">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="fd164-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fd164-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="fd164-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd164-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fd164-129">DLL</span><span class="sxs-lookup"><span data-stu-id="fd164-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd164-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd164-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="fd164-131">IID</span><span class="sxs-lookup"><span data-stu-id="fd164-131">IID</span></span><br/>                      | <span data-ttu-id="fd164-132">IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="fd164-132">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd164-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd164-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd164-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fd164-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fd164-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fd164-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fd164-136">**EnableSuperPan**</span><span class="sxs-lookup"><span data-stu-id="fd164-136">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





