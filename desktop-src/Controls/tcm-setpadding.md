---
title: Messaggio TCM_SETPADDING (COMmctrl. h)
description: Imposta la quantità di spazio (riempimento) intorno all'icona e all'etichetta di ogni scheda in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl sepadding.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- Controlli di Windows Message TCM_SETPADDING
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300967"
---
# <a name="tcm_setpadding-message"></a><span data-ttu-id="f92fc-105">\_Messaggio di SEPADDING TCM</span><span class="sxs-lookup"><span data-stu-id="f92fc-105">TCM\_SETPADDING message</span></span>

<span data-ttu-id="f92fc-106">Imposta la quantità di spazio (riempimento) intorno all'icona e all'etichetta di ogni scheda in un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="f92fc-106">Sets the amount of space (padding) around each tab's icon and label in a tab control.</span></span> <span data-ttu-id="f92fc-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ sepadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) .</span><span class="sxs-lookup"><span data-stu-id="f92fc-107">You can send this message explicitly or by using the [**TabCtrl\_SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f92fc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f92fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f92fc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f92fc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f92fc-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **int** che specifica la quantità di spaziatura interna orizzontale, in pixel.</span><span class="sxs-lookup"><span data-stu-id="f92fc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the amount of horizontal padding, in pixels.</span></span> <span data-ttu-id="f92fc-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un valore **int** che specifica la quantità di spaziatura interna verticale, in pixel.</span><span class="sxs-lookup"><span data-stu-id="f92fc-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the amount of vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f92fc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f92fc-112">Return value</span></span>

<span data-ttu-id="f92fc-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="f92fc-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f92fc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f92fc-114">Requirements</span></span>



| <span data-ttu-id="f92fc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f92fc-115">Requirement</span></span> | <span data-ttu-id="f92fc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f92fc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f92fc-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f92fc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f92fc-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f92fc-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f92fc-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f92fc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f92fc-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f92fc-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f92fc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f92fc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f92fc-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f92fc-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

