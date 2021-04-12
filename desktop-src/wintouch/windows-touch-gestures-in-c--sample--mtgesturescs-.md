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
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a><span data-ttu-id="a85bc-110">Movimenti tocco di Windows nell'esempio C# (MTGesturesCS)</span><span class="sxs-lookup"><span data-stu-id="a85bc-110">Windows Touch Gestures in C# Sample (MTGesturesCS)</span></span>

<span data-ttu-id="a85bc-111">Questa sezione descrive l'esempio di movimenti tocco di Windows in C#.</span><span class="sxs-lookup"><span data-stu-id="a85bc-111">This section describes the Windows Touch Gestures sample in C#.</span></span>

<span data-ttu-id="a85bc-112">Questo esempio di movimenti tocco di Windows illustra come usare i messaggi di movimento per tradurre, ruotare e ridimensionare una casella di cui è stato eseguito il rendering tramite il Graphics Device Interface (GDI) gestendo il messaggio di [**WM_GESTURE**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="a85bc-112">This Windows Touch Gestures sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="a85bc-113">Lo screenshot seguente mostra l'aspetto dell'esempio durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a85bc-113">The following screen shot shows how the sample looks when it is running.</span></span>

![screenshot che mostra i movimenti tocco di Windows nell'esempio c Sharp quando è in esecuzione, con un rettangolo bianco delineato al centro sullo schermo](images/mtgesturescs.png)

<span data-ttu-id="a85bc-115">Per questo esempio, i messaggi di movimento vengono passati a un motore di movimento che chiama quindi i metodi per disegnare oggetti per tradurre, ruotare e ridimensionare un oggetto con metodi per la gestione di questi comandi.</span><span class="sxs-lookup"><span data-stu-id="a85bc-115">For this sample, gesture messages are passed to a gesture engine which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="a85bc-116">Per rendere possibile questa operazione in C#, viene creato un modulo speciale, TouchableForm, per gestire i messaggi di movimento.</span><span class="sxs-lookup"><span data-stu-id="a85bc-116">To make this possible in C#, a special form, TouchableForm, is created to handle gesture messages.</span></span> <span data-ttu-id="a85bc-117">Questo form utilizza quindi i messaggi per apportare modifiche a un oggetto Drawing, DrawingObject, per modificare la modalità di rendering dell'oggetto nel metodo Paint.</span><span class="sxs-lookup"><span data-stu-id="a85bc-117">This form then uses the messages to make changes on a drawing object, DrawingObject, to change how the object renders in the Paint method.</span></span>

<span data-ttu-id="a85bc-118">Per illustrare il funzionamento dell'esempio, prendere in considerazione i passaggi per l'utilizzo del comando Pan per tradurre la casella sottoposta a rendering.</span><span class="sxs-lookup"><span data-stu-id="a85bc-118">To help show how the sample works, consider the steps for using the pan command to translate the rendered box.</span></span> <span data-ttu-id="a85bc-119">Un utente esegue il gesto di panoramica che genera un messaggio di [**WM_GESTURE**](wm-gesture.md) con l'identificatore del movimento GID_PAN.</span><span class="sxs-lookup"><span data-stu-id="a85bc-119">A user performs the pan gesture which generates a [**WM_GESTURE**](wm-gesture.md) message with the gesture identifier GID_PAN.</span></span> <span data-ttu-id="a85bc-120">TouchableForm gestisce i messaggi e aggiorna la posizione dell'oggetto Drawing e l'oggetto viene quindi sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="a85bc-120">The TouchableForm handles this messages and updates the position of the drawing object, and the object will then render itself translated.</span></span>

<span data-ttu-id="a85bc-121">Nel codice seguente viene illustrato il modo in cui il gestore movimenti recupera i parametri dal messaggio di [**WM_GESTURE**](wm-gesture.md) e quindi esegue la conversione sulla casella di cui è stato eseguito il rendering tramite una chiamata al metodo Move dell'oggetto Drawing.</span><span class="sxs-lookup"><span data-stu-id="a85bc-121">The following code shows how the gesture handler retrieves parameters from the [**WM_GESTURE**](wm-gesture.md) message and then performs translation on the rendered box through a call to the drawing object's move method.</span></span>

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

<span data-ttu-id="a85bc-122">Nel codice seguente viene illustrato il modo in cui il metodo Move dell'oggetto Drawing aggiorna le variabili di posizione interna.</span><span class="sxs-lookup"><span data-stu-id="a85bc-122">The following code shows how the drawing object's move method updates internal position variables.</span></span>

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

<span data-ttu-id="a85bc-123">Il codice seguente mostra come viene usata la posizione nel metodo Paint dell'oggetto Drawing.</span><span class="sxs-lookup"><span data-stu-id="a85bc-123">The following code shows how the position is used in the drawing object's paint method.</span></span>

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

<span data-ttu-id="a85bc-124">I movimenti di Pan provocheranno il rendering della casella disegnata.</span><span class="sxs-lookup"><span data-stu-id="a85bc-124">Pan gestures will cause the drawn box to be rendered translated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a85bc-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a85bc-125">Related topics</span></span>

<span data-ttu-id="a85bc-126">[Applicazione movimenti multitocco (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [applicazione movimenti multitocco (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [esempi di Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="a85bc-126">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
