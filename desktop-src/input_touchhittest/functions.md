---
title: Funzioni (hit testing touch)
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le funzioni di hit testing.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- interazione dell'utente
- input
- indicatore di misura
- tocco
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334021"
---
# <a name="touch-hit-testing-functions"></a>Funzioni di hit testing tocco

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le [funzioni di hit testing](functions.md).

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
| --- | --- |
| [**EvaluateProximityToPolygon**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | Restituisce il Punteggio di un poligono come destinazione del tocco probabile (rispetto a tutti gli altri poligoni che intersecano l'area di contatto tocco) e un punto di tocco regolato all'interno del poligono. <br/> |
| [**EvaluateProximityToRect**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | Restituisce il Punteggio di un rettangolo come destinazione del tocco probabile, rispetto a tutti gli altri rettangoli che intersecano l'area di contatto tocco e a un punto di tocco regolato all'interno del rettangolo. <br/> |
| [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | Restituisce il Punteggio di valutazione di prossimità e le coordinate del punto di tocco modificate come valore compresso per il callback del [messaggio WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) . <br/> |
| [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | Registra una finestra per elaborare la notifica di [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md)<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Riferimento all'hit testing tocco](touchhittest-reference.md)
