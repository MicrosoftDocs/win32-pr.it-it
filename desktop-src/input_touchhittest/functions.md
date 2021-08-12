---
title: Funzioni (hit testing tocco)
description: Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le funzioni touch hit testing.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- interazione dell'utente
- input
- indicatore di misura
- tocco
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 83ab93fbff031423b6478926e499077ac78b1aec686d596ca069fda6d1b2298b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248358"
---
# <a name="touch-hit-testing-functions"></a>Funzioni touch hit testing

Negli argomenti di questa sezione vengono fornite le specifiche di riferimento per le [funzioni touch hit testing](functions.md).

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
| --- | --- |
| [**EvaluateProximityToPolygon**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | Restituisce il punteggio di un poligono come probabile destinazione di tocco (rispetto a tutti gli altri poligoni che intersecano l'area di contatto tocco) e un punto di tocco regolato all'interno del poligono. <br/> |
| [**EvaluateProximityToRect**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | Restituisce il punteggio di un rettangolo come probabile destinazione del tocco, rispetto a tutti gli altri rettangoli che intersecano l'area di contatto del tocco e un punto di tocco regolato all'interno del rettangolo. <br/> |
| [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | Restituisce il punteggio di valutazione di prossimità e le coordinate del punto di tocco regolate come valore imballato per il callback WM_TOUCHHITTESTING [messaggio.](../inputmsg/wm-touchhittesting.md) <br/> |
| [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | Registra una finestra per elaborare la [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) notifica<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Informazioni di riferimento sui test di hit testing tocco](touchhittest-reference.md)
