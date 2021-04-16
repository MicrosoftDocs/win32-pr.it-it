---
description: "Passaggio 4: creare la bitmap nell'area client"
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: "Passaggio 4: creare la bitmap nell'area client"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4975215e5d75de9909f029a3378bd6cc8bc60916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401806"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a>Passaggio 4: creare la bitmap nell'area client

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Questo argomento è il passaggio 4 dell' [acquisizione di un frame di poster](grabbing-a-poster-frame.md).

Il passaggio finale consiste nel creare la bitmap nell'area client della finestra dell'applicazione, usando la funzione [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) . In questo esempio la bitmap viene semplicemente disegnata nell'angolo superiore sinistro dell'area client, indipendentemente dalle dimensioni della finestra:


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



Le variabili *pbuffer* e *PBMI* sono dichiarate nel [passaggio 1: creare il Framework Windows](step-1--create-the-windows-framework.md)e i relativi valori vengono ottenuti nel [passaggio 3: implementare la funzione Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di un frame di poster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
