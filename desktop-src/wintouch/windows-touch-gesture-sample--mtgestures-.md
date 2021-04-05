---
title: Esempio di movimento tocco di Windows (MTGestures)
description: In questa sezione viene descritto l'esempio di movimento tocco di Windows.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
keywords:
- Windows Touch, esempi di codice
- Windows Touch, codice di esempio
- Windows Touch, movimenti
- Windows Touch, esempi di movimenti
- Esempi di movimento
- movimenti, codice di esempio
- movimenti, esempi di codice
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 0e01d97e844af37caeb5c33f3cb780601da4629d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723446"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a>Esempio di movimento tocco di Windows (MTGestures)

In questa sezione viene descritto l'esempio di movimento tocco di Windows.

Nell'esempio di movimento tocco di Windows viene illustrato come utilizzare i messaggi di movimento per tradurre, ruotare e ridimensionare una casella sottoposta a rendering dal Graphics Device Interface (GDI) gestendo il messaggio di [**WM_GESTURE**](wm-gesture.md) . Lo screenshot seguente mostra l'aspetto dell'esempio durante l'esecuzione.

![screenshot che mostra l'esempio di movimento tocco di Windows quando è in esecuzione, con un rettangolo bianco delineato ruotato in nero sullo schermo](images/mtgestures.png)

Per questo esempio, i messaggi di movimento vengono passati a un motore di movimento, che chiama quindi i metodi per disegnare oggetti per tradurre, ruotare e ridimensionare un oggetto con metodi per la gestione di questi comandi. Per illustrare il funzionamento dell'esempio, prendere in considerazione i passaggi per l'uso del comando di tocco con due dita per abilitare o disabilitare le linee diagonali nella casella di cui è stato eseguito il rendering. Un utente esegue il gesto di tocco con due dita, che genera un messaggio gestito dal programma. Quando il messaggio viene gestito, verrà attivato o disattivato un valore booleano per il rendering delle diagonali nell'oggetto Drawing e l'oggetto eseguirà il rendering delle linee diagonali.

Nel codice seguente viene illustrato il modo in cui i messaggi di movimento vengono passati al motore di movimento dal metodo WndProc.

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

Il codice seguente illustra il modo in cui il motore di movimento gestisce il comando di tocco con due dita.

```C++
// Two-finger tap command
void CMyGestureEngine::ProcessTwoFingerTap(void)
{
    if(_pcRect)
    {
        _pcRect->ToggleDrawDiagonals();
    }
}
```

Nel codice seguente viene illustrato il modo in cui l'oggetto Drawing commuta le diagonali.

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

Il codice seguente mostra come l'oggetto esegue il rendering delle linee diagonali nel metodo di disegnare.

```C++
    if(_bDrawDiagonals)
    {
        // draw diagonals
        MoveToEx(hdc,ptRect[0].x,ptRect[0].y,NULL);
        LineTo(hdc,ptRect[2].x,ptRect[2].y);
        MoveToEx(hdc,ptRect[1].x,ptRect[1].y,NULL);
        LineTo(hdc,ptRect[3].x,ptRect[3].y);
    }
```

## <a name="related-topics"></a>Argomenti correlati

[Applicazione movimenti multitocco (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [applicazione movimenti multitocco (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [esempi di Windows Touch](windows-touch-samples.md)
