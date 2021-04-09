---
title: Messaggio TDM_SET_MARQUEE_PROGRESS_BAR (COMmctrl. h)
description: Indica se l'indicatore di stato ospitato di una finestra di dialogo attività deve essere visualizzato in modalità marquee.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- Controlli di Windows Message TDM_SET_MARQUEE_PROGRESS_BAR
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121298"
---
# <a name="tdm_set_marquee_progress_bar-message"></a><span data-ttu-id="c16e0-104">Messaggio indicatore indicatore di stato TDM \_ set \_ Marquee \_ \_</span><span class="sxs-lookup"><span data-stu-id="c16e0-104">TDM\_SET\_MARQUEE\_PROGRESS\_BAR message</span></span>

<span data-ttu-id="c16e0-105">Indica se l'indicatore di stato ospitato di una finestra di dialogo attività deve essere visualizzato in modalità marquee.</span><span class="sxs-lookup"><span data-stu-id="c16e0-105">Indicates whether the hosted progress bar of a task dialog should be displayed in marquee mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="c16e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c16e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c16e0-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c16e0-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c16e0-108">**Bool** che indica se l'indicatore di stato deve essere visualizzato in modalità marquee.</span><span class="sxs-lookup"><span data-stu-id="c16e0-108">A **BOOL** that indicates whether the progress bar should be shown in marquee mode.</span></span> <span data-ttu-id="c16e0-109">Il valore **true** attiva la modalità marquee e il valore **false** disattiva la modalità marquee.</span><span class="sxs-lookup"><span data-stu-id="c16e0-109">A value of **TRUE** turns on marquee mode, and a value of **FALSE** turns off marquee mode.</span></span>

</dd> <dt>

<span data-ttu-id="c16e0-110">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c16e0-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c16e0-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c16e0-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c16e0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c16e0-112">Return value</span></span>

<span data-ttu-id="c16e0-113">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c16e0-113">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="c16e0-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c16e0-114">Remarks</span></span>

<span data-ttu-id="c16e0-115">Per informazioni sulla modalità Marquee, vedere [controllo indicatore di stato](progress-bar-control.md).</span><span class="sxs-lookup"><span data-stu-id="c16e0-115">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c16e0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c16e0-116">Requirements</span></span>



| <span data-ttu-id="c16e0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c16e0-117">Requirement</span></span> | <span data-ttu-id="c16e0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c16e0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c16e0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c16e0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c16e0-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c16e0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c16e0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c16e0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c16e0-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c16e0-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c16e0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c16e0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c16e0-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c16e0-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





