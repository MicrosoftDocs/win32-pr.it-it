---
description: "Passaggio 4: Disegnare la bitmap nell'area client"
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: "Passaggio 4: Disegnare la bitmap nell'area client"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253e7d8a5b7508d5ae9f27195dbb7d59b30508ff2aacd8ec2713e0f4d6c909f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951790"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a>Passaggio 4: Disegnare la bitmap nell'area client

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Questo argomento è il passaggio 4 di [Grabbing a Poster Frame](grabbing-a-poster-frame.md).

Il passaggio finale consiste nel disegnare la bitmap nell'area client della finestra dell'applicazione usando la [**funzione SetDIBitsToDevice.**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) Questo esempio disegna semplicemente la bitmap nell'angolo superiore sinistro dell'area client, indipendentemente dalle dimensioni della finestra:


```C++
case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);
        if (pbmi)
        {
            int result = SetDIBitsToDevice(hdc, 0, 0, 
                pbmi->biWidth,
                pbmi->biHeight,
                0, 0, 0,
                pbmi->biHeight,
                pBuffer,
                reinterpret_cast<BITMAPINFO*>(pbmi),
                DIB_RGB_COLORS);
        }
        EndPaint(hwnd, &ps);
    }
    break;
```



Le *variabili pBuffer* *e pbmi* vengono dichiarate in [Passaggio 1:](step-1--create-the-windows-framework.md)Creare Windows Framework e i relativi valori vengono ottenuti in [Passaggio 3: Implementare](step-3--implement-the-frame-grabbing-function.md)la funzione Frame-Grabbing .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Afferrare un frame poster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
