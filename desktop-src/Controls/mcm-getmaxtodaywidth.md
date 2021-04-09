---
title: Messaggio MCM_GETMAXTODAYWIDTH (COMmctrl. h)
description: Recupera la larghezza massima di \ 0034; Today \ 0034; stringa in un controllo di calendario mensile. Sono inclusi il testo dell'etichetta e il testo della data. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetMaxTodayWidth.
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- Controlli di Windows Message MCM_GETMAXTODAYWIDTH
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741818"
---
# <a name="mcm_getmaxtodaywidth-message"></a><span data-ttu-id="09bf7-106">\_Messaggio GETMAXTODAYWIDTH MCM</span><span class="sxs-lookup"><span data-stu-id="09bf7-106">MCM\_GETMAXTODAYWIDTH message</span></span>

<span data-ttu-id="09bf7-107">Recupera la larghezza massima della stringa "Today" in un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="09bf7-107">Retrieves the maximum width of the "today" string in a month calendar control.</span></span> <span data-ttu-id="09bf7-108">Sono inclusi il testo dell'etichetta e il testo della data.</span><span class="sxs-lookup"><span data-stu-id="09bf7-108">This includes the label text and the date text.</span></span> <span data-ttu-id="09bf7-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) .</span><span class="sxs-lookup"><span data-stu-id="09bf7-109">You can send this message explicitly or by using the [**MonthCal\_GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="09bf7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="09bf7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09bf7-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="09bf7-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="09bf7-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="09bf7-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="09bf7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="09bf7-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="09bf7-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="09bf7-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09bf7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09bf7-115">Return value</span></span>

<span data-ttu-id="09bf7-116">Restituisce la larghezza, in pixel, della stringa "Today".</span><span class="sxs-lookup"><span data-stu-id="09bf7-116">Returns the width of the "today" string, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="09bf7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09bf7-117">Requirements</span></span>



| <span data-ttu-id="09bf7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="09bf7-118">Requirement</span></span> | <span data-ttu-id="09bf7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="09bf7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09bf7-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09bf7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="09bf7-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09bf7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="09bf7-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09bf7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="09bf7-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="09bf7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09bf7-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="09bf7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="09bf7-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09bf7-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





