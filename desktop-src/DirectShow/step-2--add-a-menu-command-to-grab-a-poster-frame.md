---
description: 'Passaggio 2: aggiungere un comando di menu per acquisire un frame di poster'
ms.assetid: 9a0f807b-5543-41d4-ad2a-030a4346131c
title: 'Passaggio 2: aggiungere un comando di menu per acquisire un frame di poster'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d049dc4e79197cfbe0a86b065eaf67a5ea567a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131890"
---
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a>Passaggio 2: aggiungere un comando di menu per acquisire un frame di poster

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Questo argomento è il passaggio 2 dell' [acquisizione di un frame di poster](grabbing-a-poster-frame.md).

Successivamente, aggiungere un comando per l'utente per acquisire un frame di poster da un file. Creare una voce di menu con un ID risorsa di \_ bitmap IDM e aggiungere l'istruzione case seguente alla routine della finestra:


```C++
case WM_COMMAND:
    switch (LOWORD(wparam))
    {
    case IDM_BITMAP:
        {
            HRESULT hr = DoShowBitmap(hwnd, &pbmi);
            if (SUCCEEDED(hr))
            {
                pBuffer = reinterpret_cast<BYTE*>(pbmi) + 
                    sizeof(BITMAPINFOHEADER);
                InvalidateRect(hwnd, NULL, TRUE);
            }
            else
            {
                MessageBox(hwnd, TEXT("Cannot display the image."),
                    TEXT("Error"), MB_OK | MB_ICONERROR);
            }
        }
        break;  // IDM_BITMAP
    }
    break;  // WM_COMMAND
```



La funzione DoShowBitmap restituirà il buffer allocato in *PBMI*. Supponendo che la funzione abbia esito positivo, l'indirizzo della bitmap (


```C++
pBuffer
```



) può essere calcolato come offset da *PBMI*. Nella funzione DoShowBitmap, visualizzare una finestra di dialogo **Apri file** che consente all'utente di scegliere un file e quindi chiamare la funzione GetBitmap definita dall'applicazione, che recupererà la bitmap:


```C++
HRESULT DoShowBitmap(HWND hwnd, BITMAPINFOHEADER** ppbmih)
{
    OPENFILENAME ofn;       // common dialog box structure
    // Initialize OPENFILENAME (not shown).
    // Display the Open File dialog box.  
    if (GetOpenFileName(&ofn) != TRUE) // failed to open file
    {
        return E_FAIL;
    }
    return GetBitmap(ofn.lpstrFile, ppbmih);
}
```



[Passaggio 3: implementare la funzione Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di un frame di poster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



