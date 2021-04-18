---
title: Metodi CreateHwndRenderTarget di ID2D1Factory (D2d1. h)
description: Crea un ID2D1HwndRenderTarget, una destinazione di rendering che esegue il rendering in una finestra.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Metodo CreateHwndRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329880"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a><span data-ttu-id="1a89b-104">Metodi ID2D1Factory:: CreateHwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="1a89b-104">ID2D1Factory::CreateHwndRenderTarget methods</span></span>

<span data-ttu-id="1a89b-105">Crea un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), una destinazione di rendering che esegue il rendering in una finestra.</span><span class="sxs-lookup"><span data-stu-id="1a89b-105">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span>

### <a name="overload-list"></a><span data-ttu-id="1a89b-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="1a89b-106">Overload list</span></span>



| <span data-ttu-id="1a89b-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="1a89b-107">Method</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="1a89b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a89b-108">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a89b-109">[**CreateHwndRenderTarget ( \_ \_ proprietà destinazione rendering \_ d2d1 \* , \_ \_ proprietà destinazione rendering HWND d2d1 \_ \_ \* , ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a89b-109">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES\*,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES\*,ID2D1HwndRenderTarget\*\*)**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span> | <span data-ttu-id="1a89b-110">Crea un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), una destinazione di rendering che esegue il rendering in una finestra.</span><span class="sxs-lookup"><span data-stu-id="1a89b-110">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |
| <span data-ttu-id="1a89b-111">[**CreateHwndRenderTarget ( \_ \_ proprietà destinazione rendering d2d1 \_&, \_ proprietà di \_ destinazione rendering HWND d2d1 \_ \_&, ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span><span class="sxs-lookup"><span data-stu-id="1a89b-111">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES&,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES&,ID2D1HwndRenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span></span>   | <span data-ttu-id="1a89b-112">Crea un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), una destinazione di rendering che esegue il rendering in una finestra.</span><span class="sxs-lookup"><span data-stu-id="1a89b-112">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1a89b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a89b-113">Remarks</span></span>

<span data-ttu-id="1a89b-114">Quando si crea una destinazione di rendering e l'accelerazione hardware è disponibile, è necessario allocare risorse sulla GPU del computer.</span><span class="sxs-lookup"><span data-stu-id="1a89b-114">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="1a89b-115">Creando una destinazione di rendering una volta e mantenendola il più a lungo possibile, si ottengono vantaggi in termini di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="1a89b-115">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="1a89b-116">L'applicazione deve creare le destinazioni di rendering una volta e mantenerle per la durata dell'applicazione o fino a quando non viene ricevuto l'errore di [**\_ \_ destinazione D2DERR ricreate**](direct2d-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1a89b-116">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="1a89b-117">Quando si riceve questo errore, è necessario ricreare la destinazione di rendering (e tutte le risorse create).</span><span class="sxs-lookup"><span data-stu-id="1a89b-117">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="examples"></a><span data-ttu-id="1a89b-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="1a89b-118">Examples</span></span>

<span data-ttu-id="1a89b-119">Nell'esempio seguente viene creato un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1a89b-119">The following example creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



## <a name="requirements"></a><span data-ttu-id="1a89b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a89b-120">Requirements</span></span>



| <span data-ttu-id="1a89b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a89b-121">Requirement</span></span> | <span data-ttu-id="1a89b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1a89b-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1a89b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a89b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1a89b-124"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a89b-124"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a89b-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="1a89b-125">Library</span></span><br/> | <dl> <span data-ttu-id="1a89b-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a89b-126"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a89b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1a89b-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a89b-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a89b-128"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a89b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a89b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a89b-130">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="1a89b-130">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
