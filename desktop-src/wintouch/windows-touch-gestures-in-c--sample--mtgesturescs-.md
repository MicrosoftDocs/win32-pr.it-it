---
title: Movimenti tocco di Windows nell'esempio C (MTGesturesCS)
description: In questa sezione viene descritto l'esempio di movimenti tocco di Windows in C \.
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
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
ms.openlocfilehash: e6ffc0e8caf63807d4df80a1b96229f2fa7b5ff9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398564"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a>Movimenti tocco di Windows nell'esempio C# (MTGesturesCS)

Questa sezione descrive l'esempio di movimenti tocco di Windows in C#.

Questo esempio di movimenti tocco di Windows illustra come usare i messaggi di movimento per tradurre, ruotare e ridimensionare una casella di cui è stato eseguito il rendering tramite il Graphics Device Interface (GDI) gestendo il messaggio di [**WM_GESTURE**](wm-gesture.md) . Lo screenshot seguente mostra l'aspetto dell'esempio durante l'esecuzione.

![screenshot che mostra i movimenti tocco di Windows nell'esempio c Sharp quando è in esecuzione, con un rettangolo bianco delineato al centro sullo schermo](images/mtgesturescs.png)

Per questo esempio, i messaggi di movimento vengono passati a un motore di movimento che chiama quindi i metodi per disegnare oggetti per tradurre, ruotare e ridimensionare un oggetto con metodi per la gestione di questi comandi. Per rendere possibile questa operazione in C#, viene creato un modulo speciale, TouchableForm, per gestire i messaggi di movimento. Questo form utilizza quindi i messaggi per apportare modifiche a un oggetto Drawing, DrawingObject, per modificare la modalità di rendering dell'oggetto nel metodo Paint.

Per illustrare il funzionamento dell'esempio, prendere in considerazione i passaggi per l'utilizzo del comando Pan per tradurre la casella sottoposta a rendering. Un utente esegue il gesto di panoramica che genera un messaggio di [**WM_GESTURE**](wm-gesture.md) con l'identificatore del movimento GID_PAN. TouchableForm gestisce i messaggi e aggiorna la posizione dell'oggetto Drawing e l'oggetto viene quindi sottoposto a rendering.

Nel codice seguente viene illustrato il modo in cui il gestore movimenti recupera i parametri dal messaggio di [**WM_GESTURE**](wm-gesture.md) e quindi esegue la conversione sulla casella di cui è stato eseguito il rendering tramite una chiamata al metodo Move dell'oggetto Drawing.

```CSharp
            switch (gi.dwID)
            {
                case GID_BEGIN:
                case GID_END:
                    break;
               (...)
                case GID_PAN:
                    switch (gi.dwFlags)
                    {
                        case GF_BEGIN:
                            _ptFirst.X = gi.ptsLocation.x;
                            _ptFirst.Y = gi.ptsLocation.y;
                            _ptFirst = PointToClient(_ptFirst);
                            break;

                        default:
                            // We read the second point of this gesture. It is a
                            // middle point between fingers in this new position
                            _ptSecond.X = gi.ptsLocation.x;
                            _ptSecond.Y = gi.ptsLocation.y;
                            _ptSecond = PointToClient(_ptSecond);

                            // We apply move operation of the object
                            _dwo.Move(_ptSecond.X - _ptFirst.X, _ptSecond.Y - _ptFirst.Y);

                            Invalidate();

                            // We have to copy second point into first one to
                            // prepare for the next step of this gesture.
                            _ptFirst = _ptSecond;
                            break;
                    }
                    break;
```

Nel codice seguente viene illustrato il modo in cui il metodo Move dell'oggetto Drawing aggiorna le variabili di posizione interna.

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

Il codice seguente mostra come viene usata la posizione nel metodo Paint dell'oggetto Drawing.

```CSharp
public void Paint(Graphics graphics)
        {
(...)
            for (int j = 0; j < 5; j++)
            {
                int idx = arrPts[j].X;
                int idy = arrPts[j].Y;

                // rotation
                arrPts[j].X = (int)(idx * dCos + idy * dSin);
                arrPts[j].Y = (int)(idy * dCos - idx * dSin);

                // translation
                arrPts[j].X += _ptCenter.X;
                arrPts[j].Y += _ptCenter.Y;
            }
(...)
        }
```

I movimenti di Pan provocheranno il rendering della casella disegnata.

## <a name="related-topics"></a>Argomenti correlati

[Applicazione movimenti multitocco (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [applicazione movimenti multitocco (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [esempi di Windows Touch](windows-touch-samples.md)
