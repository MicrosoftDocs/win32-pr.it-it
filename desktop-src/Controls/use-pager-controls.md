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
# <a name="how-to-use-pager-controls"></a><span data-ttu-id="db86d-103">Come usare i controlli pager</span><span class="sxs-lookup"><span data-stu-id="db86d-103">How to Use Pager Controls</span></span>

<span data-ttu-id="db86d-104">In questa sezione viene descritto come implementare il controllo pager nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="db86d-104">This section describes how to implement the pager control in your application.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="db86d-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="db86d-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="db86d-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="db86d-106">Technologies</span></span>

-   [<span data-ttu-id="db86d-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="db86d-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="db86d-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="db86d-108">Prerequisites</span></span>

-   <span data-ttu-id="db86d-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="db86d-109">C/C++</span></span>
-   <span data-ttu-id="db86d-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="db86d-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="db86d-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="db86d-111">Instructions</span></span>

### <a name="initialize-a-pager-control"></a><span data-ttu-id="db86d-112">Inizializzare un controllo pager</span><span class="sxs-lookup"><span data-stu-id="db86d-112">Initialize a Pager Control</span></span>

<span data-ttu-id="db86d-113">Per utilizzare il controllo pager, è necessario chiamare la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con il \_ \_ flag di classe PAGESCROLLER ICC impostato nel membro **dwICC** della struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="db86d-113">To use the pager control, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function with the ICC\_PAGESCROLLER\_CLASS flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

### <a name="create-a-pager-control"></a><span data-ttu-id="db86d-114">Creazione di un controllo pager</span><span class="sxs-lookup"><span data-stu-id="db86d-114">Create a Pager Control</span></span>

<span data-ttu-id="db86d-115">Usare [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o l'API [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo cercapersone.</span><span class="sxs-lookup"><span data-stu-id="db86d-115">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) API to create a pager control.</span></span> <span data-ttu-id="db86d-116">Il nome della classe per il controllo è [**WC \_ PAGESCROLLER**](common-control-window-classes.md), che è definito in commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="db86d-116">The class name for the control is [**WC\_PAGESCROLLER**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="db86d-117">Lo [**stile \_ orizzontalmente PGS**](pager-control-styles.md) viene usato per creare un cercapersone orizzontale e lo stile [**di \_ PGS Vert**](pager-control-styles.md) viene usato per creare un cercapersone verticale.</span><span class="sxs-lookup"><span data-stu-id="db86d-117">The [**PGS\_HORZ**](pager-control-styles.md) style is used to create a horizontal pager, and the [**PGS\_VERT**](pager-control-styles.md) style is used to create a vertical pager.</span></span> <span data-ttu-id="db86d-118">Poiché si tratta di un controllo figlio, deve essere utilizzato anche lo stile [**WS \_ figlio**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="db86d-118">Because this is a child control, the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style should also be used.</span></span>

<span data-ttu-id="db86d-119">Dopo la creazione del controllo pager, è probabile che si desideri assegnare una finestra contenuta.</span><span class="sxs-lookup"><span data-stu-id="db86d-119">After the pager control is created, you will most likely want to assign a contained window to it.</span></span> <span data-ttu-id="db86d-120">Se la finestra contenuta è una finestra figlio, è necessario rendere la finestra figlio un elemento figlio del controllo cercapersone in modo che le dimensioni e la posizione vengano calcolate correttamente.</span><span class="sxs-lookup"><span data-stu-id="db86d-120">If the contained window is a child window, you should make the child window a child of the pager control so that the size and position will be calculated correctly.</span></span> <span data-ttu-id="db86d-121">La finestra viene quindi assegnata al controllo pager con il messaggio [**PGM \_ figlio**](pgm-setchild.md) .</span><span class="sxs-lookup"><span data-stu-id="db86d-121">You then assign the window to the pager control with the [**PGM\_SETCHILD**](pgm-setchild.md) message.</span></span> <span data-ttu-id="db86d-122">Tenere presente che questo messaggio non modifica effettivamente la finestra padre della finestra contenuta; assegna semplicemente la finestra contenuta.</span><span class="sxs-lookup"><span data-stu-id="db86d-122">Be aware that this message does not actually change the parent window of the contained window; it simply assigns the contained window.</span></span> <span data-ttu-id="db86d-123">Se la finestra contenuta è uno dei controlli comuni, deve disporre dello stile [**CCS \_ noresize**](common-control-styles.md) per impedire che il controllo tenti di ridimensionarsi in base alle dimensioni del controllo cercapersone.</span><span class="sxs-lookup"><span data-stu-id="db86d-123">If the contained window is one of the common controls, it must have the [**CCS\_NORESIZE**](common-control-styles.md) style to prevent the control from attempting to resize itself to the pager control's size.</span></span>

### <a name="process-pager-control-notifications"></a><span data-ttu-id="db86d-124">Notifiche del controllo cercapersone del processo</span><span class="sxs-lookup"><span data-stu-id="db86d-124">Process Pager Control Notifications</span></span>

<span data-ttu-id="db86d-125">Come minimo, è necessario elaborare la notifica di [ \_ CALCSIZE PGN](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="db86d-125">At a minimum, it is necessary to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification.</span></span> <span data-ttu-id="db86d-126">Se non si elabora questa notifica e si immette un valore per la larghezza o l'altezza, le frecce di scorrimento nel controllo pager non verranno visualizzate.</span><span class="sxs-lookup"><span data-stu-id="db86d-126">If you do not process this notification and enter a value for the width or height, the scroll arrows in the pager control will not be displayed.</span></span> <span data-ttu-id="db86d-127">Questo perché il controllo pager usa la larghezza o l'altezza fornite nella notifica PGN \_ CALCSIZE per determinare le dimensioni "ideali" della finestra contenuta.</span><span class="sxs-lookup"><span data-stu-id="db86d-127">This is because the pager control uses the width or height supplied in the PGN\_CALCSIZE notification to determine the "ideal" size of the contained window.</span></span>

<span data-ttu-id="db86d-128">Nell'esempio seguente viene illustrato come elaborare il caso di notifica [ \_ CALCSIZE di PGN](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="db86d-128">The following example demonstrates how to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification case.</span></span> <span data-ttu-id="db86d-129">In questo esempio, la finestra contenuta è un controllo Toolbar che contiene un numero sconosciuto di pulsanti a una dimensione sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="db86d-129">In this example, the contained window is a toolbar control that contains an unknown number of buttons at an unknown size.</span></span> <span data-ttu-id="db86d-130">Nell'esempio viene illustrato come utilizzare il messaggio [**TB \_ GETMAXSIZE**](tb-getmaxsize.md) per determinare le dimensioni di tutti gli elementi nella barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="db86d-130">The example shows how to use the [**TB\_GETMAXSIZE**](tb-getmaxsize.md) message to determine the size of all of the items in the toolbar.</span></span> <span data-ttu-id="db86d-131">Nell'esempio viene quindi inserita la larghezza di tutti gli elementi nel membro **larghezza** della struttura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) che viene passata alla notifica.</span><span class="sxs-lookup"><span data-stu-id="db86d-131">The example then places the width of all of the items into the **iWidth** member of the [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that is passed to the notification.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="db86d-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db86d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db86d-133">Uso di controlli pager</span><span class="sxs-lookup"><span data-stu-id="db86d-133">Using Pager Controls</span></span>](using-pager-controls.md)
</dt> <dt>

<span data-ttu-id="db86d-134">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="db86d-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 