---
title: Enumerazione VMDisplayVideoMode (VPCCOMInterfaces. h)
description: Specifica la modalità video di visualizzazione.
ms.assetid: 9ffd1bb5-115d-4554-92c6-5dcf86f904a5
keywords:
- VMDisplayVideoMode enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMDisplayVideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b159a8c251c83643ae9897842b313ea9be567e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476546"
---
# <a name="vmdisplayvideomode-enumeration"></a><span data-ttu-id="0c2b0-104">Enumerazione VMDisplayVideoMode</span><span class="sxs-lookup"><span data-stu-id="0c2b0-104">VMDisplayVideoMode enumeration</span></span>

<span data-ttu-id="0c2b0-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0c2b0-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0c2b0-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0c2b0-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0c2b0-107">Specifica la modalità video di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0c2b0-107">Specifies the display video mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c2b0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c2b0-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVideoMode_TextMode  = 0,
  vmVideoMode_CGAMode   = 1,
  vmVideoMode_VGAMode   = 2,
  vmVideoMode_SVGAMode  = 3
} VMDisplayVideoMode;
```



## <a name="constants"></a><span data-ttu-id="0c2b0-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="0c2b0-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0c2b0-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**TextMode vmVideoMode \_**</span><span class="sxs-lookup"><span data-stu-id="0c2b0-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmVideoMode\_TextMode**</span></span>
</dt> <dd>

<span data-ttu-id="0c2b0-111">Modalità testo.</span><span class="sxs-lookup"><span data-stu-id="0c2b0-111">Text mode.</span></span>

</dd> <dt>

<span data-ttu-id="0c2b0-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**\_CGAMode vmVideoMode**</span><span class="sxs-lookup"><span data-stu-id="0c2b0-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmVideoMode\_CGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="0c2b0-113">Modalità CGA.</span><span class="sxs-lookup"><span data-stu-id="0c2b0-113">CGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="0c2b0-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**\_VGAMode vmVideoMode**</span><span class="sxs-lookup"><span data-stu-id="0c2b0-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmVideoMode\_VGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="0c2b0-115">Modalità VGA.</span><span class="sxs-lookup"><span data-stu-id="0c2b0-115">VGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="0c2b0-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**\_SVGAMode vmVideoMode**</span><span class="sxs-lookup"><span data-stu-id="0c2b0-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmVideoMode\_SVGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="0c2b0-117">Modalità SVGA.</span><span class="sxs-lookup"><span data-stu-id="0c2b0-117">SVGA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c2b0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c2b0-118">Requirements</span></span>



| <span data-ttu-id="0c2b0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c2b0-119">Requirement</span></span> | <span data-ttu-id="0c2b0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0c2b0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c2b0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c2b0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0c2b0-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0c2b0-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c2b0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c2b0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0c2b0-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0c2b0-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0c2b0-125">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0c2b0-125">End of client support</span></span><br/>    | <span data-ttu-id="0c2b0-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c2b0-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0c2b0-127">Prodotto</span><span class="sxs-lookup"><span data-stu-id="0c2b0-127">Product</span></span><br/>                  | <span data-ttu-id="0c2b0-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0c2b0-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0c2b0-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c2b0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c2b0-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c2b0-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c2b0-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c2b0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c2b0-132">**IVMDisplay:: VideoMode**</span><span class="sxs-lookup"><span data-stu-id="0c2b0-132">**IVMDisplay::VideoMode**</span></span>](ivmdisplay-videomode.md)
</dt> </dl>

 

