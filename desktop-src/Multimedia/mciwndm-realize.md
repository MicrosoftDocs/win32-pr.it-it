---
title: Messaggio di MCIWNDM_REALIZE (VFW. h)
description: Il \_ messaggio MCIWNDM realizza la tavolozza attualmente usata dal dispositivo MCI in una finestra di MCIWnd. Questa macro viene definita con il \_ messaggio MCIWNDM realizz. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndRealize.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- MCIWNDM_REALIZE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963825"
---
# <a name="mciwndm_realize-message"></a><span data-ttu-id="5cb9f-106">MCIWNDM \_ realizzare un messaggio</span><span class="sxs-lookup"><span data-stu-id="5cb9f-106">MCIWNDM\_REALIZE message</span></span>

<span data-ttu-id="5cb9f-107">Il messaggio **MCIWNDM \_ realizza** la tavolozza attualmente usata dal dispositivo MCI in una finestra di MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-107">The **MCIWNDM\_REALIZE** message realizes the palette currently used by the MCI device in an MCIWnd window.</span></span> <span data-ttu-id="5cb9f-108">Questa macro viene definita con il messaggio **MCIWNDM \_ realizz** .</span><span class="sxs-lookup"><span data-stu-id="5cb9f-108">This macro is defined with the **MCIWNDM\_REALIZE** message.</span></span> <span data-ttu-id="5cb9f-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .</span><span class="sxs-lookup"><span data-stu-id="5cb9f-109">You can send this message explicitly or by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span>


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="5cb9f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cb9f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cb9f-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span><span class="sxs-lookup"><span data-stu-id="5cb9f-111"><span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*</span></span>
</dt> <dd>

<span data-ttu-id="5cb9f-112">Flag di sfondo.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-112">Background flag.</span></span> <span data-ttu-id="5cb9f-113">Specificare **true** per questo parametro se la finestra è un'applicazione in background.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-113">Specify **TRUE** for this parameter if the window is a background application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cb9f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cb9f-114">Return Value</span></span>

<span data-ttu-id="5cb9f-115">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-115">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cb9f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cb9f-116">Remarks</span></span>

<span data-ttu-id="5cb9f-117">**MCIWNDM \_ REALIZZARE** usa la tavolozza del dispositivo MCI e chiama la funzione [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) .</span><span class="sxs-lookup"><span data-stu-id="5cb9f-117">**MCIWNDM\_REALIZE** uses the palette of the MCI device and calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function.</span></span> <span data-ttu-id="5cb9f-118">Se l'applicazione gestisce in modo esplicito i messaggi [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) e [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) , è necessario usare questo messaggio nell'applicazione invece di usare **RealizePalette**.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-118">If your application explicitly handles the [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) messages, you should use this message in your application instead of using **RealizePalette**.</span></span> <span data-ttu-id="5cb9f-119">Se il corpo di uno di questi gestori di messaggi contiene solo **RealizePalette**, il messaggio viene trasmesso alla finestra MCIWnd, che rende automaticamente disponibile la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="5cb9f-119">If the body of one of these message handlers contains only **RealizePalette**, forward the message to the MCIWnd window, which will automatically realize the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cb9f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cb9f-120">Requirements</span></span>



| <span data-ttu-id="5cb9f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cb9f-121">Requirement</span></span> | <span data-ttu-id="5cb9f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="5cb9f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5cb9f-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cb9f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5cb9f-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5cb9f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5cb9f-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cb9f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5cb9f-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5cb9f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5cb9f-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cb9f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cb9f-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cb9f-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cb9f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cb9f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb9f-130">**MCIWndRealize**</span><span class="sxs-lookup"><span data-stu-id="5cb9f-130">**MCIWndRealize**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[<span data-ttu-id="5cb9f-131">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="5cb9f-131">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="5cb9f-132">**\_PALETTECHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="5cb9f-132">**WM\_PALETTECHANGED**</span></span>](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[<span data-ttu-id="5cb9f-133">**\_QUERYNEWPALETTE WM**</span><span class="sxs-lookup"><span data-stu-id="5cb9f-133">**WM\_QUERYNEWPALETTE**</span></span>](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

