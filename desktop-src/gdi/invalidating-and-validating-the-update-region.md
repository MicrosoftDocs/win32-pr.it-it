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
# <a name="invalidating-and-validating-the-update-region"></a>Invalidare e convalidare l'area di aggiornamento

Un'applicazione invalida una parte di una finestra e imposta l'area di aggiornamento tramite la funzione [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) o [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) . Queste funzioni aggiungono il rettangolo o l'area specificata (in coordinate client) all'area di aggiornamento, combinando il rettangolo o l'area con qualsiasi elemento che il sistema o l'applicazione potrebbe avere precedentemente aggiunto all'area di aggiornamento.

Le funzioni [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) e [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) non generano messaggi di [**\_ disegno WM**](wm-paint.md) . Al contrario, il sistema accumula le modifiche apportate da queste funzioni e le proprie modifiche mentre una finestra elabora altri messaggi nella coda di messaggi. Accumulando le modifiche, una finestra elabora tutte le modifiche in una sola volta anziché aggiornare i bit e le parti un passaggio alla volta.

Le funzioni [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) e [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) convalidano una parte della finestra rimuovendo un rettangolo o un'area specificata dall'area di aggiornamento. Queste funzioni vengono in genere usate quando la finestra ha aggiornato una parte specifica della schermata nell'area di aggiornamento prima di ricevere il messaggio di [**\_ disegno WM**](wm-paint.md) .

 

 



