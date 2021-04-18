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
# <a name="step-1-create-the-windows-framework"></a><span data-ttu-id="9913e-103">Passaggio 1: creare il Framework Windows</span><span class="sxs-lookup"><span data-stu-id="9913e-103">Step 1: Create the Windows Framework</span></span>

<span data-ttu-id="9913e-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="9913e-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9913e-105">Iniziare creando il Framework di base di un'applicazione Windows, tra cui WinMain e una procedura di finestra.</span><span class="sxs-lookup"><span data-stu-id="9913e-105">Start by creating the basic framework of a Windows application, including WinMain and a window procedure.</span></span> <span data-ttu-id="9913e-106">La funzione WinMain non è riportata di seguito. chiamare [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) prima del ciclo di messaggi per inizializzare la libreria com e [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) dopo la chiusura del ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="9913e-106">The WinMain function is not shown here; call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before the message loop to initialize the COM library, and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) after the message loop exits.</span></span> <span data-ttu-id="9913e-107">Iniziare con la procedura minima della finestra seguente:</span><span class="sxs-lookup"><span data-stu-id="9913e-107">Start with the following minimal window procedure:</span></span>


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



<span data-ttu-id="9913e-108">Quando si recupera un frame di poster dal rilevatore multimediale, viene restituito un buffer che contiene una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguita dai bit dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="9913e-108">When you retrieve a poster frame from the Media Detector, it returns a buffer that contains a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the image bits.</span></span> <span data-ttu-id="9913e-109">Definire quindi due variabili statiche nella procedura della finestra: *PBMI* conterrà un puntatore alla struttura **BITMAPINFOHEADER** e *pbuffer* conterrà un puntatore alla bitmap.</span><span class="sxs-lookup"><span data-stu-id="9913e-109">Therefore, define two static variables in the window procedure: *pbmi* will hold a pointer to the **BITMAPINFOHEADER** structure, and *pBuffer* will hold a pointer to the bitmap.</span></span> <span data-ttu-id="9913e-110">Tramite l'applicazione verrà allocato il buffer in *PBMI* utilizzando `new` , quindi è necessario eliminare il buffer prima che la finestra venga distrutta.</span><span class="sxs-lookup"><span data-stu-id="9913e-110">The application will allocate the buffer in *pbmi* using `new`, so it must delete the buffer before the window is destroyed.</span></span> <span data-ttu-id="9913e-111">Il puntatore *pbuffer* viene calcolato come offset da *PBMI*, pertanto non è necessario eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="9913e-111">The *pBuffer* pointer is calculated as an offset from *pbmi*, so there is no need to delete it.</span></span>

<span data-ttu-id="9913e-112">[Passaggio 2: aggiungere un comando di menu per acquisire un frame di poster](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span><span class="sxs-lookup"><span data-stu-id="9913e-112">Next: [Step 2: Add a Menu Command to Grab a Poster Frame](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="9913e-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9913e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9913e-114">Acquisizione di un frame di poster</span><span class="sxs-lookup"><span data-stu-id="9913e-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
