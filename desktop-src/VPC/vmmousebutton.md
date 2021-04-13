---
title: Enumerazione VMMouseButton (VPCCOMInterfaces. h)
description: Specifica il pulsante del mouse.
ms.assetid: d09e63cb-9dc5-424f-b130-c0b0dd07fe11
keywords:
- VMMouseButton enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMMouseButton
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18744af5a4f8068b9bb371cb15e06c365561f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478310"
---
# <a name="vmmousebutton-enumeration"></a><span data-ttu-id="da81c-104">Enumerazione VMMouseButton</span><span class="sxs-lookup"><span data-stu-id="da81c-104">VMMouseButton enumeration</span></span>

<span data-ttu-id="da81c-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="da81c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="da81c-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="da81c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="da81c-107">Specifica il pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="da81c-107">Specifies the mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="da81c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da81c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmMouseButton_Left    = 1,
  vmMouseButton_Right   = 2,
  vmMouseButton_Center  = 3
} VMMouseButton;
```



## <a name="constants"></a><span data-ttu-id="da81c-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="da81c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="da81c-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton a \_ sinistra**</span><span class="sxs-lookup"><span data-stu-id="da81c-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton\_Left**</span></span>
</dt> <dd>

<span data-ttu-id="da81c-111">Rappresenta il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="da81c-111">The left mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="da81c-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton a \_ destra**</span><span class="sxs-lookup"><span data-stu-id="da81c-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton\_Right**</span></span>
</dt> <dd>

<span data-ttu-id="da81c-113">Rappresenta il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="da81c-113">The right mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="da81c-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**\_centro vmMouseButton**</span><span class="sxs-lookup"><span data-stu-id="da81c-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmMouseButton\_Center**</span></span>
</dt> <dd>

<span data-ttu-id="da81c-115">Pulsante centrale del mouse.</span><span class="sxs-lookup"><span data-stu-id="da81c-115">The center mouse button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da81c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da81c-116">Requirements</span></span>



| <span data-ttu-id="da81c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="da81c-117">Requirement</span></span> | <span data-ttu-id="da81c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="da81c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="da81c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da81c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="da81c-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="da81c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da81c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da81c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="da81c-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="da81c-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="da81c-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="da81c-123">End of client support</span></span><br/>    | <span data-ttu-id="da81c-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="da81c-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="da81c-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="da81c-125">Product</span></span><br/>                  | <span data-ttu-id="da81c-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="da81c-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="da81c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da81c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="da81c-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="da81c-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da81c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da81c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da81c-130">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="da81c-130">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

