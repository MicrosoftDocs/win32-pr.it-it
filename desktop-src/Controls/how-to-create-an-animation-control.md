---
title: Come creare un controllo di animazione
description: Questo argomento illustra come creare un controllo di animazione.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8117d7c9393a828786532bd3d3fbfcf4f4eaaf6bb1bfdccdc5a2f97fa1c5cb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435821"
---
# <a name="how-to-create-an-animation-control"></a>Come creare un controllo di animazione

Questo argomento illustra come creare un controllo di animazione. L'esempio di codice C++ associato crea un controllo di animazione in una finestra di dialogo. Posiziona il controllo di animazione sotto un controllo specificato e imposta le dimensioni del controllo di animazione in base alle dimensioni di un frame nel clip Audio-Video Interleaved (AVI).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione
-   File AVI

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-an-instance-of-the-animation-control"></a>Passaggio 1: Creare un'istanza del controllo di animazione.

Usare la macro [**Animate \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) per creare un'istanza del controllo di animazione.


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a>Passaggio 2: Posizionare il controllo di animazione.

Ottiene le coordinate dello schermo del pulsante di controllo specificato.


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



Convertire le coordinate dell'angolo inferiore sinistro in coordinate client.


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



Posizionare il controllo di animazione sotto il pulsante di controllo specificato.


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a>Passaggio 3: Aprire il clip AVI.

Chiamare la macro [**Animate \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) per aprire il clip AVI e visualizzare il primo fotogramma nel controllo di animazione. Chiamare la **funzione ShowWindow** per rendere visibile il controllo di animazione.


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a>Esempio completo


```C++
// CreateAnimationCtrl - creates an animation control, positions it 
//                       below the specified control in a dialog box, 
//                       and opens the AVI clip for the animation control. 
// Returns the handle to the animation control. 
// hwndDlg             - handle to the dialog box. 
// nIDCtl              - identifier of the control below which the animation control 
//                       is to be positioned. 
// 
// Constants 
//     IDC_ANIMATE - identifier of the animation control. 
//     CX_FRAME, CY_FRAME - width and height of the frames 
//     in the AVI clip. 

HWND CreateAnimationCtrl(HWND hwndDlg, int nIDCtl) 
{ 
    HWND hwndAnim = NULL;    
    
    // Create the animation control.
    // IDC_ANIMATE - identifier of the animation control. 
    // hwndDlg - handle to the dialog box.
    RECT rc;
    hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
        WS_BORDER | WS_CHILD, g_hinst); 

    // Get the screen coordinates of the specified control button.
    // nIDCtl - identifier of the control below which the animation control is to be positioned.
    GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 

    // Convert the coordinates of the lower-left corner to 
    // client coordinates.
    POINT pt;
    pt.x = rc.left; 
    pt.y = rc.bottom; 
    ScreenToClient(hwndDlg, &pt); 

    // Position the animation control below the Stop button.
    // CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
    SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
        CX_FRAME, CY_FRAME, 
        SWP_NOZORDER | SWP_DRAWFRAME);

    // Open the AVI clip, and show the animation control.
    Animate_Open(hwndAnim, "SEARCH.AVI"); 
    ShowWindow(hwndAnim, SW_SHOW); 

    return hwndAnim; 
} 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli di animazione](animation-control-overview.md)
</dt> <dt>

[Informazioni di riferimento sul controllo Animation](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Uso dei controlli di animazione](using-animation-control.md)
</dt> <dt>

[Animazione](animation-control-reference.md)
</dt> </dl>

 

 




