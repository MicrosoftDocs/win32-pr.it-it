---
title: Messaggio MCM_GETMINREQRECT (COMmctrl. h)
description: Recupera le dimensioni minime necessarie per visualizzare un mese intero in un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetMinReqRect.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- Controlli di Windows Message MCM_GETMINREQRECT
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476072"
---
# <a name="mcm_getminreqrect-message"></a><span data-ttu-id="e5a3d-105">\_Messaggio GETMINREQRECT MCM</span><span class="sxs-lookup"><span data-stu-id="e5a3d-105">MCM\_GETMINREQRECT message</span></span>

<span data-ttu-id="e5a3d-106">Recupera le dimensioni minime necessarie per visualizzare un mese intero in un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-106">Retrieves the minimum size required to display a full month in a month calendar control.</span></span> <span data-ttu-id="e5a3d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) .</span><span class="sxs-lookup"><span data-stu-id="e5a3d-107">You can send this message explicitly or by using the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5a3d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5a3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5a3d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5a3d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e5a3d-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e5a3d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5a3d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5a3d-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceverà informazioni sul rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive bounding rectangle information.</span></span> <span data-ttu-id="e5a3d-113">Questo parametro deve essere un indirizzo valido e non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5a3d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5a3d-114">Return value</span></span>

<span data-ttu-id="e5a3d-115">Restituisce un valore diverso da zero e *lParam* riceve le informazioni di delimitazione applicabili in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-115">Returns nonzero and *lParam* receives the applicable bounding information if successful.</span></span> <span data-ttu-id="e5a3d-116">In caso contrario, il messaggio restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5a3d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5a3d-117">Remarks</span></span>

<span data-ttu-id="e5a3d-118">Le dimensioni minime della finestra richiesta per un controllo di calendario mensile dipendono dal tipo di carattere correntemente selezionato, dagli stili dei controlli, dalle metriche di sistema e dalle impostazioni internazionali.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-118">The minimum required window size for a month calendar control depends on the currently selected font, control styles, system metrics, and regional settings.</span></span> <span data-ttu-id="e5a3d-119">Quando un'applicazione modifica qualsiasi elemento che influisca sulle dimensioni minime della finestra o elabora un messaggio [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) , deve inviare **MCM \_ GETMINREQRECT** per determinare le nuove dimensioni minime.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-119">When an application changes anything that affects the minimum window size, or processes a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message, it should send **MCM\_GETMINREQRECT** to determine the new minimum size.</span></span>

> [!Note]  
> <span data-ttu-id="e5a3d-120">Il rettangolo restituito da **MCM \_ GETMINREQRECT** non include la larghezza della stringa "Today", se presente.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-120">The rectangle returned by **MCM\_GETMINREQRECT** does not include the width of the "Today" string, if it is present.</span></span> <span data-ttu-id="e5a3d-121">Se lo [**stile \_ notoday MCS**](month-calendar-control-styles.md) non è impostato, l'applicazione deve recuperare anche il rettangolo che definisce la larghezza della stringa "Today" inviando un messaggio [**MCM \_ GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a3d-121">If the [**MCS\_NOTODAY**](month-calendar-control-styles.md) style is not set, your application should also retrieve the rectangle that defines the "Today" string width by sending a [**MCM\_GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) message.</span></span> <span data-ttu-id="e5a3d-122">Usare il più grande dei due rettangoli per assicurarsi che la stringa "Today" non venga troncata.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-122">Use the larger of the two rectangles to ensure that the "Today" string is not clipped.</span></span>

 

<span data-ttu-id="e5a3d-123">I membri **superiore** e **sinistro** della struttura a cui punta *lParam* saranno sempre zero.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-123">The **top** and **left** members of the structure pointed to by *lParam* will always be zero.</span></span> <span data-ttu-id="e5a3d-124">I membri **destro** e **inferiore** rappresentano il valore minimo *CX* e *CY* necessari per il controllo.</span><span class="sxs-lookup"><span data-stu-id="e5a3d-124">The **right** and **bottom** members represent the minimum *cx* and *cy* required for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a3d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5a3d-125">Requirements</span></span>



| <span data-ttu-id="e5a3d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5a3d-126">Requirement</span></span> | <span data-ttu-id="e5a3d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e5a3d-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a3d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5a3d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a3d-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5a3d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e5a3d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5a3d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a3d-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e5a3d-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5a3d-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5a3d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5a3d-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5a3d-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

