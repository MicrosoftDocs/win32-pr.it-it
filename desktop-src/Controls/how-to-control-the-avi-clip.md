---
title: Come controllare il clip AVI
description: In questo argomento viene illustrato come utilizzare le macro di controllo dell'animazione per riprodurre, arrestare e chiudere un clip di Audio-Video Interleaved (AVI) associato.
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c11f7d8f519f98f3293d5be29fac0e0a40dd704
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474705"
---
# <a name="how-to-control-the-avi-clip"></a>Come controllare il clip AVI

In questo argomento viene illustrato come utilizzare le macro di controllo dell'animazione per riprodurre, arrestare e chiudere un clip di Audio-Video Interleaved (AVI) associato.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows
-   File AVI

## <a name="instructions"></a>Istruzioni


Creare una funzione che accetta come parametri un handle per il controllo dell'animazione e un flag che indica l'azione da eseguire sul clip AVI associato.

La funzione nell'esempio C++ seguente chiama una delle tre macro del controllo di animazione ([**animate \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**animate \_ Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**animate \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) in base al valore del parametro *nOutput azione* . L'handle per il controllo dell'animazione associato al clip AVI viene passato tramite il parametro *hwndAnim* .


```C++
// DoAnimation - plays, stops, or closes an animation control's 
//               AVI clip, depending on the value of an action flag. 
// hwndAnim    - handle to an animation control. 
// nAction     - flag that determines whether to play, stop, or close 
//               the AVI clip. 

void DoAnimation(HWND hwndAnim, int nAction) 
{ 
    int const PLAYIT = 1, STOPIT = 2, CLOSEIT = 3; 
    switch (nAction) { 
        case PLAYIT: 
         // Play the clip continuously starting with the 
         // first frame. 
            Animate_Play(hwndAnim, 0, -1, -1); 
            break; 

        case STOPIT: 
            Animate_Stop(hwndAnim); 
            break; 

        case CLOSEIT: 
            Animate_Close(hwndAnim); 
            break; 

        default: 
            break; 
    }
    
    return; 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli di animazione](animation-control-overview.md)
</dt> <dt>

[Riferimento al controllo Animation](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Uso di controlli di animazione](using-animation-control.md)
</dt> <dt>

[Controllo animazione](animation-control-reference.md)
</dt> </dl>

 

 




