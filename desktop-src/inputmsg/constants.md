---
title: Costanti notifiche e messaggi di input del puntatore
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per i messaggi di input del puntatore e le costanti di notifica.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114803138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6db54614e10c02cea5dfd4df9b7cf637abb3977c
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334398"
---
# <a name="pointer-input-messages-and-notifications-constants"></a><span data-ttu-id="22750-103">Costanti notifiche e messaggi di input del puntatore</span><span class="sxs-lookup"><span data-stu-id="22750-103">Pointer Input Messages and Notifications constants</span></span>

<span data-ttu-id="22750-104">Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per [i messaggi di input del puntatore e](messages-and-notifications-portal.md) le costanti di notifica.</span><span class="sxs-lookup"><span data-stu-id="22750-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) constants.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="22750-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="22750-105">In this section</span></span>



| <span data-ttu-id="22750-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="22750-106">Topic</span></span>                                                                             | <span data-ttu-id="22750-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22750-107">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22750-108">**Stato del tasto di modifica**</span><span class="sxs-lookup"><span data-stu-id="22750-108">**Modifier Key State**</span></span>](modifier-key-states-constants.md)<br/>            | <span data-ttu-id="22750-109">Indica i tasti di modifica della tastiera che sono stati premuti al momento della generazione dell'input.</span><span class="sxs-lookup"><span data-stu-id="22750-109">Indicates which keyboard modifier keys were pressed at the time input was being generated.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="22750-110">**Flag di penna**</span><span class="sxs-lookup"><span data-stu-id="22750-110">**Pen Flags**</span></span>](pen-flags-constants.md)<br/>                               | <span data-ttu-id="22750-111">Valori che possono essere visualizzati nel campo **penFlags** della struttura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="22750-111">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                         |
| [<span data-ttu-id="22750-112">**Maschera di penna**</span><span class="sxs-lookup"><span data-stu-id="22750-112">**Pen Mask**</span></span>](pen-mask-constants.md)<br/>                                 | <span data-ttu-id="22750-113">Valori che possono essere visualizzati nel campo **penMask** della struttura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="22750-113">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                          |
| [<span data-ttu-id="22750-114">**Modifica dispositivo puntatore**</span><span class="sxs-lookup"><span data-stu-id="22750-114">**Pointer Device Change**</span></span>](pointer-device-change-constants.md)<br/>       | <span data-ttu-id="22750-115">Valori che possono essere passati nel parametro *wParam* del messaggio di [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="22750-115">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span><br/>                                                                    |
| [<span data-ttu-id="22750-116">**Flag puntatore**</span><span class="sxs-lookup"><span data-stu-id="22750-116">**Pointer Flags**</span></span>](pointer-flags-contants.md)<br/>                        | <span data-ttu-id="22750-117">Valori che possono essere visualizzati nel campo **pointerFlags** della struttura [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="22750-117">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                              |
| [<span data-ttu-id="22750-118">**Flag messaggi puntatore**</span><span class="sxs-lookup"><span data-stu-id="22750-118">**Pointer Message Flags**</span></span>](pointer-message-flags.md)<br/>                 | <span data-ttu-id="22750-119">Valori utilizzati in diverse macro del puntatore (vedere [macro](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="22750-119">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="22750-120">**Flag tocco**</span><span class="sxs-lookup"><span data-stu-id="22750-120">**Touch Flags**</span></span>](touch-flags-constants.md)<br/>                           | <span data-ttu-id="22750-121">Valori che possono essere visualizzati nel campo **touchFlags** della struttura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="22750-121">Values that can appear in the **touchFlags** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                   |
| [<span data-ttu-id="22750-122">**Finestra hit testing tocco**</span><span class="sxs-lookup"><span data-stu-id="22750-122">**Touch Hit Testing Window**</span></span>](touch-hit-testing-window-constants.md)<br/> | <span data-ttu-id="22750-123">Indica la modalità di elaborazione dei messaggi per l'hit testing di tocco da parte di Windows registrate tramite la funzione [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="22750-123">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span><br/> |
| [<span data-ttu-id="22750-124">**Touch mask**</span><span class="sxs-lookup"><span data-stu-id="22750-124">**Touch Mask**</span></span>](touch-mask-constants.md)<br/>                             | <span data-ttu-id="22750-125">Valori che possono essere visualizzati nel campo **touchMask** della struttura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="22750-125">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span><br/>                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="22750-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22750-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22750-127">Riferimento al messaggio di input del puntatore</span><span class="sxs-lookup"><span data-stu-id="22750-127">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

