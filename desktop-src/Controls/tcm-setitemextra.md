---
title: Messaggio TCM_SETITEMEXTRA (COMmctrl. h)
description: Imposta il numero di byte per tabulazione riservata ai dati definiti dall'applicazione in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- Controlli di Windows Message TCM_SETITEMEXTRA
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118962"
---
# <a name="tcm_setitemextra-message"></a><span data-ttu-id="9fdb0-105">\_Messaggio TCM SETITEMEXTRA</span><span class="sxs-lookup"><span data-stu-id="9fdb0-105">TCM\_SETITEMEXTRA message</span></span>

<span data-ttu-id="9fdb0-106">Imposta il numero di byte per tabulazione riservata ai dati definiti dall'applicazione in un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-106">Sets the number of bytes per tab reserved for application-defined data in a tab control.</span></span> <span data-ttu-id="9fdb0-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) .</span><span class="sxs-lookup"><span data-stu-id="9fdb0-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9fdb0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fdb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fdb0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9fdb0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fdb0-110">Numero di byte aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-110">Number of extra bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9fdb0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fdb0-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9fdb0-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fdb0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fdb0-113">Return value</span></span>

<span data-ttu-id="9fdb0-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fdb0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fdb0-115">Remarks</span></span>

<span data-ttu-id="9fdb0-116">Per impostazione predefinita, il numero di byte aggiuntivi è quattro.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-116">By default, the number of extra bytes is four.</span></span> <span data-ttu-id="9fdb0-117">Un'applicazione che modifica il numero di byte aggiuntivi non può utilizzare la struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) per recuperare e impostare i dati definiti dall'applicazione per una scheda. È invece necessario definire una nuova struttura costituita dalla struttura [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) seguita da membri definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-117">An application that changes the number of extra bytes cannot use the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure to retrieve and set the application-defined data for a tab. Instead, you must define a new structure that consists of the [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) structure followed by application-defined members.</span></span>

<span data-ttu-id="9fdb0-118">Un'applicazione deve modificare solo il numero di byte aggiuntivi quando un controllo struttura a schede non contiene alcuna tabulazione.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-118">An application should only change the number of extra bytes when a tab control does not contain any tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fdb0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fdb0-119">Requirements</span></span>



| <span data-ttu-id="9fdb0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fdb0-120">Requirement</span></span> | <span data-ttu-id="9fdb0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9fdb0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fdb0-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fdb0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9fdb0-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fdb0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9fdb0-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fdb0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9fdb0-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9fdb0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9fdb0-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fdb0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fdb0-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fdb0-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





