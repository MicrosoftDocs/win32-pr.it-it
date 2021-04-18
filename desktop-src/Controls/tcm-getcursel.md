---
title: Messaggio TCM_GETCURSEL (COMmctrl. h)
description: Determina la scheda attualmente selezionata in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TabCtrl GetCurSel.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- Controlli di Windows Message TCM_GETCURSEL
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302365"
---
# <a name="tcm_getcursel-message"></a><span data-ttu-id="ff581-105">TCM- \_ messaggio GETcursel</span><span class="sxs-lookup"><span data-stu-id="ff581-105">TCM\_GETCURSEL message</span></span>

<span data-ttu-id="ff581-106">Determina la scheda attualmente selezionata in un controllo struttura a schede.</span><span class="sxs-lookup"><span data-stu-id="ff581-106">Determines the currently selected tab in a tab control.</span></span> <span data-ttu-id="ff581-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="ff581-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff581-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff581-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff581-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff581-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ff581-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ff581-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ff581-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff581-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ff581-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ff581-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff581-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff581-113">Return value</span></span>

<span data-ttu-id="ff581-114">Restituisce l'indice della scheda selezionata in caso di esito positivo, oppure-1 se non è selezionata alcuna scheda.</span><span class="sxs-lookup"><span data-stu-id="ff581-114">Returns the index of the selected tab if successful, or -1 if no tab is selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff581-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff581-115">Requirements</span></span>



| <span data-ttu-id="ff581-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff581-116">Requirement</span></span> | <span data-ttu-id="ff581-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ff581-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ff581-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff581-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ff581-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff581-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ff581-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff581-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ff581-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ff581-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ff581-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff581-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff581-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff581-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





