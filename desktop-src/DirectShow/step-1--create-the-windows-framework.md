---
description: 'Passaggio 1: Creare Windows Framework'
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 'Passaggio 1: Creare Windows Framework'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feba710c8df948e34c0da0ca9e7a1de85622bfae462290cbce3f36777854cb6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072515"
---
# <a name="step-1-create-the-windows-framework"></a>Passaggio 1: Creare Windows Framework

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Per iniziare, creare il framework di base di un'Windows, tra cui WinMain e una routine della finestra. La funzione WinMain non viene visualizzata qui. Chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) prima del ciclo di messaggi per inizializzare la libreria COM e [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) dopo la chiusura del ciclo di messaggi. Iniziare con la procedura di finestra minima seguente:


```C++
LRESULT CALLBACK MainWndProc(HWND hwnd, UINT msg, WPARAM wparam, LPARAM lparam)
{
    static BITMAPINFOHEADER *pbmi = NULL;
    static BYTE *pBuffer = NULL;
    switch (msg)
    {
    case WM_CLOSE:
        DestroyWindow(hwnd);
        break;
    case WM_DESTROY:
        if (pbmi) delete [] pbmi;
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hwnd, msg, wparam, lparam);
    }
    return 0;
}
```



Quando si recupera un frame poster da Media Detector, restituisce un buffer contenente una [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguita dai bit dell'immagine. Definire quindi due variabili statiche nella routine della finestra: *pbmi* contenerà un puntatore alla struttura **BITMAPINFOHEADER** e *pBuffer* contenerà un puntatore alla bitmap. L'applicazione alloca il buffer in *pbmi* usando , quindi deve eliminare il buffer prima che `new` la finestra venga distrutta definitivamente. Il *puntatore pBuffer* viene calcolato come offset da *pbmi,* quindi non è necessario eliminarlo.

Passaggio [2: Aggiungere un comando di menu per afferrare un frame poster](step-2--add-a-menu-command-to-grab-a-poster-frame.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Afferrare un frame poster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
