---
title: Messaggio LB_SETTABSTOPS (winuser. h)
description: Imposta le posizioni di interruzione di tabulazione in una casella di riepilogo.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- Controlli di Windows Message LB_SETTABSTOPS
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874333"
---
# <a name="lb_settabstops-message"></a><span data-ttu-id="4d5f9-104">\_Messaggio SETTABSTOPS lb</span><span class="sxs-lookup"><span data-stu-id="4d5f9-104">LB\_SETTABSTOPS message</span></span>

<span data-ttu-id="4d5f9-105">Imposta le posizioni di interruzione di tabulazione in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-105">Sets the tab-stop positions in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d5f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d5f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d5f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d5f9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d5f9-108">Specifica il numero di arresti tabulari.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-108">Specifies the number of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="4d5f9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d5f9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d5f9-110">Puntatore al primo membro di una matrice di numeri interi contenenti le tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-110">Pointer to the first member of an array of integers containing the tab stops.</span></span> <span data-ttu-id="4d5f9-111">I numeri interi rappresentano il numero di trimestri della larghezza media dei caratteri per il tipo di carattere selezionato nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-111">The integers represent the number of quarters of the average character width for the font that is selected into the list box.</span></span> <span data-ttu-id="4d5f9-112">Ad esempio, una tabulazione di 4 viene posizionata a 1,0 unità di caratteri e una tabulazione di 6 viene posizionata a 1,5 unità di caratteri medie.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-112">For example, a tab stop of 4 is placed at 1.0 character units, and a tab stop of 6 is placed at 1.5 average character units.</span></span> <span data-ttu-id="4d5f9-113">Tuttavia, se la casella di riepilogo fa parte di una finestra di dialogo, i numeri interi si trovano in unità modello di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-113">However, if the list box is part of a dialog box, the integers are in dialog template units.</span></span> <span data-ttu-id="4d5f9-114">Le tabulazioni devono essere ordinate in ordine crescente. le schede con le versioni precedenti non sono consentite.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-114">The tab stops must be sorted in ascending order; backward tabs are not allowed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d5f9-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d5f9-115">Return value</span></span>

<span data-ttu-id="4d5f9-116">Se tutte le schede specificate sono impostate, il valore restituito è **true**; in caso contrario, è **false**.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-116">If all the specified tabs are set, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d5f9-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d5f9-117">Remarks</span></span>

<span data-ttu-id="4d5f9-118">Per rispondere al messaggio **lb \_ SETTABSTOPS** , è necessario che la casella di riepilogo sia stata creata con lo stile [**\_ USETABSTOPS lbs**](list-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4d5f9-118">To respond to the **LB\_SETTABSTOPS** message, the list box must have been created with the [**LBS\_USETABSTOPS**](list-box-styles.md) style.</span></span>

<span data-ttu-id="4d5f9-119">Se *wParam* è 0 e *lParam* è **null**, la tabulazione predefinita è due unità modello di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-119">If *wParam* is 0 and *lParam* is **NULL**, the default tab stop is two dialog template units.</span></span> <span data-ttu-id="4d5f9-120">Se *wParam* è 1, la casella di riepilogo disporrà di tabulazioni separate dalla distanza specificata da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-120">If *wParam* is 1, the list box will have tab stops separated by the distance specified by *lParam*.</span></span>

<span data-ttu-id="4d5f9-121">Se *lParam* punta a più di un valore singolo, viene impostata una tabulazione per ogni valore in *lParam*, fino al numero specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-121">If *lParam* points to more than a single value, a tab stop will be set for each value in *lParam*, up to the number specified by *wParam*.</span></span>

<span data-ttu-id="4d5f9-122">I valori specificati da *lParam* si trovano nelle unità dei modelli di finestra di dialogo, ovvero le unità indipendenti dal dispositivo utilizzate nei modelli di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-122">The values specified by *lParam* are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="4d5f9-123">Per convertire le misurazioni dalle unità del modello di finestra di dialogo alle unità dello schermo (pixel), usare la funzione [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="4d5f9-123">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="4d5f9-124">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il buffer a cui punta *lParam* deve risiedere nella memoria scrivibile, anche se il messaggio non modifica la matrice.</span><span class="sxs-lookup"><span data-stu-id="4d5f9-124">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The buffer pointed to by *lParam* must reside in writable memory, even though the message does not modify the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d5f9-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d5f9-125">Requirements</span></span>



| <span data-ttu-id="4d5f9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d5f9-126">Requirement</span></span> | <span data-ttu-id="4d5f9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4d5f9-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d5f9-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d5f9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4d5f9-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d5f9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4d5f9-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d5f9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4d5f9-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d5f9-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4d5f9-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d5f9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d5f9-133"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d5f9-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d5f9-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d5f9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d5f9-135">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="4d5f9-135">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

