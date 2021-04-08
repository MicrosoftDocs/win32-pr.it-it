---
title: Come usare i controlli pager
description: In questa sezione viene descritto come implementare il controllo pager nell'applicazione.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bfff0c8d8097c4b0e861506bb73f55467b711
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047444"
---
# <a name="how-to-use-pager-controls"></a>Come usare i controlli pager

In questa sezione viene descritto come implementare il controllo pager nell'applicazione.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="initialize-a-pager-control"></a>Inizializzare un controllo pager

Per utilizzare il controllo pager, è necessario chiamare la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con il \_ \_ flag di classe PAGESCROLLER ICC impostato nel membro **dwICC** della struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .

### <a name="create-a-pager-control"></a>Creazione di un controllo pager

Usare [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o l'API [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo cercapersone. Il nome della classe per il controllo è [**WC \_ PAGESCROLLER**](common-control-window-classes.md), che è definito in commctrl. h. Lo [**stile \_ orizzontalmente PGS**](pager-control-styles.md) viene usato per creare un cercapersone orizzontale e lo stile [**di \_ PGS Vert**](pager-control-styles.md) viene usato per creare un cercapersone verticale. Poiché si tratta di un controllo figlio, deve essere utilizzato anche lo stile [**WS \_ figlio**](/windows/desktop/winmsg/window-styles) .

Dopo la creazione del controllo pager, è probabile che si desideri assegnare una finestra contenuta. Se la finestra contenuta è una finestra figlio, è necessario rendere la finestra figlio un elemento figlio del controllo cercapersone in modo che le dimensioni e la posizione vengano calcolate correttamente. La finestra viene quindi assegnata al controllo pager con il messaggio [**PGM \_ figlio**](pgm-setchild.md) . Tenere presente che questo messaggio non modifica effettivamente la finestra padre della finestra contenuta; assegna semplicemente la finestra contenuta. Se la finestra contenuta è uno dei controlli comuni, deve disporre dello stile [**CCS \_ noresize**](common-control-styles.md) per impedire che il controllo tenti di ridimensionarsi in base alle dimensioni del controllo cercapersone.

### <a name="process-pager-control-notifications"></a>Notifiche del controllo cercapersone del processo

Come minimo, è necessario elaborare la notifica di [ \_ CALCSIZE PGN](pgn-calcsize.md) . Se non si elabora questa notifica e si immette un valore per la larghezza o l'altezza, le frecce di scorrimento nel controllo pager non verranno visualizzate. Questo perché il controllo pager usa la larghezza o l'altezza fornite nella notifica PGN \_ CALCSIZE per determinare le dimensioni "ideali" della finestra contenuta.

Nell'esempio seguente viene illustrato come elaborare il caso di notifica [ \_ CALCSIZE di PGN](pgn-calcsize.md) . In questo esempio, la finestra contenuta è un controllo Toolbar che contiene un numero sconosciuto di pulsanti a una dimensione sconosciuta. Nell'esempio viene illustrato come utilizzare il messaggio [**TB \_ GETMAXSIZE**](tb-getmaxsize.md) per determinare le dimensioni di tutti gli elementi nella barra degli strumenti. Nell'esempio viene quindi inserita la larghezza di tutti gli elementi nel membro **larghezza** della struttura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) che viene passata alla notifica.


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

[Uso di controlli pager](using-pager-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 