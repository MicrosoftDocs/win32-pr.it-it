---
title: Come creare un controllo di animazione
description: In questo argomento viene illustrato come creare un controllo di animazione.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ff190617996e42e6580b82311fb51f4248000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044336"
---
# <a name="how-to-create-an-animation-control"></a>Come creare un controllo di animazione

In questo argomento viene illustrato come creare un controllo di animazione. Nell'esempio di codice C++ associato viene creato un controllo Animation in una finestra di dialogo. Posiziona il controllo animazione sotto un controllo specificato e imposta le dimensioni del controllo animazione in base alle dimensioni di un frame nell'Audio-Video clip con interfoliazione (AVI).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows
-   File AVI

## <a name="instructions"></a>Istruzioni

### <a name="step-1-create-an-instance-of-the-animation-control"></a>Passaggio 1: creare un'istanza del controllo Animation.

Utilizzare la macro [**animazione \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) per creare un'istanza del controllo Animation.


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a>Passaggio 2: posizionare il controllo dell'animazione.

Ottiene le coordinate dello schermo del pulsante di controllo specificato.


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



Converte le coordinate dell'angolo inferiore sinistro in coordinate client.


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



Posizionare il controllo animazione sotto il pulsante di controllo specificato.


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a>Passaggio 3: aprire il clip AVI.

Chiamare la macro [**\_ Apri animazione**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) per aprire il clip AVI e visualizzare il primo fotogramma del controllo Animation. Chiamare la funzione **ShowWindow** per rendere visibile il controllo dell'animazione.


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

[Riferimento al controllo Animation](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Uso di controlli di animazione](using-animation-control.md)
</dt> <dt>

[Animazione](animation-control-reference.md)
</dt> </dl>

 

 




