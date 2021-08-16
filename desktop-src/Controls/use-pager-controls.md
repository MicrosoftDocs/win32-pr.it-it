---
title: Come usare i controlli pager
description: Questa sezione descrive come implementare il controllo pager nell'applicazione.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b917943f5f86498bb3cbea2c58842049c4618caf64a66a6b8db1cb2ab86a315b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828642"
---
# <a name="how-to-use-pager-controls"></a>Come usare i controlli pager

Questa sezione descrive come implementare il controllo pager nell'applicazione.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="initialize-a-pager-control"></a>Inizializzare un controllo Pager

Per usare il controllo pager, è necessario chiamare la [**funzione InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con il flag ICC PAGESCROLLER CLASS impostato nel membro \_ \_ **dwICC** della struttura [**INITCOMMONCONTROLSEX.**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)

### <a name="create-a-pager-control"></a>Creare un controllo Pager

Usare [**l'API CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo pager. Il nome della classe per il controllo [**è WC \_ PAGESCROLLER,**](common-control-window-classes.md)definito in Commctrl.h. Lo [**stile PGS \_ HORZ**](pager-control-styles.md) viene usato per creare un pager orizzontale e lo stile [**PGS \_ VERT**](pager-control-styles.md) viene usato per creare un pager verticale. Poiché si tratta di un controllo figlio, è necessario usare anche lo [**stile \_ WS CHILD.**](/windows/desktop/winmsg/window-styles)

Dopo aver creato il controllo pager, è molto probabile che si voglia assegnare una finestra indipendente. Se la finestra contenuta è una finestra figlio, è necessario impostare la finestra figlio come figlio del controllo pager in modo che le dimensioni e la posizione vengano calcolate correttamente. Assegnare quindi la finestra al controllo pager con il [**messaggio PGM \_ SETCHILD.**](pgm-setchild.md) Tenere presente che questo messaggio non modifica effettivamente la finestra padre della finestra contenuta. assegna semplicemente la finestra contenuta. Se la finestra contenuta è uno dei controlli comuni, deve avere lo stile [**\_ CCS NORESIZE**](common-control-styles.md) per impedire al controllo di tentare di ridimensionarsi in base alle dimensioni del controllo pager.

### <a name="process-pager-control-notifications"></a>Elaborare le notifiche del controllo Pager

Come minimo, è necessario elaborare la notifica [PGN \_ CALCSIZE.](pgn-calcsize.md) Se non si elabora questa notifica e si immette un valore per la larghezza o l'altezza, le frecce di scorrimento nel controllo pager non verranno visualizzate. Questo perché il controllo pager usa la larghezza o l'altezza fornita nella notifica PGN CALCSIZE per determinare le dimensioni \_ "ideali" della finestra contenuta.

L'esempio seguente illustra come elaborare il caso [di notifica \_ PGN CALCSIZE.](pgn-calcsize.md) In questo esempio la finestra contenuta è un controllo barra degli strumenti che contiene un numero sconosciuto di pulsanti di dimensioni sconosciute. L'esempio illustra come usare il messaggio [**\_ TB GETMAXSIZE**](tb-getmaxsize.md) per determinare le dimensioni di tutti gli elementi nella barra degli strumenti. L'esempio inserisce quindi la larghezza di tutti gli elementi nel membro **iWidth** della struttura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) passata alla notifica.


```C++
case PGN_SCROLL:{

    LPNMPGSCROLL pScroll = (LPNMPGSCROLL)lParam;
 
    switch(pScroll->iDir){
     
        case PGF_SCROLLLEFT:
        case PGF_SCROLLRIGHT:
        case PGF_SCROLLUP:
        case PGF_SCROLLDOWN:
     
            pScroll->iScroll = 20;
        
            break;
        }
    }
  
return 0;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli pager](using-pager-controls.md)
</dt> <dt>

[Windows di controlli comuni (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 