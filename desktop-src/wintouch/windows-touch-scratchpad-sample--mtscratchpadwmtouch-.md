---
title: Windows Esempio di Touch Scratchpad (C++)
description: L'Windows touch scratchpad illustra come usare i messaggi Windows Touch per disegnare tracce dei punti di tocco in una finestra.
ms.assetid: 6c4b4595-1e95-499c-b045-b5ae01aa5a6e
keywords:
- Windows Tocco, esempi di codice
- Windows Tocco, codice di esempio
- Windows Esempi di Touch,Scratchpad
- Esempi di Scratchpad
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 7f3be8c120a935bc1a8d65dfdd8c7ab9894e0360d3415e8c645e5b3afae87012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086252"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Windows Esempio di Touch Scratchpad (C++)

[L'Windows touch scratchpad](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) illustra come usare i messaggi Windows Touch per disegnare tracce dei punti di tocco in una finestra. La traccia del dito principale, quella che è stata inserita per prima sul digitalizzatore, viene disegnata in nero. Le dita secondarie vengono disegnate in altri sei colori: rosso, verde, blu, ciano, magenta e giallo. L'immagine seguente mostra l'aspetto dell'applicazione durante l'esecuzione.

![Screenshot che mostra il touch scratchpad di Windows, con linee a righe rosse e nere sullo schermo](images/mtscratchpadwmtouch.png)

Per questa applicazione, la finestra viene registrata come finestra di tocco, i messaggi di tocco vengono interpretati per aggiungere punti tocco agli oggetti tratto e viene eseguito il rendering dei tratti input penna sullo schermo nel gestore di messaggi **WM_PAINT.**

Il codice seguente illustra come la finestra viene registrata come finestra di tocco.

```C++
    // Register application window for receiving multitouch input. Use default settings.
    if(!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multitouch input", L"Error", MB_OK);
        return FALSE;
    }
```

Il codice seguente illustra come vengono usati i messaggi di tocco per aggiungere punti di tocco ai tratti input penna.

```C++
        // WM_TOUCH message handlers
        case WM_TOUCH:
            {
                // WM_TOUCH message can contain several messages from different contacts
                // packed together.
                // Message parameters need to be decoded:
                unsigned int numInputs = (unsigned int) wParam; // Number of actual per-contact messages
                TOUCHINPUT* ti = new TOUCHINPUT[numInputs]; // Allocate the storage for the parameters of the per-contact messages
                if(ti == NULL)
                {
                    break;
                }
                // Unpack message parameters into the array of TOUCHINPUT structures, each
                // representing a message for one single contact.
                if(GetTouchInputInfo((HTOUCHINPUT)lParam, numInputs, ti, sizeof(TOUCHINPUT)))
                {
                    // For each contact, dispatch the message to the appropriate message
                    // handler.
                    for(unsigned int i=0; i<numInputs; ++i)
                    {
                        if(ti[i].dwFlags & TOUCHEVENTF_DOWN)
                        {
                            OnTouchDownHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_MOVE)
                        {
                            OnTouchMoveHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_UP)
                        {
                            OnTouchUpHandler(hWnd, ti[i]);
                        }
                    }
                }
                CloseTouchInputHandle((HTOUCHINPUT)lParam);
                delete [] ti;
            }
            break;
```

Il codice seguente illustra come i tratti input penna vengono disegnati sullo schermo nel **WM_PAINT** di messaggi.

```C++
        case WM_PAINT:
            hdc = BeginPaint(hWnd, &ps);
            // Full redraw: draw complete collection of finished strokes and
            // also all the strokes that are currently in drawing.
            g_StrkColFinished.Draw(hdc);
            g_StrkColDrawing.Draw(hdc);
            EndPaint(hWnd, &ps);
            break;
```

Il codice seguente illustra come l'oggetto stroke esegue il rendering dei tratti sullo schermo.

```C++
void CStroke::Draw(HDC hDC) const
{
    if(m_nCount < 2)
    {
        return;
    }

    HPEN hPen = CreatePen(PS_SOLID, 3, m_clr);
    HGDIOBJ hOldPen = SelectObject(hDC, hPen);
    Polyline(hDC, m_arrData, m_nCount);
    SelectObject(hDC, hOldPen);
    DeleteObject(hPen);
}
```

## <a name="related-topics"></a>Argomenti correlati

[Windows Touch Scratchpad (C#)](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md), [Multi-Touch Scratchpad Application (WM_TOUCH/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [Multi-Touch Scratchpad Application (WM_TOUCH/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [Windows Touch Samples](windows-touch-samples.md)
