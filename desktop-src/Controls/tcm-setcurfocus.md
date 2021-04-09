---
title: Messaggio TCM_SETCURFOCUS (COMmctrl. h)
description: Imposta lo stato attivo su una scheda specificata in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl SetCurFocus.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- Controlli di Windows Message TCM_SETCURFOCUS
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964249"
---
# <a name="tcm_setcurfocus-message"></a><span data-ttu-id="400b9-105">\_Messaggio TCM SETCURFOCUS</span><span class="sxs-lookup"><span data-stu-id="400b9-105">TCM\_SETCURFOCUS message</span></span>

<span data-ttu-id="400b9-106">Imposta lo stato attivo su una scheda specificata in un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="400b9-106">Sets the focus to a specified tab in a tab control.</span></span> <span data-ttu-id="400b9-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) .</span><span class="sxs-lookup"><span data-stu-id="400b9-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="400b9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="400b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="400b9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="400b9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="400b9-110">Indice della scheda che ottiene lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="400b9-110">Index of the tab that gets the focus.</span></span>

</dd> <dt>

<span data-ttu-id="400b9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="400b9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="400b9-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="400b9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="400b9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="400b9-113">Return value</span></span>

<span data-ttu-id="400b9-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="400b9-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="400b9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="400b9-115">Remarks</span></span>

<span data-ttu-id="400b9-116">Se il controllo struttura a schede ha lo stile dei [**\_ pulsanti TCS**](tab-control-styles.md) (modalità pulsante), la scheda con lo stato attivo potrebbe essere diversa dalla scheda selezionata. Ad esempio, quando si seleziona una scheda, l'utente può premere i tasti di direzione per impostare lo stato attivo su una scheda diversa senza modificare la scheda selezionata. In modalità pulsante, **TCM \_ SETCURFOCUS** imposta lo stato attivo per l'input sul pulsante associato alla scheda specificata, ma non modifica la scheda selezionata.</span><span class="sxs-lookup"><span data-stu-id="400b9-116">If the tab control has the [**TCS\_BUTTONS**](tab-control-styles.md) style (button mode), the tab with the focus may be different from the selected tab. For example, when a tab is selected, the user can press the arrow keys to set the focus to a different tab without changing the selected tab. In button mode, **TCM\_SETCURFOCUS** sets the input focus to the button associated with the specified tab, but it does not change the selected tab.</span></span>

<span data-ttu-id="400b9-117">Se il controllo struttura a schede non ha lo stile dei [**\_ pulsanti TCS**](tab-control-styles.md) , la modifica dello stato attivo cambia anche la scheda selezionata. In questo caso, il controllo struttura a schede invia i codici di notifica [TCN \_ SELCHANGING](tcn-selchanging.md) e [TCN \_ selChange](tcn-selchange.md) alla relativa finestra padre.</span><span class="sxs-lookup"><span data-stu-id="400b9-117">If the tab control does not have the [**TCS\_BUTTONS**](tab-control-styles.md) style, changing the focus also changes the selected tab. In this case, the tab control sends the [TCN\_SELCHANGING](tcn-selchanging.md) and [TCN\_SELCHANGE](tcn-selchange.md) notification codes to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="400b9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="400b9-118">Requirements</span></span>



| <span data-ttu-id="400b9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="400b9-119">Requirement</span></span> | <span data-ttu-id="400b9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="400b9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="400b9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="400b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="400b9-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="400b9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="400b9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="400b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="400b9-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="400b9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="400b9-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="400b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="400b9-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="400b9-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="400b9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="400b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="400b9-128">**TCM \_ GETCURFOCUS**</span><span class="sxs-lookup"><span data-stu-id="400b9-128">**TCM\_GETCURFOCUS**</span></span>](tcm-getcurfocus.md)
</dt> </dl>

 

 





