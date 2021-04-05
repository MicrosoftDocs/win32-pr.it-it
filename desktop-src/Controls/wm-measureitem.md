---
title: Messaggio WM_MEASUREITEM (winuser. h)
description: Inviato alla finestra proprietaria di una casella combinata, una casella di riepilogo, un controllo visualizzazione elenco o una voce di menu quando viene creato il controllo o il menu.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- Controlli di Windows Message WM_MEASUREITEM
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874105"
---
# <a name="wm_measureitem-message"></a><span data-ttu-id="fed52-104">\_Messaggio MeasureItem WM</span><span class="sxs-lookup"><span data-stu-id="fed52-104">WM\_MEASUREITEM message</span></span>

<span data-ttu-id="fed52-105">Inviato alla finestra proprietaria di una casella combinata, una casella di riepilogo, un controllo visualizzazione elenco o una voce di menu quando viene creato il controllo o il menu.</span><span class="sxs-lookup"><span data-stu-id="fed52-105">Sent to the owner window of a combo box, list box, list-view control, or menu item when the control or menu is created.</span></span>

<span data-ttu-id="fed52-106">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fed52-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="fed52-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fed52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fed52-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fed52-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fed52-109">Contiene il valore del membro **CtlID** della struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta il parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="fed52-109">Contains the value of the **CtlID** member of the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter.</span></span> <span data-ttu-id="fed52-110">Questo valore identifica il controllo che ha inviato il messaggio **WM \_ MeasureItem** .</span><span class="sxs-lookup"><span data-stu-id="fed52-110">This value identifies the control that sent the **WM\_MEASUREITEM** message.</span></span> <span data-ttu-id="fed52-111">Se il valore è zero, il messaggio è stato inviato da un menu.</span><span class="sxs-lookup"><span data-stu-id="fed52-111">If the value is zero, the message was sent by a menu.</span></span> <span data-ttu-id="fed52-112">Se il valore è diverso da zero, il messaggio è stato inviato da una casella combinata o da una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="fed52-112">If the value is nonzero, the message was sent by a combo box or by a list box.</span></span> <span data-ttu-id="fed52-113">Se il valore è diverso da zero e il valore del membro **ItemId** di **MEASUREITEMSTRUCT** a cui punta *lParam* è (uint) 1, il messaggio è stato inviato da un campo di modifica combinata.</span><span class="sxs-lookup"><span data-stu-id="fed52-113">If the value is nonzero, and the value of the **itemID** member of the **MEASUREITEMSTRUCT** pointed to by *lParam* is (UINT)  1, the message was sent by a combo edit field.</span></span>

</dd> <dt>

<span data-ttu-id="fed52-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fed52-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fed52-115">Puntatore a una struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) che contiene le dimensioni del controllo creato dal proprietario o della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="fed52-115">Pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that contains the dimensions of the owner-drawn control or menu item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fed52-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fed52-116">Return value</span></span>

<span data-ttu-id="fed52-117">Se un'applicazione elabora il messaggio, deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="fed52-117">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fed52-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="fed52-118">Remarks</span></span>

<span data-ttu-id="fed52-119">Quando la finestra proprietaria riceve il messaggio **WM \_ MeasureItem** , il proprietario compila la struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta il parametro *lParam* del messaggio e restituisce; in questo modo si informa il sistema delle dimensioni del controllo.</span><span class="sxs-lookup"><span data-stu-id="fed52-119">When the owner window receives the **WM\_MEASUREITEM** message, the owner fills in the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure pointed to by the *lParam* parameter of the message and returns; this informs the system of the dimensions of the control.</span></span> <span data-ttu-id="fed52-120">Se viene creata una casella di riepilogo o una casella combinata con lo stile [**\_ OwnerDrawVariable**](list-box-styles.md) o [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) , questo messaggio viene inviato al proprietario per ogni elemento nel controllo. in caso contrario, il messaggio viene inviato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="fed52-120">If a list box or combo box is created with the [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style, this message is sent to the owner for each item in the control; otherwise, this message is sent once.</span></span>

<span data-ttu-id="fed52-121">Il sistema invia il messaggio **WM \_ MeasureItem** alla finestra proprietaria di caselle combinate e caselle di riepilogo create con lo stile OwnerDrawFixed prima di inviare il messaggio [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) .</span><span class="sxs-lookup"><span data-stu-id="fed52-121">The system sends the **WM\_MEASUREITEM** message to the owner window of combo boxes and list boxes created with the OWNERDRAWFIXED style before sending the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message.</span></span> <span data-ttu-id="fed52-122">Di conseguenza, quando il proprietario riceve questo messaggio, il sistema non ha ancora determinato l'altezza e la larghezza del tipo di carattere utilizzato nel controllo; le chiamate di funzione e i calcoli che richiedono questi valori devono verificarsi nella funzione principale dell'applicazione o della libreria.</span><span class="sxs-lookup"><span data-stu-id="fed52-122">As a result, when the owner receives this message, the system has not yet determined the height and width of the font used in the control; function calls and calculations requiring these values should occur in the main function of the application or library.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed52-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fed52-123">Requirements</span></span>



| <span data-ttu-id="fed52-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fed52-124">Requirement</span></span> | <span data-ttu-id="fed52-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fed52-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed52-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fed52-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fed52-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fed52-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fed52-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fed52-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fed52-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fed52-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fed52-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fed52-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fed52-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fed52-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fed52-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fed52-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="fed52-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fed52-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fed52-134">**MEASUREITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="fed52-134">**MEASUREITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

<span data-ttu-id="fed52-135">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="fed52-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="fed52-136">**\_INITDIALOG WM**</span><span class="sxs-lookup"><span data-stu-id="fed52-136">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

