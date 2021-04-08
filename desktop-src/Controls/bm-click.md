---
title: Messaggio BM_CLICK (winuser. h)
description: Simula l'utente che fa clic su un pulsante. Questo messaggio fa in modo che il pulsante riceva i \_ messaggi WM LBUTTONDOWN e WM \_ LBUTTONUP e la finestra padre del pulsante per ricevere un \_ codice di notifica fatto clic su BN.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- Controlli di Windows Message BM_CLICK
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048070"
---
# <a name="bm_click-message"></a><span data-ttu-id="75f6b-105">\_Messaggio di clic BM</span><span class="sxs-lookup"><span data-stu-id="75f6b-105">BM\_CLICK message</span></span>

<span data-ttu-id="75f6b-106">Simula l'utente che fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="75f6b-106">Simulates the user clicking a button.</span></span> <span data-ttu-id="75f6b-107">Questo messaggio fa in modo che il pulsante riceva i messaggi [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) e [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) e la finestra padre del pulsante per ricevere un codice di notifica [ \_ fatto clic su BN](bn-clicked.md) .</span><span class="sxs-lookup"><span data-stu-id="75f6b-107">This message causes the button to receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) and [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages, and the button's parent window to receive a [BN\_CLICKED](bn-clicked.md) notification code.</span></span>

## <a name="parameters"></a><span data-ttu-id="75f6b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="75f6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75f6b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75f6b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75f6b-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="75f6b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="75f6b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75f6b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75f6b-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="75f6b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75f6b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75f6b-113">Return value</span></span>

<span data-ttu-id="75f6b-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="75f6b-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75f6b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="75f6b-115">Remarks</span></span>

<span data-ttu-id="75f6b-116">Se il pulsante si trova in una finestra di dialogo e la finestra di dialogo non è attiva, il messaggio di **\_ clic BM** potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="75f6b-116">If the button is in a dialog box and the dialog box is not active, the **BM\_CLICK** message might fail.</span></span> <span data-ttu-id="75f6b-117">Per garantire l'esito positivo della situazione, chiamare la funzione [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) per attivare la finestra di dialogo prima di inviare il messaggio di **\_ clic BM** al pulsante.</span><span class="sxs-lookup"><span data-stu-id="75f6b-117">To ensure success in this situation, call the [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) function to activate the dialog box before sending the **BM\_CLICK** message to the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="75f6b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75f6b-118">Requirements</span></span>



| <span data-ttu-id="75f6b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="75f6b-119">Requirement</span></span> | <span data-ttu-id="75f6b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="75f6b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75f6b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75f6b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="75f6b-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75f6b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="75f6b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75f6b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="75f6b-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="75f6b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="75f6b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75f6b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="75f6b-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75f6b-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

