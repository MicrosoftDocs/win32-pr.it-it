---
description: 'Passaggio 1: creare il Framework Windows'
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 'Passaggio 1: creare il Framework Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff1712f631db520ff30065e8943d13b280f3d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314410"
---
# <a name="step-1-create-the-windows-framework"></a>Passaggio 1: creare il Framework Windows

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Iniziare creando il Framework di base di un'applicazione Windows, tra cui WinMain e una procedura di finestra. La funzione WinMain non è riportata di seguito. chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) prima del ciclo di messaggi per inizializzare la libreria com e [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) dopo la chiusura del ciclo di messaggi. Iniziare con la procedura minima della finestra seguente:


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



Quando si recupera un frame di poster dal rilevatore multimediale, viene restituito un buffer che contiene una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguita dai bit dell'immagine. Definire quindi due variabili statiche nella procedura della finestra: *PBMI* conterrà un puntatore alla struttura **BITMAPINFOHEADER** e *pbuffer* conterrà un puntatore alla bitmap. Tramite l'applicazione verrà allocato il buffer in *PBMI* utilizzando `new` , quindi è necessario eliminare il buffer prima che la finestra venga distrutta. Il puntatore *pbuffer* viene calcolato come offset da *PBMI*, pertanto non è necessario eliminarlo.

[Passaggio 2: aggiungere un comando di menu per acquisire un frame di poster](step-2--add-a-menu-command-to-grab-a-poster-frame.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di un frame di poster](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
