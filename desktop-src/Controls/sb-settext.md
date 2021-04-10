---
title: Messaggio SB_SETTEXT (COMmctrl. h)
description: Imposta il testo nella parte specificata di una finestra di stato.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- Controlli di Windows Message SB_SETTEXT
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120695"
---
# <a name="sb_settext-message"></a><span data-ttu-id="ee785-104">\_Messaggio di testo SB</span><span class="sxs-lookup"><span data-stu-id="ee785-104">SB\_SETTEXT message</span></span>

<span data-ttu-id="ee785-105">Imposta il testo nella parte specificata di una finestra di stato.</span><span class="sxs-lookup"><span data-stu-id="ee785-105">Sets the text in the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee785-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee785-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee785-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee785-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee785-108">Il [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) della parola di ordine inferiore specifica l'indice in base zero della parte da impostare.</span><span class="sxs-lookup"><span data-stu-id="ee785-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the low-order word specifies the zero-based index of the part to set.</span></span> <span data-ttu-id="ee785-109">Se **LOBYTE** è impostato su SB \_ SIMPLEID, si presuppone che la finestra di stato sia una barra di stato in modalità semplice, ovvero una barra di stato con una sola parte.</span><span class="sxs-lookup"><span data-stu-id="ee785-109">If the **LOBYTE** is set to SB\_SIMPLEID, the status window is assumed to be a simple mode status bar; that is, a status bar with only one part.</span></span>

<span data-ttu-id="ee785-110">Il [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) della parola di ordine inferiore specifica il tipo di operazione di disegno.</span><span class="sxs-lookup"><span data-stu-id="ee785-110">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the low-order word specifies the type of the drawing operation.</span></span> <span data-ttu-id="ee785-111">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ee785-111">This parameter can be one of the following values.</span></span>

<span data-ttu-id="ee785-112">La parola più ordinata di *wParam* viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="ee785-112">The high-order word of *wParam* is ignored.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee785-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ee785-113">Value</span></span></th>
<th><span data-ttu-id="ee785-114">Significato</span><span class="sxs-lookup"><span data-stu-id="ee785-114">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <span data-ttu-id="ee785-115"><dt><strong>0</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ee785-115"><dt><strong>0</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="ee785-116">Il testo viene disegnato con un bordo da visualizzare in basso rispetto al piano della finestra.</span><span class="sxs-lookup"><span data-stu-id="ee785-116">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <span data-ttu-id="ee785-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ee785-117"><dt><strong>SBT_NOBORDERS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="ee785-118">Il testo viene disegnato senza bordi.</span><span class="sxs-lookup"><span data-stu-id="ee785-118">The text is drawn without borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <span data-ttu-id="ee785-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ee785-119"><dt><strong>SBT_OWNERDRAW</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="ee785-120">Il testo viene disegnato dalla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="ee785-120">The text is drawn by the parent window.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ee785-121">Una barra di stato in modalità semplice non supporta il disegno del proprietario.</span><span class="sxs-lookup"><span data-stu-id="ee785-121">A simple mode status bar does not support owner drawing.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <span data-ttu-id="ee785-122"><dt><strong>SBT_POPOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ee785-122"><dt><strong>SBT_POPOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="ee785-123">Il testo viene disegnato con un bordo da visualizzare più in alto rispetto al piano della finestra.</span><span class="sxs-lookup"><span data-stu-id="ee785-123">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <span data-ttu-id="ee785-124"><dt><strong>SBT_RTLREADING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ee785-124"><dt><strong>SBT_RTLREADING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="ee785-125">Il testo verrà visualizzato nella direzione opposta al testo nella finestra padre.</span><span class="sxs-lookup"><span data-stu-id="ee785-125">The text will be displayed in the opposite direction to the text in the parent window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <span data-ttu-id="ee785-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="ee785-126"><dt><strong>SBT_NOTABPARSING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="ee785-127">I caratteri di tabulazione vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="ee785-127">Tab characters are ignored.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="ee785-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee785-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee785-129">Puntatore a una stringa con terminazione null che specifica il testo da impostare.</span><span class="sxs-lookup"><span data-stu-id="ee785-129">Pointer to a null-terminated string that specifies the text to set.</span></span> <span data-ttu-id="ee785-130">Se *wParam* è SBT \_ OWNERDRAW, questo parametro rappresenta 32 bit di dati.</span><span class="sxs-lookup"><span data-stu-id="ee785-130">If *wParam* is SBT\_OWNERDRAW, this parameter represents 32 bits of data.</span></span> <span data-ttu-id="ee785-131">La finestra padre deve interpretare i dati e creare il testo quando riceve il messaggio [**WM \_ DrawItem**](wm-drawitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ee785-131">The parent window must interpret the data and draw the text when it receives the [**WM\_DRAWITEM**](wm-drawitem.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee785-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee785-132">Return value</span></span>

<span data-ttu-id="ee785-133">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ee785-133">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee785-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee785-134">Remarks</span></span>

<span data-ttu-id="ee785-135">Il messaggio invalida la parte della finestra che è stata modificata, causando la visualizzazione del nuovo testo quando la finestra successiva riceve il messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) .</span><span class="sxs-lookup"><span data-stu-id="ee785-135">The message invalidates the portion of the window that has changed, causing it to display the new text when the window next receives the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="ee785-136">Normale testo visualizzato da sinistra a destra (LTR).</span><span class="sxs-lookup"><span data-stu-id="ee785-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="ee785-137">È possibile eseguire il *mirroring* di Windows per visualizzare lingue quali l'ebraico o l'arabo con lettura da destra a sinistra (RTL).</span><span class="sxs-lookup"><span data-stu-id="ee785-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="ee785-138">Se \_ si imposta SBT RTLREADING, la stringa *lParam* verrà letta nella direzione opposta dal testo nella finestra padre.</span><span class="sxs-lookup"><span data-stu-id="ee785-138">If SBT\_RTLREADING is set, the *lParam* string will read in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee785-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee785-139">Requirements</span></span>



| <span data-ttu-id="ee785-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee785-140">Requirement</span></span> | <span data-ttu-id="ee785-141">Valore</span><span class="sxs-lookup"><span data-stu-id="ee785-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee785-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee785-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ee785-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee785-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee785-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee785-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ee785-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ee785-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ee785-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee785-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee785-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee785-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ee785-148">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ee785-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ee785-149">**SB \_ SETTEXTW** (Unicode) e **SB \_ setexta** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ee785-149">**SB\_SETTEXTW** (Unicode) and **SB\_SETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="ee785-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee785-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee785-151">**SB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="ee785-151">**SB\_GETTEXT**</span></span>](sb-gettext.md)
</dt> </dl>

 

