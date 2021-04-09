---
title: Messaggio TCM_SETCURSEL (COMmctrl. h)
description: Seleziona una scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl.
ms.assetid: cf709d8c-c522-47c8-8ff3-463dc8e924b5
keywords:
- Controlli di Windows Message TCM_SETCURSEL
topic_type:
- apiref
api_name:
- TCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90033c5a19b0eb7b73f9ed886e8dad8d1ca4c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964248"
---
# <a name="tcm_setcursel-message"></a><span data-ttu-id="d1da4-105">\_Messaggio di DEcursel TCM</span><span class="sxs-lookup"><span data-stu-id="d1da4-105">TCM\_SETCURSEL message</span></span>

<span data-ttu-id="d1da4-106">Seleziona una scheda in un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="d1da4-106">Selects a tab in a tab control.</span></span> <span data-ttu-id="d1da4-107">È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="d1da4-107">You can send this message explicitly or by using the [**TabCtrl\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1da4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1da4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1da4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1da4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1da4-110">Indice della scheda da selezionare.</span><span class="sxs-lookup"><span data-stu-id="d1da4-110">Index of the tab to select.</span></span>

</dd> <dt>

<span data-ttu-id="d1da4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1da4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d1da4-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d1da4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1da4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1da4-113">Return value</span></span>

<span data-ttu-id="d1da4-114">Restituisce l'indice della scheda selezionata in precedenza, se ha esito positivo, oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d1da4-114">Returns the index of the previously selected tab if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1da4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1da4-115">Remarks</span></span>

<span data-ttu-id="d1da4-116">Un controllo struttura a schede non invia un codice di notifica [TCN \_ SELCHANGING](tcn-selchanging.md) o [TCN \_ selChange](tcn-selchange.md) quando viene selezionata una scheda utilizzando questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="d1da4-116">A tab control does not send a [TCN\_SELCHANGING](tcn-selchanging.md) or [TCN\_SELCHANGE](tcn-selchange.md) notification code when a tab is selected using this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1da4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1da4-117">Requirements</span></span>



| <span data-ttu-id="d1da4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1da4-118">Requirement</span></span> | <span data-ttu-id="d1da4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d1da4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1da4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1da4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d1da4-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1da4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1da4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1da4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d1da4-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d1da4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1da4-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1da4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1da4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1da4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





