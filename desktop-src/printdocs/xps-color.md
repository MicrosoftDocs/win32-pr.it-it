---
description: Struttura che descrive un singolo valore di colore.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (Xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c148c2a5452154bfe33b0c74d695fe78f0cdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317272"
---
# <a name="xps_color"></a><span data-ttu-id="fdfb4-103">\_colore XPS</span><span class="sxs-lookup"><span data-stu-id="fdfb4-103">XPS\_COLOR</span></span>

<span data-ttu-id="fdfb4-104">Struttura che descrive un singolo valore di colore.</span><span class="sxs-lookup"><span data-stu-id="fdfb4-104">A structure that describes a single color value.</span></span>

``` syntax
typedef union switch (XPS_COLOR_TYPE colorType) value
{
    case XPS_COLOR_TYPE_SRGB:
        struct {
            byte alpha, red, green, blue;
        } sRGB;
    case XPS_COLOR_TYPE_SCRGB:
        struct {
            FLOAT alpha, red, green, blue;
        } scRGB;
    case XPS_COLOR_TYPE_CONTEXT:
        struct {
            byte channelCount;
            FLOAT channels[9];
        } context;
} XPS_COLOR;
```

## <a name="remarks"></a><span data-ttu-id="fdfb4-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="fdfb4-105">Remarks</span></span>

<span data-ttu-id="fdfb4-106">Il formato della struttura dipende dal valore di *ColorType*.</span><span class="sxs-lookup"><span data-stu-id="fdfb4-106">The structure's format depends on the value of *colorType*.</span></span>

<dl>

<span data-ttu-id="fdfb4-107">[**\_tipo di colore XPS \_ \_ sRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fdfb4-107">[**XPS\_COLOR\_TYPE\_SRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span></span>  
<span data-ttu-id="fdfb4-108">[**\_tipo di colore XPS \_ \_**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fdfb4-108">[**XPS\_COLOR\_TYPE\_SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span></span>  
[<span data-ttu-id="fdfb4-109">**\_contesto del \_ tipo di colore XPS \_**</span><span class="sxs-lookup"><span data-stu-id="fdfb4-109">**XPS\_COLOR\_TYPE\_CONTEXT**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a><span data-ttu-id="fdfb4-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdfb4-110">Requirements</span></span>



| <span data-ttu-id="fdfb4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdfb4-111">Requirement</span></span> | <span data-ttu-id="fdfb4-112">Valore</span><span class="sxs-lookup"><span data-stu-id="fdfb4-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdfb4-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdfb4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="fdfb4-114">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fdfb4-114">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="fdfb4-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fdfb4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="fdfb4-116">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fdfb4-116">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="fdfb4-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fdfb4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdfb4-118"><dt>Xpsobjectmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdfb4-118"><dt>Xpsobjectmodel.h</dt></span></span> </dl>                                              |
| <span data-ttu-id="fdfb4-119">IDL</span><span class="sxs-lookup"><span data-stu-id="fdfb4-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fdfb4-120"><dt>XpsObjectModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fdfb4-120"><dt>XpsObjectModel.idl</dt></span></span> </dl>                                            |



## <a name="see-also"></a><span data-ttu-id="fdfb4-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdfb4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdfb4-122">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="fdfb4-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

