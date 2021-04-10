---
description: Inviato quando un utente esegue un gesto di penna. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: Messaggio WM_TABLET_FLICK (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c95598ac23f37918c67eec70c2ed205f8a4fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226046"
---
# <a name="wm_tablet_flick-message"></a><span data-ttu-id="05479-104">\_Messaggio di \_ scorrimento rapido del Tablet WM</span><span class="sxs-lookup"><span data-stu-id="05479-104">WM\_TABLET\_FLICK message</span></span>

<span data-ttu-id="05479-105">Inviato quando un utente esegue un gesto di penna.</span><span class="sxs-lookup"><span data-stu-id="05479-105">Sent when a user performs a pen flick.</span></span> <span data-ttu-id="05479-106">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="05479-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a><span data-ttu-id="05479-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="05479-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05479-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05479-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05479-109">Una [**\_ struttura di dati di scorrimento**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) che contiene informazioni sul Flick della penna che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="05479-109">A [**FLICK\_DATA Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) that contains information about the pen flick that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="05479-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05479-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05479-111">[**Struttura del \_ punto di scorrimento**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) che specifica la posizione in cui si è verificato il tocco di penna.</span><span class="sxs-lookup"><span data-stu-id="05479-111">The [**FLICK\_POINT Structure**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) that specifies where the pen flick occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="05479-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="05479-112">Remarks</span></span>

<span data-ttu-id="05479-113">Un gesto rapido con penna è un movimento di penna unidirezionale che richiede all'utente di contattare il digitalizzatore in un movimento rapido e semplice.</span><span class="sxs-lookup"><span data-stu-id="05479-113">A pen flick is a unidirectional pen gesture that requires the user to contact the digitizer in a quick, straight flicking motion.</span></span> <span data-ttu-id="05479-114">Un gesto rapido è caratterizzato da alta velocità e da un elevato grado di unidritità.</span><span class="sxs-lookup"><span data-stu-id="05479-114">A flick is characterized by high speed and a high degree of straightness.</span></span> <span data-ttu-id="05479-115">Un gesto rapido viene identificato in base alla direzione.</span><span class="sxs-lookup"><span data-stu-id="05479-115">A flick is identified by its direction.</span></span> <span data-ttu-id="05479-116">I gesti rapidi possono essere eseguiti in otto direzioni corrispondenti alle direzioni Cardinal e secondaria della bussola.</span><span class="sxs-lookup"><span data-stu-id="05479-116">Flicks can be made in eight directions corresponding to the cardinal and secondary compass directions.</span></span>

<span data-ttu-id="05479-117">Quando si verifica un gesto rapido penna, Windows invia prima di tutto una notifica a un'applicazione inviando un messaggio di **\_ \_ scorrimento rapido del Tablet WM** , che una finestra riceve tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="05479-117">When a pen flick occurs, Windows first notifies an application by sending a **WM\_TABLET\_FLICK** message, which a window receives through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="05479-118">Restituisce la **costante \_ \_ \_ maschera gestita WM di scorrimento** , descritta in [costanti rapide](flicks-constants.md), per indicare che l'applicazione ha risposto al messaggio di **\_ \_ scorrimento rapido del Tablet WM** .</span><span class="sxs-lookup"><span data-stu-id="05479-118">Return the **FLICK\_WM\_HANDLED\_MASK** constant, described in [Flicks Constants](flicks-constants.md), to indicate that the application responded to the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="05479-119">Se l'applicazione non restituisce la **\_ \_ \_ maschera gestita di Flick WM**, Windows esegue l'azione predefinita specificata nel pannello di controllo Flicks inviando una notifica di completamento, ad esempio [**WM \_ APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM \_ VSCROLL**](../controls/wm-vscroll.md)o [**WM \_ KeyDown**](../inputdev/wm-keydown.md), a seconda dell'azione associata al gesto rapido della penna.</span><span class="sxs-lookup"><span data-stu-id="05479-119">If the application does not return **FLICK\_WM\_HANDLED\_MASK**, Windows performs the default action specified in the flicks control panel by sending a follow-up notification, such as [**WM\_APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM\_VSCROLL**](../controls/wm-vscroll.md), or [**WM\_KEYDOWN**](../inputdev/wm-keydown.md), depending on which action is associated with the pen flick.</span></span>

<span data-ttu-id="05479-120">Prestare attenzione quando si gestisce il messaggio di **\_ \_ scorrimento rapido del Tablet WM** .</span><span class="sxs-lookup"><span data-stu-id="05479-120">Use caution when handling the **WM\_TABLET\_FLICK** message.</span></span> <span data-ttu-id="05479-121">**WM \_ Il TABLET \_ Flick** viene passato tramite la funzione [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="05479-121">**WM\_TABLET\_FLICK** is passed via the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="05479-122">Se si chiamano metodi su un'interfaccia COM, tale oggetto deve trovarsi all'interno dello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="05479-122">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="05479-123">In caso contrario, COM genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="05479-123">If not, COM throws an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="05479-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05479-124">Requirements</span></span>



| <span data-ttu-id="05479-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="05479-125">Requirement</span></span> | <span data-ttu-id="05479-126">Valore</span><span class="sxs-lookup"><span data-stu-id="05479-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="05479-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05479-127">Minimum supported client</span></span><br/> | <span data-ttu-id="05479-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05479-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="05479-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05479-129">Minimum supported server</span></span><br/> | <span data-ttu-id="05479-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05479-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="05479-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05479-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="05479-132"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="05479-132"><dt>Tpcshrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05479-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05479-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05479-134">**Scorri la \_ struttura dei dati**</span><span class="sxs-lookup"><span data-stu-id="05479-134">**flick\_data structure**</span></span>](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[<span data-ttu-id="05479-135">**\_messaggio di \_ scorrimento rapido del Tablet WM**</span><span class="sxs-lookup"><span data-stu-id="05479-135">**wm\_tablet\_flick message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="05479-136">movimenti rapidi</span><span class="sxs-lookup"><span data-stu-id="05479-136">flicks gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="05479-137">[risposta ai gesti rapidi della penna](/previous-versions/windows/desktop/ms703447(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="05479-137">[responding to pen flicks](/previous-versions/windows/desktop/ms703447(v=vs.85))</span></span>
</dt> </dl>

 

 
