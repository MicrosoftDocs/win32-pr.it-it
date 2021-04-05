---
description: Inviato a una finestra che l'utente sta ridimensionando. Elaborando questo messaggio, un'applicazione può monitorare le dimensioni e la posizione del rettangolo di trascinamento e, se necessario, modificarne le dimensioni o la posizione.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: Messaggio WM_SIZING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756632"
---
# <a name="wm_sizing-message"></a><span data-ttu-id="ad197-104">\_Messaggio di ridimensionamento WM</span><span class="sxs-lookup"><span data-stu-id="ad197-104">WM\_SIZING message</span></span>

<span data-ttu-id="ad197-105">Inviato a una finestra che l'utente sta ridimensionando.</span><span class="sxs-lookup"><span data-stu-id="ad197-105">Sent to a window that the user is resizing.</span></span> <span data-ttu-id="ad197-106">Elaborando questo messaggio, un'applicazione può monitorare le dimensioni e la posizione del rettangolo di trascinamento e, se necessario, modificarne le dimensioni o la posizione.</span><span class="sxs-lookup"><span data-stu-id="ad197-106">By processing this message, an application can monitor the size and position of the drag rectangle and, if needed, change its size or position.</span></span>

<span data-ttu-id="ad197-107">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ad197-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a><span data-ttu-id="ad197-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad197-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad197-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad197-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad197-110">Bordo della finestra da ridimensionare.</span><span class="sxs-lookup"><span data-stu-id="ad197-110">The edge of the window that is being sized.</span></span> <span data-ttu-id="ad197-111">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad197-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ad197-112">Valore</span><span class="sxs-lookup"><span data-stu-id="ad197-112">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="ad197-113">Significato</span><span class="sxs-lookup"><span data-stu-id="ad197-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <span data-ttu-id="ad197-114"><dt>**WMSZ \_ ULTIMI**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ad197-114"><dt>**WMSZ\_BOTTOM**</dt> <dt>6</dt></span></span> </dl>                | <span data-ttu-id="ad197-115">Bordo inferiore</span><span class="sxs-lookup"><span data-stu-id="ad197-115">Bottom edge</span></span><br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <span data-ttu-id="ad197-116"><dt>**WMSZ \_ BOTTOMLEFT**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ad197-116"><dt>**WMSZ\_BOTTOMLEFT**</dt> <dt>7</dt></span></span> </dl>    | <span data-ttu-id="ad197-117">Angolo inferiore sinistro</span><span class="sxs-lookup"><span data-stu-id="ad197-117">Bottom-left corner</span></span><br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <span data-ttu-id="ad197-118"><dt>**WMSZ \_ BOTTOMRIGHT**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="ad197-118"><dt>**WMSZ\_BOTTOMRIGHT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="ad197-119">Angolo inferiore destro</span><span class="sxs-lookup"><span data-stu-id="ad197-119">Bottom-right corner</span></span><br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <span data-ttu-id="ad197-120"><dt>**WMSZ \_ A sinistra**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ad197-120"><dt>**WMSZ\_LEFT**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="ad197-121">Bordo sinistro</span><span class="sxs-lookup"><span data-stu-id="ad197-121">Left edge</span></span><br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <span data-ttu-id="ad197-122"><dt>**WMSZ \_ DIRITTO**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ad197-122"><dt>**WMSZ\_RIGHT**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="ad197-123">Bordo destro</span><span class="sxs-lookup"><span data-stu-id="ad197-123">Right edge</span></span><br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <span data-ttu-id="ad197-124"><dt>**WMSZ \_ PRIMI**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ad197-124"><dt>**WMSZ\_TOP**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="ad197-125">Bordo superiore</span><span class="sxs-lookup"><span data-stu-id="ad197-125">Top edge</span></span><br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <span data-ttu-id="ad197-126"><dt>**WMSZ \_ In uscita**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ad197-126"><dt>**WMSZ\_TOPLEFT**</dt> <dt>4</dt></span></span> </dl>             | <span data-ttu-id="ad197-127">Angolo superiore sinistro</span><span class="sxs-lookup"><span data-stu-id="ad197-127">Top-left corner</span></span><br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <span data-ttu-id="ad197-128"><dt>**WMSZ \_ In destra**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ad197-128"><dt>**WMSZ\_TOPRIGHT**</dt> <dt>5</dt></span></span> </dl>          | <span data-ttu-id="ad197-129">Angolo superiore destro</span><span class="sxs-lookup"><span data-stu-id="ad197-129">Top-right corner</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="ad197-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad197-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad197-131">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) con le coordinate dello schermo del rettangolo di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="ad197-131">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the screen coordinates of the drag rectangle.</span></span> <span data-ttu-id="ad197-132">Per modificare le dimensioni o la posizione del rettangolo di trascinamento, un'applicazione deve modificare i membri di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="ad197-132">To change the size or position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad197-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad197-133">Return value</span></span>

<span data-ttu-id="ad197-134">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="ad197-134">Type: **LRESULT**</span></span>

<span data-ttu-id="ad197-135">Un'applicazione deve restituire **true** se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="ad197-135">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad197-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad197-136">Requirements</span></span>



| <span data-ttu-id="ad197-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad197-137">Requirement</span></span> | <span data-ttu-id="ad197-138">Valore</span><span class="sxs-lookup"><span data-stu-id="ad197-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad197-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad197-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ad197-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad197-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ad197-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad197-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ad197-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad197-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad197-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad197-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad197-144"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad197-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad197-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad197-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad197-146">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ad197-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad197-147">**\_trasferimento WM**</span><span class="sxs-lookup"><span data-stu-id="ad197-147">**WM\_MOVING**</span></span>](wm-moving.md)
</dt> <dt>

[<span data-ttu-id="ad197-148">**\_dimensioni WM**</span><span class="sxs-lookup"><span data-stu-id="ad197-148">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

<span data-ttu-id="ad197-149">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="ad197-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ad197-150">Windows</span><span class="sxs-lookup"><span data-stu-id="ad197-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="ad197-151">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="ad197-151">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="ad197-152">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad197-152">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
