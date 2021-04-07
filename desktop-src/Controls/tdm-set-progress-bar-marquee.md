---
title: Messaggio TDM_SET_PROGRESS_BAR_MARQUEE (COMmctrl. h)
description: Avvia e arresta la visualizzazione Marquee dell'indicatore di stato in una finestra di dialogo attività e imposta la velocità del Marquee.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- Controlli di Windows Message TDM_SET_PROGRESS_BAR_MARQUEE
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048700"
---
# <a name="tdm_set_progress_bar_marquee-message"></a><span data-ttu-id="fea2b-104">Messaggio del Marquee indicatore di \_ stato set TDM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="fea2b-104">TDM\_SET\_PROGRESS\_BAR\_MARQUEE message</span></span>

<span data-ttu-id="fea2b-105">Avvia e arresta la visualizzazione Marquee dell'indicatore di stato in una finestra di dialogo attività e imposta la velocità del Marquee.</span><span class="sxs-lookup"><span data-stu-id="fea2b-105">Starts and stops the marquee display of the progress bar in a task dialog, and sets the speed of the marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="fea2b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fea2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fea2b-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fea2b-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fea2b-108">Valore **bool** che indica se attivare o disattivare la visualizzazione Marquee.</span><span class="sxs-lookup"><span data-stu-id="fea2b-108">A **BOOL** that indicates whether to turn the marquee display on or off.</span></span> <span data-ttu-id="fea2b-109">Utilizzare **true** per attivare la visualizzazione Marquee oppure **false** per disattivarla.</span><span class="sxs-lookup"><span data-stu-id="fea2b-109">Use **TRUE** to turn on the marquee display, or **FALSE** to turn it off.</span></span>

</dd> <dt>

<span data-ttu-id="fea2b-110">*lParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fea2b-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fea2b-111">**Uint** che specifica il tempo, in millisecondi, tra gli aggiornamenti dell'animazione Marquee.</span><span class="sxs-lookup"><span data-stu-id="fea2b-111">A **UINT** that specifies the time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="fea2b-112">Se questo parametro è zero, l'animazione Marquee viene aggiornata ogni 30 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="fea2b-112">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fea2b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fea2b-113">Return value</span></span>

<span data-ttu-id="fea2b-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="fea2b-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="fea2b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fea2b-115">Remarks</span></span>

<span data-ttu-id="fea2b-116">Per informazioni sulla modalità Marquee, vedere [controllo indicatore di stato](progress-bar-control.md).</span><span class="sxs-lookup"><span data-stu-id="fea2b-116">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fea2b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fea2b-117">Requirements</span></span>



| <span data-ttu-id="fea2b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fea2b-118">Requirement</span></span> | <span data-ttu-id="fea2b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fea2b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fea2b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fea2b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fea2b-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fea2b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fea2b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fea2b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fea2b-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fea2b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fea2b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fea2b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fea2b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fea2b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





