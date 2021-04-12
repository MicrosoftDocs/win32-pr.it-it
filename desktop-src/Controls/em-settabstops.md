---
title: Messaggio EM_SETTABSTOPS (winuser. h)
description: Il \_ messaggio SETTABSTOPS em imposta la tabulazione in un controllo di modifica su più righe.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- Controlli di Windows Message EM_SETTABSTOPS
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120126"
---
# <a name="em_settabstops-message"></a><span data-ttu-id="2ea7c-104">\_Messaggio SETTABSTOPS em</span><span class="sxs-lookup"><span data-stu-id="2ea7c-104">EM\_SETTABSTOPS message</span></span>

<span data-ttu-id="2ea7c-105">Il **messaggio \_ SETTABSTOPS em** imposta la tabulazione in un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-105">The **EM\_SETTABSTOPS** message sets the tab stops in a multiline edit control.</span></span> <span data-ttu-id="2ea7c-106">Quando il testo viene copiato nel controllo, qualsiasi carattere di tabulazione nel testo causa la generazione dello spazio fino alla tabulazione successiva.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-106">When text is copied to the control, any tab character in the text causes space to be generated up to the next tab stop.</span></span>

<span data-ttu-id="2ea7c-107">Questo messaggio viene elaborato solo dai controlli di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-107">This message is processed only by multiline edit controls.</span></span> <span data-ttu-id="2ea7c-108">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-108">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ea7c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ea7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ea7c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ea7c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ea7c-111">Numero di arresti di tabulazione contenuti nella matrice.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-111">The number of tab stops contained in the array.</span></span> <span data-ttu-id="2ea7c-112">Se questo parametro è zero, il parametro *lParam* viene ignorato e le tabulazioni predefinite vengono impostate in ogni unità del modello di finestra di dialogo 32.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-112">If this parameter is zero, the *lParam* parameter is ignored and default tab stops are set at every 32 dialog template units.</span></span> <span data-ttu-id="2ea7c-113">Se questo parametro è 1, le tabulazioni vengono impostate in ogni *n* unità modello di finestra di dialogo, dove *n* è la distanza a cui punta il parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="2ea7c-113">If this parameter is 1, tab stops are set at every *n* dialog template units, where *n* is the distance pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="2ea7c-114">Se questo parametro è maggiore di 1, *lParam* è un puntatore a una matrice di tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-114">If this parameter is greater than 1, *lParam* is a pointer to an array of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="2ea7c-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ea7c-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ea7c-116">Puntatore a una matrice di interi senza segno che specifica le tabulazioni, nelle unità del modello di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-116">A pointer to an array of unsigned integers specifying the tab stops, in dialog template units.</span></span> <span data-ttu-id="2ea7c-117">Se il parametro *wParam* è 1, questo parametro è un puntatore a un Unsigned Integer che contiene la distanza tra tutti i punti di tabulazione, nelle unità del modello di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-117">If the *wParam* parameter is 1, this parameter is a pointer to an unsigned integer containing the distance between all tab stops, in dialog template units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ea7c-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ea7c-118">Return value</span></span>

<span data-ttu-id="2ea7c-119">Se tutte le schede sono impostate, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-119">If all the tabs are set, the return value is **TRUE**.</span></span>

<span data-ttu-id="2ea7c-120">Se tutte le schede non sono impostate, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-120">If all the tabs are not set, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ea7c-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ea7c-121">Remarks</span></span>

<span data-ttu-id="2ea7c-122">Il **messaggio \_ SETTABSTOPS em** non ridisegnato automaticamente la finestra di controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-122">The **EM\_SETTABSTOPS** message does not automatically redraw the edit control window.</span></span> <span data-ttu-id="2ea7c-123">Se l'applicazione sta cambiando la tabulazione per il testo già presente nel controllo di modifica, deve chiamare la funzione [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) per ricreare la finestra di controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-123">If the application is changing the tab stops for text already in the edit control, it should call the [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function to redraw the edit control window.</span></span>

<span data-ttu-id="2ea7c-124">I valori specificati nella matrice si trovano nelle unità dei modelli di finestra di dialogo, ovvero le unità indipendenti dal dispositivo utilizzate nei modelli di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-124">The values specified in the array are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="2ea7c-125">Per convertire le misurazioni dalle unità del modello di finestra di dialogo alle unità dello schermo (pixel), usare la funzione [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="2ea7c-125">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="2ea7c-126">**Modifica avanzata:** Supportato in Microsoft Rich Edit 3,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-126">**Rich Edit:** Supported in Microsoft Rich Edit 3.0 and later.</span></span> <span data-ttu-id="2ea7c-127">Un controllo Rich Edit può includere il numero massimo di interruzioni di tabulazioni specificato da MAX \_ Tab \_ stops.</span><span class="sxs-lookup"><span data-stu-id="2ea7c-127">A rich edit control can have the maximum number of tab stops specified by MAX\_TAB\_STOPS.</span></span> <span data-ttu-id="2ea7c-128">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="2ea7c-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ea7c-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ea7c-129">Requirements</span></span>



| <span data-ttu-id="2ea7c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ea7c-130">Requirement</span></span> | <span data-ttu-id="2ea7c-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2ea7c-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ea7c-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ea7c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2ea7c-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ea7c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2ea7c-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ea7c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2ea7c-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ea7c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2ea7c-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ea7c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ea7c-137"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ea7c-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ea7c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ea7c-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ea7c-139">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="2ea7c-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2ea7c-140">**InvalidateRect**</span><span class="sxs-lookup"><span data-stu-id="2ea7c-140">**InvalidateRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[<span data-ttu-id="2ea7c-141">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="2ea7c-141">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

