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
# <a name="windows-touch-gesture-sample-mtgestures"></a><span data-ttu-id="23a21-110">Esempio di movimento tocco di Windows (MTGestures)</span><span class="sxs-lookup"><span data-stu-id="23a21-110">Windows Touch Gesture Sample (MTGestures)</span></span>

<span data-ttu-id="23a21-111">In questa sezione viene descritto l'esempio di movimento tocco di Windows.</span><span class="sxs-lookup"><span data-stu-id="23a21-111">This section describes the Windows Touch Gesture sample.</span></span>

<span data-ttu-id="23a21-112">Nell'esempio di movimento tocco di Windows viene illustrato come utilizzare i messaggi di movimento per tradurre, ruotare e ridimensionare una casella sottoposta a rendering dal Graphics Device Interface (GDI) gestendo il messaggio di [**WM_GESTURE**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="23a21-112">The Windows Touch Gesture sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="23a21-113">Lo screenshot seguente mostra l'aspetto dell'esempio durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="23a21-113">The following screen shot shows how the sample looks when it is running.</span></span>

![screenshot che mostra l'esempio di movimento tocco di Windows quando è in esecuzione, con un rettangolo bianco delineato ruotato in nero sullo schermo](images/mtgestures.png)

<span data-ttu-id="23a21-115">Per questo esempio, i messaggi di movimento vengono passati a un motore di movimento, che chiama quindi i metodi per disegnare oggetti per tradurre, ruotare e ridimensionare un oggetto con metodi per la gestione di questi comandi.</span><span class="sxs-lookup"><span data-stu-id="23a21-115">For this sample, gesture messages are passed to a gesture engine, which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="23a21-116">Per illustrare il funzionamento dell'esempio, prendere in considerazione i passaggi per l'uso del comando di tocco con due dita per abilitare o disabilitare le linee diagonali nella casella di cui è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="23a21-116">To help show how the sample works, consider the steps for using the two-finger tap command to enable or disable diagonal lines in the rendered box.</span></span> <span data-ttu-id="23a21-117">Un utente esegue il gesto di tocco con due dita, che genera un messaggio gestito dal programma.</span><span class="sxs-lookup"><span data-stu-id="23a21-117">A user performs the two-finger tap gesture, which generates a message that is handled by the program.</span></span> <span data-ttu-id="23a21-118">Quando il messaggio viene gestito, verrà attivato o disattivato un valore booleano per il rendering delle diagonali nell'oggetto Drawing e l'oggetto eseguirà il rendering delle linee diagonali.</span><span class="sxs-lookup"><span data-stu-id="23a21-118">When the message is handled, it will toggle a Boolean for rendering diagonals on the drawing object, and the object will then render the diagonal lines.</span></span>

<span data-ttu-id="23a21-119">Nel codice seguente viene illustrato il modo in cui i messaggi di movimento vengono passati al motore di movimento dal metodo WndProc.</span><span class="sxs-lookup"><span data-stu-id="23a21-119">The following code shows how gesture messages are passed to the gesture engine from the WndProc method.</span></span>

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

<span data-ttu-id="23a21-120">Il codice seguente illustra il modo in cui il motore di movimento gestisce il comando di tocco con due dita.</span><span class="sxs-lookup"><span data-stu-id="23a21-120">The following code shows how the gesture engine handles the two-finger tap command.</span></span>

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

<span data-ttu-id="23a21-121">Nel codice seguente viene illustrato il modo in cui l'oggetto Drawing commuta le diagonali.</span><span class="sxs-lookup"><span data-stu-id="23a21-121">The following code shows how the drawing object toggles its diagonals.</span></span>

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

<span data-ttu-id="23a21-122">Il codice seguente mostra come l'oggetto esegue il rendering delle linee diagonali nel metodo di disegnare.</span><span class="sxs-lookup"><span data-stu-id="23a21-122">The following code shows how the object renders diagonal lines in its draw method.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="23a21-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23a21-123">Related topics</span></span>

<span data-ttu-id="23a21-124">[Applicazione movimenti multitocco (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [applicazione movimenti multitocco (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [esempi di Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="23a21-124">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
