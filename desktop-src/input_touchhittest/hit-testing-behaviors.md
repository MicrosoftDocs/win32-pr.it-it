---
title: Comportamenti di hit testing tocco
description: Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare la modalità di elaborazione dei messaggi per l'hit testing di tocco da parte di Windows registrate tramite la funzione RegisterTouchHitTestingWindow.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
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
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302207"
---
# <a name="touch-hit-testing-behaviors"></a><span data-ttu-id="25d30-103">Comportamenti di hit testing tocco</span><span class="sxs-lookup"><span data-stu-id="25d30-103">Touch Hit Testing Behaviors</span></span>

<span data-ttu-id="25d30-104">Le costanti seguenti vengono usate dalle applicazioni o dai framework dell'interfaccia utente per identificare la modalità di elaborazione dei messaggi per l'hit testing di tocco da parte di Windows registrate tramite la funzione [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="25d30-104">The following constants are used by applications or UI frameworks to identify how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

| <span data-ttu-id="25d30-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="25d30-105">Constant/value</span></span> | <span data-ttu-id="25d30-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25d30-106">Description</span></span> |
|---|---|
| <span data-ttu-id="25d30-107">**TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="25d30-107">**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</span></span> | <span data-ttu-id="25d30-108">Indica che i messaggi di [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) non vengono inviati alla finestra di destinazione, ma vengono inviati alle finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="25d30-108">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span data-ttu-id="25d30-109">**TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="25d30-109">**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</span></span>    | <span data-ttu-id="25d30-110">Indica che [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messaggi vengono inviati alla finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="25d30-110">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span data-ttu-id="25d30-111">**TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="25d30-111">**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</span></span>          | <span data-ttu-id="25d30-112">Indica che i messaggi di [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) non vengono inviati alla finestra di destinazione o alle finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="25d30-112">Indicates that [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |

## <a name="requirements"></a><span data-ttu-id="25d30-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25d30-113">Requirements</span></span>

| <span data-ttu-id="25d30-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="25d30-114">Requirement</span></span> | <span data-ttu-id="25d30-115">Valore</span><span class="sxs-lookup"><span data-stu-id="25d30-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="25d30-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25d30-116">Minimum supported client</span></span><br/> | <span data-ttu-id="25d30-117">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="25d30-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="25d30-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25d30-118">Minimum supported server</span></span><br/> | <span data-ttu-id="25d30-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="25d30-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="25d30-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25d30-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="25d30-121"><dt>Winuser. h</span><span class="sxs-lookup"><span data-stu-id="25d30-121"><dt>Winuser.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="25d30-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25d30-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25d30-123">Costanti</span><span class="sxs-lookup"><span data-stu-id="25d30-123">Constants</span></span>](constants.md)
