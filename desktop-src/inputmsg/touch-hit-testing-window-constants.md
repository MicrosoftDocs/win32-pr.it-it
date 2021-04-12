---
title: Costanti finestra di hit testing tocco
description: Indica la modalità di elaborazione dei messaggi per l'hit testing di tocco da parte di Windows registrate tramite la funzione RegisterTouchHitTestingWindow.
ms.assetid: CC6CCD0B-882F-4DA7-B886-D4BD18D6060C
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 46d577e03eaf918e4f2ea40aae30a2ab5112b630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400811"
---
# <a name="touch-hit-testing-window-constants"></a><span data-ttu-id="f1125-103">Costanti finestra di hit testing tocco</span><span class="sxs-lookup"><span data-stu-id="f1125-103">Touch Hit Testing Window Constants</span></span>

<span data-ttu-id="f1125-104">Indica la modalità di elaborazione dei messaggi per l'hit testing di tocco da parte di Windows registrate tramite la funzione [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="f1125-104">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>



| <span data-ttu-id="f1125-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="f1125-105">Constant/value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="f1125-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1125-106">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TOUCH_HIT_TESTING_DEFAULT"></span><span id="touch_hit_testing_default"></span><dl> <span data-ttu-id="f1125-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f1125-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="f1125-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messaggi non vengono inviati alla finestra di destinazione, ma vengono inviati alle finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="f1125-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span id="TOUCH_HIT_TESTING_CLIENT"></span><span id="touch_hit_testing_client"></span><dl> <span data-ttu-id="f1125-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f1125-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="f1125-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messaggi vengono inviati alla finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f1125-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span id="TOUCH_HIT_TESTING_NONE"></span><span id="touch_hit_testing_none"></span><dl> <span data-ttu-id="f1125-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="f1125-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span></span> </dl>          | <span data-ttu-id="f1125-112">I messaggi di [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) non vengono inviati alla finestra di destinazione o alle finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="f1125-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="f1125-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1125-113">Requirements</span></span>



| <span data-ttu-id="f1125-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1125-114">Requirement</span></span> | <span data-ttu-id="f1125-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f1125-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f1125-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1125-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f1125-117">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f1125-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f1125-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1125-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f1125-119">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f1125-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f1125-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1125-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1125-121"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1125-121"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1125-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1125-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1125-123">Costanti</span><span class="sxs-lookup"><span data-stu-id="f1125-123">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="f1125-124">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="f1125-124">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

