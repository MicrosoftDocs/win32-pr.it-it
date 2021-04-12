---
title: Messaggio PSM_SETCURSEL (Prsht. h)
description: Attiva la pagina specificata in una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- Controlli di Windows Message PSM_SETCURSEL
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119575"
---
# <a name="psm_setcursel-message"></a><span data-ttu-id="cde0f-105">\_Messaggio di RImaledizione di PSM</span><span class="sxs-lookup"><span data-stu-id="cde0f-105">PSM\_SETCURSEL message</span></span>

<span data-ttu-id="cde0f-106">Attiva la pagina specificata in una finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="cde0f-106">Activates the specified page in a property sheet.</span></span> <span data-ttu-id="cde0f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .</span><span class="sxs-lookup"><span data-stu-id="cde0f-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cde0f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cde0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cde0f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cde0f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cde0f-110">Indice in base zero della pagina.</span><span class="sxs-lookup"><span data-stu-id="cde0f-110">The zero-based index of the page.</span></span> <span data-ttu-id="cde0f-111">Un'applicazione può specificare l'indice o l'handle o entrambi.</span><span class="sxs-lookup"><span data-stu-id="cde0f-111">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="cde0f-112">Se vengono specificati entrambi, *lParam* avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="cde0f-112">If both are specified, *lParam* takes precedence.</span></span>

</dd> <dt>

<span data-ttu-id="cde0f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cde0f-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cde0f-114">Handle della pagina da attivare.</span><span class="sxs-lookup"><span data-stu-id="cde0f-114">The handle to the page to activate.</span></span> <span data-ttu-id="cde0f-115">Un'applicazione può specificare l'indice o l'handle o entrambi.</span><span class="sxs-lookup"><span data-stu-id="cde0f-115">An application can specify the index or the handle or both.</span></span> <span data-ttu-id="cde0f-116">Se vengono specificati entrambi, *lParam* avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="cde0f-116">If both are specified, *lParam* takes precedence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cde0f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cde0f-117">Return value</span></span>

<span data-ttu-id="cde0f-118">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cde0f-118">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cde0f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="cde0f-119">Remarks</span></span>

<span data-ttu-id="cde0f-120">La finestra che sta per perdere l'attivazione riceve il codice di notifica [ \_ KILLACTIVE PSN](psn-killactive.md) e la finestra che sta ottenendo l'attivazione riceve il codice di notifica [ \_ seattivo PSN](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="cde0f-120">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cde0f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cde0f-121">Requirements</span></span>



| <span data-ttu-id="cde0f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cde0f-122">Requirement</span></span> | <span data-ttu-id="cde0f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="cde0f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cde0f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cde0f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cde0f-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cde0f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cde0f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cde0f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cde0f-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cde0f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cde0f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cde0f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cde0f-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="cde0f-129"><dt>Prsht.h</dt></span></span> </dl> |



 

 





