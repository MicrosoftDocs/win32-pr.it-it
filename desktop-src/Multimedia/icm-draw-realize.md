---
title: Messaggio di ICM_DRAW_REALIZE (VFW. h)
description: Il \_ messaggio ICM Draw \_ réalisateur informa un driver di rendering di realizzare la relativa tavolozza di disegno durante il disegno. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawRealize.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- ICM_DRAW_REALIZE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400538"
---
# <a name="icm_draw_realize-message"></a><span data-ttu-id="dadfa-105">Messaggio di realizzazione di un \_ progetto ICM \_</span><span class="sxs-lookup"><span data-stu-id="dadfa-105">ICM\_DRAW\_REALIZE message</span></span>

<span data-ttu-id="dadfa-106">Il messaggio **ICM \_ Draw \_ réalisateur** informa un driver di rendering di realizzare la relativa tavolozza di disegno durante il disegno.</span><span class="sxs-lookup"><span data-stu-id="dadfa-106">The **ICM\_DRAW\_REALIZE** message notifies a rendering driver to realize its drawing palette while drawing.</span></span> <span data-ttu-id="dadfa-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) .</span><span class="sxs-lookup"><span data-stu-id="dadfa-107">You can send this message explicitly or by using the [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) macro.</span></span>


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a><span data-ttu-id="dadfa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dadfa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dadfa-109"><span id="hdc"></span><span id="HDC"></span>*HDC*</span><span class="sxs-lookup"><span data-stu-id="dadfa-109"><span id="hdc"></span><span id="HDC"></span>*hdc*</span></span>
</dt> <dd>

<span data-ttu-id="dadfa-110">Handle per il controller di dominio utilizzato per realizzare la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="dadfa-110">Handle to the DC used to realize the palette.</span></span>

</dd> <dt>

<span data-ttu-id="dadfa-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span><span class="sxs-lookup"><span data-stu-id="dadfa-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span></span>
</dt> <dd>

<span data-ttu-id="dadfa-112">Flag di sfondo.</span><span class="sxs-lookup"><span data-stu-id="dadfa-112">Background flag.</span></span> <span data-ttu-id="dadfa-113">Specificare **true** per realizzare la tavolozza come attività in background o **false** per realizzare la tavolozza in primo piano.</span><span class="sxs-lookup"><span data-stu-id="dadfa-113">Specify **TRUE** to realize the palette as a background task or **FALSE** to realize the palette in the foreground.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dadfa-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dadfa-114">Return Value</span></span>

<span data-ttu-id="dadfa-115">Restituisce ICERR \_ OK se la tavolozza di disegno è realizzata o ICERR non \_ supportata se la tavolozza associata ai dati decompressi viene realizzata.</span><span class="sxs-lookup"><span data-stu-id="dadfa-115">Returns ICERR\_OK if the drawing palette is realized or ICERR\_UNSUPPORTED if the palette associated with the decompressed data is realized.</span></span>

## <a name="remarks"></a><span data-ttu-id="dadfa-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="dadfa-116">Remarks</span></span>

<span data-ttu-id="dadfa-117">I driver devono rispondere a questo messaggio solo se la tavolozza di disegno è diversa dalla tavolozza decompressa.</span><span class="sxs-lookup"><span data-stu-id="dadfa-117">Drivers need to respond to this message only if the drawing palette is different from the decompressed palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="dadfa-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dadfa-118">Requirements</span></span>



| <span data-ttu-id="dadfa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dadfa-119">Requirement</span></span> | <span data-ttu-id="dadfa-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dadfa-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dadfa-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dadfa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dadfa-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dadfa-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dadfa-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dadfa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dadfa-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dadfa-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dadfa-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dadfa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dadfa-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="dadfa-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dadfa-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dadfa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dadfa-128">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="dadfa-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="dadfa-129">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="dadfa-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





