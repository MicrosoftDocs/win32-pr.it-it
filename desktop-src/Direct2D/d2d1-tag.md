---
title: D2D1_TAG (D2d1. h)
description: Valore a 64 bit definito dall'applicazione usato per \ 160; contrassegnare un set di operazioni di rendering.
ms.assetid: 4f363295-f140-4149-ba78-3abbc56eebe8
keywords:
- D2D1_TAG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacd11aa016e64ed463f1809595c865ae7e1f124
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340573"
---
# <a name="d2d1_tag"></a><span data-ttu-id="f5db5-104">\_Tag d2d1</span><span class="sxs-lookup"><span data-stu-id="f5db5-104">D2D1\_TAG</span></span>

<span data-ttu-id="f5db5-105">Valore a 64 bit definito dall'applicazione utilizzato per contrassegnare un set di operazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="f5db5-105">An application-defined 64-bit value used to mark a set of rendering operations.</span></span>


```C++
typedef UINT64 D2D1_TAG;
```



## <a name="remarks"></a><span data-ttu-id="f5db5-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5db5-106">Remarks</span></span>

<span data-ttu-id="f5db5-107">Per impostare un tag prima di una serie di operazioni di rendering, usare il metodo [**ID2D1RenderTarget:: setags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .</span><span class="sxs-lookup"><span data-stu-id="f5db5-107">To set a tag before a series of rendering operations, use the [**ID2D1RenderTarget::SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) method.</span></span> <span data-ttu-id="f5db5-108">Per recuperare il tag corrente, usare il metodo [**ID2D1RenderTarget:: GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) .</span><span class="sxs-lookup"><span data-stu-id="f5db5-108">To retrieve the current tag, use the [**ID2D1RenderTarget::GetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5db5-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5db5-109">Requirements</span></span>



| <span data-ttu-id="f5db5-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5db5-110">Requirement</span></span> | <span data-ttu-id="f5db5-111">Valore</span><span class="sxs-lookup"><span data-stu-id="f5db5-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5db5-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5db5-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f5db5-113">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f5db5-113">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="f5db5-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5db5-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f5db5-115">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f5db5-115">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f5db5-116">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5db5-116">Minimum supported phone</span></span><br/>  | <span data-ttu-id="f5db5-117">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="f5db5-117">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="f5db5-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5db5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5db5-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5db5-119"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="f5db5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5db5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5db5-121">**GetTags**</span><span class="sxs-lookup"><span data-stu-id="f5db5-121">**GetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-gettags)
</dt> <dt>

[<span data-ttu-id="f5db5-122">**Tag di**</span><span class="sxs-lookup"><span data-stu-id="f5db5-122">**SetTags**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)
</dt> </dl>

 

