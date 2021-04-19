---
description: Codici di stato che possono essere restituiti dalle funzioni DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322513"
---
# <a name="dxgi_status"></a><span data-ttu-id="76119-103">\_stato DXGI</span><span class="sxs-lookup"><span data-stu-id="76119-103">DXGI\_STATUS</span></span>

<span data-ttu-id="76119-104">Codici di stato che possono essere restituiti dalle funzioni DXGI.</span><span class="sxs-lookup"><span data-stu-id="76119-104">Status codes that can be returned by DXGI functions.</span></span>



| <span data-ttu-id="76119-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="76119-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="76119-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76119-106">Description</span></span>                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <span data-ttu-id="76119-107"><dt>**DXGI \_ STATO \_**</dt> bloccato <dt>0x087A0001</dt></span><span class="sxs-lookup"><span data-stu-id="76119-107"><dt>**DXGI\_STATUS\_OCCLUDED**</dt> <dt>0x087A0001</dt></span></span> </dl>                                                 | <span data-ttu-id="76119-108">Il contenuto della finestra non è visibile.</span><span class="sxs-lookup"><span data-stu-id="76119-108">The window content is not visible.</span></span> <span data-ttu-id="76119-109">Quando si riceve questo stato, un'applicazione può arrestare il rendering e utilizzare il \_ \_ test di DXGI presente per determinare quando riprendere il rendering.</span><span class="sxs-lookup"><span data-stu-id="76119-109">When receiving this status, an application can stop rendering and use DXGI\_PRESENT\_TEST to determine when to resume rendering.</span></span> <span data-ttu-id="76119-110">\_ \_ Se si usa una catena di scambio Flip Model, non verrà visualizzato lo stato dxgi.</span><span class="sxs-lookup"><span data-stu-id="76119-110">You will not receive DXGI\_STATUS\_OCCLUDED if you're using a flip model swap chain.</span></span><br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <span data-ttu-id="76119-111"><dt>**DXGI \_ Modalità di stato \_ \_ modificata**</dt> <dt>0x087A0007</dt></span><span class="sxs-lookup"><span data-stu-id="76119-111"><dt>**DXGI\_STATUS\_MODE\_CHANGED**</dt> <dt>0x087A0007</dt></span></span> </dl>                                    | <span data-ttu-id="76119-112">La modalità di visualizzazione del desktop è stata modificata. è possibile che si verifichino la conversione o l'allungamento dei colori.</span><span class="sxs-lookup"><span data-stu-id="76119-112">The desktop display mode has been changed, there might be color conversion/stretching.</span></span> <span data-ttu-id="76119-113">L'applicazione deve chiamare [**IDXGISwapChain:: ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) per trovare la corrispondenza con la nuova modalità di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="76119-113">The application should call [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) to match the new display mode.</span></span><br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <span data-ttu-id="76119-114"><dt>**DXGI \_ \_ \_ Modifica della modalità \_ di stato in \_ corso**</dt> <dt>0x087A0008</dt></span><span class="sxs-lookup"><span data-stu-id="76119-114"><dt>**DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</dt> <dt>0x087A0008</dt></span></span> </dl> | <span data-ttu-id="76119-115">[**IDXGISwapChain:: ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) e [**IDXGISwapChain:: SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) restituiranno \_ \_ \_ una modifica della modalità \_ di stato DXGI in \_ corso se si verifica una transizione in modalità a schermo intero/con finestra quando viene chiamata una delle API.</span><span class="sxs-lookup"><span data-stu-id="76119-115">[**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) and [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) will return DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS if a fullscreen/windowed mode transition is occurring when either API is called.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="76119-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="76119-116">Remarks</span></span>

<span data-ttu-id="76119-117">Il valore **HRESULT** per ogni valore di **\_ stato DXGI** è determinato da questa macro definita in DXGItype. h:</span><span class="sxs-lookup"><span data-stu-id="76119-117">The **HRESULT** value for each **DXGI\_STATUS** value is determined from this macro that is defined in DXGItype.h:</span></span>


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



<span data-ttu-id="76119-118">**\_ Lo stato DXGI \_** , ad esempio, viene definito come **0x087A0001**:</span><span class="sxs-lookup"><span data-stu-id="76119-118">For example, **DXGI\_STATUS\_OCCLUDED** is defined as **0x087A0001**:</span></span>


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a><span data-ttu-id="76119-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76119-119">Requirements</span></span>



| <span data-ttu-id="76119-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="76119-120">Requirement</span></span> | <span data-ttu-id="76119-121">Valore</span><span class="sxs-lookup"><span data-stu-id="76119-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="76119-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76119-122">Header</span></span><br/> | <dl> <span data-ttu-id="76119-123"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="76119-123"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76119-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76119-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76119-125">Costanti DXGI</span><span class="sxs-lookup"><span data-stu-id="76119-125">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




