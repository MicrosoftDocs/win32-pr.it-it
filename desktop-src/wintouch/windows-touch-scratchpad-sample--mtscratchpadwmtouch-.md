---
title: Esempio di Windows Touch temporanei (C++)
description: Nell'esempio Windows Touch temporanei viene illustrato come utilizzare i messaggi Windows Touch per tracciare le tracce dei punti di tocco in una finestra.
ms.assetid: 6c4b4595-1e95-499c-b045-b5ae01aa5a6e
keywords:
- Windows Touch, esempi di codice
- Windows Touch, codice di esempio
- Windows Touch, esempi temporanei
- Esempi di temporanei
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: afdd39e886d97671942b4ff67a74c0da75924fbb
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047562"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Esempio di Windows Touch temporanei (C++)

Nell' [esempio Windows Touch temporanei](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) viene illustrato come utilizzare i messaggi Windows Touch per tracciare le tracce dei punti di tocco in una finestra. La traccia del dito principale, quella che è stata inserita prima sul digitalizzatore, viene disegnata in nero. Le dita secondarie sono disegnate in sei colori: rosso, verde, blu, ciano, magenta e giallo. Nell'immagine seguente viene illustrato l'aspetto dell'applicazione durante l'esecuzione.

![screenshot che mostra il temporanei Windows Touch con controllo ortografia durante rosso e nero sullo schermo](images/mtscratchpadwmtouch.png)

Per questa applicazione, la finestra viene registrata come finestra di tocco, i messaggi di tocco vengono interpretati per aggiungere punti di tocco agli oggetti Stroke e il rendering dei tratti di input penna viene eseguito sullo schermo nel gestore di messaggi **WM_PAINT** .

Il codice seguente illustra come la finestra viene registrata come finestra di tocco.

```C++
    // Register application window for receiving multitouch input. Use default settings.
    if(!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multitouch input", L"Error", MB_OK);
        return FALSE;
    }
```

Il codice seguente illustra come vengono usati i messaggi di tocco per aggiungere punti di tocco ai tratti di input penna.

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

Nel codice seguente viene illustrato come vengono disegnati i tratti di input penna sullo schermo nel gestore di messaggi **WM_PAINT** .

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

Il codice seguente mostra come l'oggetto Stroke esegue il rendering dei tratti sullo schermo.

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

[Windows Touch temporanei Sample (C#)](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md), [applicazione temporanei multitocco (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [applicazione temporanei multitocco (WM_TOUCH/C + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), esempi di [Windows Touch](windows-touch-samples.md)
