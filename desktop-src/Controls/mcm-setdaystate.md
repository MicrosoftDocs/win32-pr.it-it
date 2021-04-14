---
title: Messaggio MCM_SETDAYSTATE (COMmctrl. h)
description: Imposta gli Stati del giorno per tutti i mesi attualmente visibili all'interno di un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal SetDayState.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- Controlli di Windows Message MCM_SETDAYSTATE
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478958"
---
# <a name="mcm_setdaystate-message"></a><span data-ttu-id="e8345-105">\_Messaggio SETDAYSTATE MCM</span><span class="sxs-lookup"><span data-stu-id="e8345-105">MCM\_SETDAYSTATE message</span></span>

<span data-ttu-id="e8345-106">Imposta gli Stati del giorno per tutti i mesi attualmente visibili all'interno di un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="e8345-106">Sets the day states for all months that are currently visible within a month calendar control.</span></span> <span data-ttu-id="e8345-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) .</span><span class="sxs-lookup"><span data-stu-id="e8345-107">You can send this message explicitly or by using the [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e8345-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8345-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8345-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8345-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8345-110">Valore che indica il numero di elementi nella matrice a cui fa riferimento *lParam* .</span><span class="sxs-lookup"><span data-stu-id="e8345-110">Value indicating how many elements are in the array that *lParam* points to.</span></span>

</dd> <dt>

<span data-ttu-id="e8345-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8345-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8345-112">Puntatore a una matrice di valori [**MONTHDAYSTATE**](monthdaystate.md) che definiscono il modo in cui il controllo calendario mensile trarrà ogni giorno nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e8345-112">Pointer to an array of [**MONTHDAYSTATE**](monthdaystate.md) values that define how the month calendar control will draw each day in its display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8345-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8345-113">Return value</span></span>

<span data-ttu-id="e8345-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e8345-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8345-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8345-115">Remarks</span></span>

<span data-ttu-id="e8345-116">Un'applicazione può impostare in modo esplicito le informazioni sullo stato del giorno inviando questo messaggio, ma lo stato non verrà mantenuto quando una parte diversa del calendario viene visualizzata nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e8345-116">An application can explicitly set day state information by sending this message, but the state will not persist when a different part of the calendar is scrolled into view.</span></span> <span data-ttu-id="e8345-117">Le informazioni sullo stato del giorno vengono in genere impostate in risposta al codice di notifica [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , che viene inviato ogni volta che è necessario aggiornare il controllo.</span><span class="sxs-lookup"><span data-stu-id="e8345-117">Day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed.</span></span>

<span data-ttu-id="e8345-118">La matrice in *lParam* deve contenere tutti gli elementi del valore restituito dalla seguente macro:</span><span class="sxs-lookup"><span data-stu-id="e8345-118">The array at *lParam* must contain as many elements as the value returned by the following macro:</span></span>

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

<span data-ttu-id="e8345-119">Tenere presente che la matrice in *lParam* deve contenere valori [**MONTHDAYSTATE**](monthdaystate.md) che corrispondono a tutti i mesi attualmente presenti nella visualizzazione del controllo, in ordine cronologico.</span><span class="sxs-lookup"><span data-stu-id="e8345-119">Keep in mind that the array at *lParam* must contain [**MONTHDAYSTATE**](monthdaystate.md) values that correspond with all months currently in the control's display, in chronological order.</span></span> <span data-ttu-id="e8345-120">Sono inclusi i due mesi che possono essere visualizzati parzialmente prima del primo mese e dopo l'ultimo mese.</span><span class="sxs-lookup"><span data-stu-id="e8345-120">This includes the two months that may be partially displayed before the first month and after the last month.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8345-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8345-121">Requirements</span></span>



| <span data-ttu-id="e8345-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8345-122">Requirement</span></span> | <span data-ttu-id="e8345-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e8345-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8345-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8345-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e8345-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8345-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e8345-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8345-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e8345-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8345-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8345-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8345-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8345-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8345-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8345-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8345-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8345-131">Utilizzo di controlli calendario mensile</span><span class="sxs-lookup"><span data-stu-id="e8345-131">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 





