---
title: Messaggio DTM_GETSYSTEMTIME (COMmctrl. h)
description: Ottiene l'ora attualmente selezionata da un controllo di selezione data e ora (DTP) e la inserisce in una struttura SYSTEMTIME specificata. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetSystemtime.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- Controlli di Windows Message DTM_GETSYSTEMTIME
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120546"
---
# <a name="dtm_getsystemtime-message"></a><span data-ttu-id="163fe-105">\_Messaggio GETSYSTEMTIME DTM</span><span class="sxs-lookup"><span data-stu-id="163fe-105">DTM\_GETSYSTEMTIME message</span></span>

<span data-ttu-id="163fe-106">Ottiene l'ora attualmente selezionata da un controllo di selezione data e ora (DTP) e la inserisce in una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) specificata.</span><span class="sxs-lookup"><span data-stu-id="163fe-106">Gets the currently selected time from a date and time picker (DTP) control and places it in a specified [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="163fe-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) .</span><span class="sxs-lookup"><span data-stu-id="163fe-107">You can send this message explicitly or use the [**DateTime\_GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="163fe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="163fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="163fe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="163fe-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="163fe-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="163fe-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="163fe-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="163fe-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="163fe-112">Puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="163fe-112">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="163fe-113">Se **DTM \_ GETSYSTEMTIME** restituisce GDT \_ valido, questa struttura conterrà l'ora attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="163fe-113">If **DTM\_GETSYSTEMTIME** returns GDT\_VALID, this structure will contain the currently selected time.</span></span> <span data-ttu-id="163fe-114">In caso contrario, non conterrà informazioni valide.</span><span class="sxs-lookup"><span data-stu-id="163fe-114">Otherwise, it will not contain valid information.</span></span> <span data-ttu-id="163fe-115">Questo parametro deve essere un puntatore valido; non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="163fe-115">This parameter must be a valid pointer; it cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="163fe-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="163fe-116">Return value</span></span>

<span data-ttu-id="163fe-117">Restituisce GDT \_ valido se le informazioni sull'ora sono state inserite correttamente in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="163fe-117">Returns GDT\_VALID if the time information was successfully placed in *lParam*.</span></span> <span data-ttu-id="163fe-118">Restituisce GDT \_ None se il controllo è stato impostato sullo stile [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) e non è stata selezionata la casella di controllo Control.</span><span class="sxs-lookup"><span data-stu-id="163fe-118">Returns GDT\_NONE if the control was set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style and the control check box was not selected.</span></span> <span data-ttu-id="163fe-119">Restituisce \_ un errore GDT se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="163fe-119">Returns GDT\_ERROR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="163fe-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="163fe-120">Requirements</span></span>



| <span data-ttu-id="163fe-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="163fe-121">Requirement</span></span> | <span data-ttu-id="163fe-122">Valore</span><span class="sxs-lookup"><span data-stu-id="163fe-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="163fe-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="163fe-123">Minimum supported client</span></span><br/> | <span data-ttu-id="163fe-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="163fe-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="163fe-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="163fe-125">Minimum supported server</span></span><br/> | <span data-ttu-id="163fe-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="163fe-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="163fe-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="163fe-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="163fe-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="163fe-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

