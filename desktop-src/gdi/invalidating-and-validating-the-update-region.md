---
description: Un'applicazione invalida una parte di una finestra e imposta l'area di aggiornamento usando la funzione InvalidateRect o InvalidateRgn.
ms.assetid: ec8abb77-47bc-4198-9daf-f2ccb0864ccc
title: Invalidazione e convalida dell'area di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6813d88674ef0339cfd3501b561e5a7c95fa5b41f0c7f212e625f9846f5beb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944171"
---
# <a name="invalidating-and-validating-the-update-region"></a>Invalidazione e convalida dell'area di aggiornamento

Un'applicazione invalida una parte di una finestra e imposta l'area di aggiornamento usando la funzione [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) [**o InvalidateRgn.**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) Queste funzioni aggiungono il rettangolo o l'area specificata (nelle coordinate del client) all'area di aggiornamento, combinando il rettangolo o l'area con qualsiasi elemento aggiunto in precedenza dal sistema o dall'applicazione all'area di aggiornamento.

Le [**funzioni InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) [**e InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) non generano [**messaggi WM \_ PAINT.**](wm-paint.md) Al contrario, il sistema accumula le modifiche apportate da queste funzioni e le proprie modifiche mentre una finestra elabora altri messaggi nella relativa coda di messaggi. Accumulando le modifiche, una finestra elabora tutte le modifiche contemporaneamente anziché aggiornare bit e parti un passaggio alla volta.

Le [**funzioni ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) [**e ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) convalidano una parte della finestra rimuovendo un rettangolo o un'area specificata dall'area di aggiornamento. Queste funzioni vengono in genere usate quando la finestra ha aggiornato una parte specifica dello schermo nell'area di aggiornamento prima di ricevere il [**messaggio WM \_ PAINT.**](wm-paint.md)

 

 



