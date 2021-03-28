---
description: Un'applicazione invalida una parte di una finestra e imposta l'area di aggiornamento tramite la funzione InvalidateRect o InvalidateRgn.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Invalidare e convalidare l'area di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba895875f9ec1350b6eb28ccb8f1721df6999ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978578"
---
# <a name="invalidating-and-validating-the-update-region"></a><span data-ttu-id="4ec97-103">Invalidare e convalidare l'area di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4ec97-103">Invalidating and Validating the Update Region</span></span>

<span data-ttu-id="4ec97-104">Un'applicazione invalida una parte di una finestra e imposta l'area di aggiornamento tramite la funzione [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) o [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) .</span><span class="sxs-lookup"><span data-stu-id="4ec97-104">An application invalidates a portion of a window and sets the update region by using the [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function.</span></span> <span data-ttu-id="4ec97-105">Queste funzioni aggiungono il rettangolo o l'area specificata (in coordinate client) all'area di aggiornamento, combinando il rettangolo o l'area con qualsiasi elemento che il sistema o l'applicazione potrebbe avere precedentemente aggiunto all'area di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4ec97-105">These functions add the specified rectangle or region (in client coordinates) to the update region, combining the rectangle or region with anything the system or the application may have previously added to the update region.</span></span>

<span data-ttu-id="4ec97-106">Le funzioni [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) e [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) non generano messaggi di [**\_ disegno WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="4ec97-106">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) and [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) functions do not generate [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="4ec97-107">Al contrario, il sistema accumula le modifiche apportate da queste funzioni e le proprie modifiche mentre una finestra elabora altri messaggi nella coda di messaggi.</span><span class="sxs-lookup"><span data-stu-id="4ec97-107">Instead, the system accumulates the changes made by these functions and its own changes while a window processes other messages in its message queue.</span></span> <span data-ttu-id="4ec97-108">Accumulando le modifiche, una finestra elabora tutte le modifiche in una sola volta anziché aggiornare i bit e le parti un passaggio alla volta.</span><span class="sxs-lookup"><span data-stu-id="4ec97-108">By accumulating changes, a window processes all changes at once instead of updating bits and pieces one step at a time.</span></span>

<span data-ttu-id="4ec97-109">Le funzioni [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) e [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) convalidano una parte della finestra rimuovendo un rettangolo o un'area specificata dall'area di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4ec97-109">The [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) and [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) functions validate a portion of the window by removing a specified rectangle or region from the update region.</span></span> <span data-ttu-id="4ec97-110">Queste funzioni vengono in genere usate quando la finestra ha aggiornato una parte specifica della schermata nell'area di aggiornamento prima di ricevere il messaggio di [**\_ disegno WM**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="4ec97-110">These functions are typically used when the window has updated a specific part of the screen in the update region before receiving the [**WM\_PAINT**](wm-paint.md) message.</span></span>

 

 



