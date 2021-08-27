---
title: Windows Movimenti tocco nell'esempio C (MTGesturesCS)
description: Questa sezione descrive l'Windows di movimenti tocco in C\ .
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
keywords:
- Windows Tocco, esempi di codice
- Windows Tocco, codice di esempio
- Windows Tocco, movimenti
- Windows Esempi di tocco, movimento
- Esempi di movimenti
- movimenti, codice di esempio
- movimenti, esempi di codice
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: ac3a7c0772ad7329d14d9909b55f8a60ef6e7d7473a06fcba921297117a00b6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089906"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a>Windows Esempio di movimenti tocco in C# (MTGesturesCS)

Questa sezione descrive l'Windows di movimenti tocco in C#.

Questo Windows di movimenti tocco illustra come usare i messaggi di movimento per traslare, ruotare e ridimensionare [](wm-gesture.md) un riquadro di cui viene eseguito il rendering da parte del Graphics Device Interface (GDI) gestendo il messaggio WM_GESTURE. Lo screenshot seguente mostra l'aspetto dell'esempio quando è in esecuzione.

![Screenshot che mostra i movimenti tocco di Windows nell'esempio c sharp quando è in esecuzione, con un rettangolo bianco con contorno nero centrato sullo schermo](images/mtgesturescs.png)

Per questo esempio, i messaggi di movimento vengono passati a un motore movimenti che chiama quindi i metodi sugli oggetti di disegno per traslare, ruotare e ridimensionare un oggetto che dispone di metodi per la gestione di questi comandi. Per rendere possibile questa operazione in C#, viene creato un modulo speciale, TouchableForm, per gestire i messaggi di movimento. Questo form usa quindi i messaggi per apportare modifiche a un oggetto di disegno, DrawingObject, per modificare la modalità di rendering dell'oggetto Paint metodo .

Per illustrare il funzionamento dell'esempio, prendere in considerazione la procedura per usare il comando pan per tradurre la casella sottoposta a rendering. Un utente esegue il movimento di panoramica che genera un messaggio [**WM_GESTURE**](wm-gesture.md) con l'identificatore del movimento GID_PAN. TouchableForm gestisce questi messaggi e aggiorna la posizione dell'oggetto di disegno e l'oggetto eseguirà quindi il rendering di se stesso tradotto.

Il codice seguente illustra come il gestore movimenti recupera i parametri dal messaggio WM_GESTURE e quindi esegue la traslazione nella casella sottoposta [**a**](wm-gesture.md) rendering tramite una chiamata al metodo move dell'oggetto di disegno.

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

Nel codice seguente viene illustrato come il metodo move dell'oggetto di disegno aggiorna le variabili di posizione interne.

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

Nel codice seguente viene illustrato come utilizzare la posizione nel metodo di disegno dell'oggetto di disegno.

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

I movimenti di panoramica determinano la traduzione della casella disegnata.

## <a name="related-topics"></a>Argomenti correlati

[Applicazione Movimenti multitocchetto (C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS)Applicazione movimenti [multitocchetto (C++),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp) [Windows touch](windows-touch-samples.md)
