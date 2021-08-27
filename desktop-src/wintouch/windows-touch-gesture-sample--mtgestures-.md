---
title: Windows Esempio di movimento tocco (MTGestures)
description: Questa sezione descrive l'esempio Windows Movimento tocco.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
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
ms.openlocfilehash: 656b269eae779cd999680e165ba071d983d18526c2e9b873c5a916d61ccdb9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110586"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a>Windows Esempio di movimento tocco (MTGestures)

Questa sezione descrive l'esempio Windows Movimento tocco.

L'esempio Windows Touch Gesture illustra come usare i messaggi di movimento per tradurre, ruotare e ridimensionare una casella di cui viene eseguito il rendering da parte del Graphics Device Interface (GDI) gestendo il messaggio WM_GESTURE [**personalizzato.**](wm-gesture.md) La schermata seguente mostra l'aspetto dell'esempio quando è in esecuzione.

![Screenshot che mostra l'esempio di movimento tocco di Windows quando è in esecuzione, con un rettangolo bianco ruotato con contorni neri sullo schermo](images/mtgestures.png)

Per questo esempio, i messaggi di movimento vengono passati a un motore movimenti, che chiama quindi i metodi sugli oggetti di disegno per convertire, ruotare e ridimensionare un oggetto che dispone di metodi per la gestione di questi comandi. Per illustrare il funzionamento dell'esempio, prendere in considerazione la procedura per usare il comando tocco con due dita per abilitare o disabilitare le linee diagonali nella casella sottoposta a rendering. Un utente esegue il movimento di tocco con due dita, che genera un messaggio gestito dal programma. Quando il messaggio viene gestito, attiva o disattiva un valore booleano per il rendering delle diagonali sull'oggetto di disegno e l'oggetto esegue il rendering delle linee diagonali.

Il codice seguente illustra come i messaggi dei movimenti vengono passati al motore dei movimenti dal metodo WndProc.

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

Il codice seguente illustra come il motore dei movimenti gestisce il comando di tocco con due dita.

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

Il codice seguente illustra come l'oggetto di disegno attiva o disattiva le diagonali.

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

Il codice seguente illustra come l'oggetto esegue il rendering di linee diagonali nel relativo metodo di disegno.

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

[Applicazione Movimenti multitocchetto (C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS)Applicazione Movimenti [multitocchetto (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows touch](windows-touch-samples.md)
