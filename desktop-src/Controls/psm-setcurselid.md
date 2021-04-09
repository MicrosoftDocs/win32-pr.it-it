---
title: Messaggio PSM_SETCURSELID (Prsht. h)
description: Attiva la pagina specificata in una finestra delle proprietà in base all'identificatore di risorsa della pagina. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet SetCurSelByID.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- Controlli di Windows Message PSM_SETCURSELID
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120707"
---
# <a name="psm_setcurselid-message"></a><span data-ttu-id="4d13d-105">\_Messaggio SETCURSELID di PSM</span><span class="sxs-lookup"><span data-stu-id="4d13d-105">PSM\_SETCURSELID message</span></span>

<span data-ttu-id="4d13d-106">Attiva la pagina specificata in una finestra delle proprietà in base all'identificatore di risorsa della pagina.</span><span class="sxs-lookup"><span data-stu-id="4d13d-106">Activates the given page in a property sheet based on the resource identifier of the page.</span></span> <span data-ttu-id="4d13d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .</span><span class="sxs-lookup"><span data-stu-id="4d13d-107">You can send this message explicitly or by using the [**PropSheet\_SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d13d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d13d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d13d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d13d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d13d-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4d13d-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4d13d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d13d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d13d-112">Identificatore di risorsa della pagina da attivare.</span><span class="sxs-lookup"><span data-stu-id="4d13d-112">Resource identifier of the page to activate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d13d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d13d-113">Return value</span></span>

<span data-ttu-id="4d13d-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4d13d-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d13d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d13d-115">Remarks</span></span>

<span data-ttu-id="4d13d-116">La finestra che sta per perdere l'attivazione riceve il codice di notifica [ \_ KILLACTIVE PSN](psn-killactive.md) e la finestra che sta ottenendo l'attivazione riceve il codice di notifica [ \_ seattivo PSN](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="4d13d-116">The window that is losing the activation receives the [PSN\_KILLACTIVE](psn-killactive.md) notification code, and the window that is gaining the activation receives the [PSN\_SETACTIVE](psn-setactive.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d13d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d13d-117">Requirements</span></span>



| <span data-ttu-id="4d13d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d13d-118">Requirement</span></span> | <span data-ttu-id="4d13d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4d13d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4d13d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d13d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4d13d-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d13d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4d13d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d13d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4d13d-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d13d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4d13d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d13d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d13d-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d13d-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





