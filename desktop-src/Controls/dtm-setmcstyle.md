---
title: Messaggio DTM_SETMCSTYLE (COMmctrl. h)
description: Imposta lo stile di un controllo di selezione data e ora (DTP). Inviare questo messaggio in modo esplicito o utilizzando la \_ macro DateTime SetMonthCalStyle.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- Controlli di Windows Message DTM_SETMCSTYLE
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120543"
---
# <a name="dtm_setmcstyle-message"></a><span data-ttu-id="81e54-105">\_Messaggio SETMCSTYLE DTM</span><span class="sxs-lookup"><span data-stu-id="81e54-105">DTM\_SETMCSTYLE message</span></span>

<span data-ttu-id="81e54-106">Imposta lo stile di un controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="81e54-106">Sets the style of a date and time picker (DTP) control.</span></span> <span data-ttu-id="81e54-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .</span><span class="sxs-lookup"><span data-stu-id="81e54-107">Send this message explicitly or by using the [**DateTime\_SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="81e54-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="81e54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81e54-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81e54-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81e54-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="81e54-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="81e54-111">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81e54-111">*lParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="81e54-112">Valore di stile.</span><span class="sxs-lookup"><span data-stu-id="81e54-112">A style value.</span></span> <span data-ttu-id="81e54-113">Per altre informazioni, vedere <a href="month-calendar-control-styles.md">stili del controllo calendario mensile</a>.</span><span class="sxs-lookup"><span data-stu-id="81e54-113">For more information see <a href="month-calendar-control-styles.md">Month Calendar Control Styles</a>.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81e54-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81e54-114">Return value</span></span>

<span data-ttu-id="81e54-115">Restituisce il valore dello stile precedente.</span><span class="sxs-lookup"><span data-stu-id="81e54-115">Returns the value of the previous style.</span></span>

## <a name="requirements"></a><span data-ttu-id="81e54-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81e54-116">Requirements</span></span>



| <span data-ttu-id="81e54-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81e54-117">Requirement</span></span> | <span data-ttu-id="81e54-118">Valore</span><span class="sxs-lookup"><span data-stu-id="81e54-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81e54-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81e54-119">Minimum supported client</span></span><br/> | <span data-ttu-id="81e54-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81e54-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81e54-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81e54-121">Minimum supported server</span></span><br/> | <span data-ttu-id="81e54-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81e54-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81e54-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81e54-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="81e54-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="81e54-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





