---
title: Come creare controlli SysLink
description: I collegamenti ipertestuali del controllo SysLink vengono implementati attraverso il markup nella stringa di inizializzazione del controllo oppure tramite l'invio di un \_ messaggio di elemento.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa5c5ff3348f35f9c67cb34bea0cc495d403ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730655"
---
# <a name="how-to-create-syslink-controls"></a><span data-ttu-id="56165-103">Come creare controlli SysLink</span><span class="sxs-lookup"><span data-stu-id="56165-103">How to Create SysLink Controls</span></span>

<span data-ttu-id="56165-104">I collegamenti ipertestuali del controllo SysLink vengono implementati attraverso il markup nella stringa di inizializzazione del controllo oppure tramite l'invio di un messaggio di [**\_ elemento**](lm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="56165-104">You implement the SysLink control's hyperlinks through markup in the control's initialization string, or by sending it a [**LM\_SETITEM**](lm-setitem.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="56165-105">Prima di creare controlli SysLink, è necessario chiamare la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , specificando la \_ classe di collegamento ICC \_ .</span><span class="sxs-lookup"><span data-stu-id="56165-105">Before creating SysLink controls, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_LINK\_CLASS.</span></span>

 

<span data-ttu-id="56165-106">Per creare un SysLink, chiamare la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra di [**\_ collegamento WC**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="56165-106">To create a SysLink, call the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_LINK**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="56165-107">Il parametro *lpWindowName* comune a queste funzioni specifica un puntatore a una stringa con terminazione zero che contiene il testo contrassegnato per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="56165-107">The *lpWindowName* parameter that is common to these functions specifies a pointer to a zero-terminated string that contains the marked-up text to display.</span></span> <span data-ttu-id="56165-108">Per gli stili della finestra specifici dei controlli SysLink, vedere [stili di controllo Syslink](syslink-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="56165-108">For window styles particular to SysLink controls, see [SysLink Control Styles](syslink-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="56165-109">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="56165-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="56165-110">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="56165-110">Technologies</span></span>

-   [<span data-ttu-id="56165-111">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="56165-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="56165-112">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="56165-112">Prerequisites</span></span>

-   <span data-ttu-id="56165-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="56165-113">C/C++</span></span>
-   <span data-ttu-id="56165-114">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="56165-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="56165-115">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="56165-115">Instructions</span></span>

### <a name="create-a-syslink-control"></a><span data-ttu-id="56165-116">Creare un controllo SysLink</span><span class="sxs-lookup"><span data-stu-id="56165-116">Create a SysLink Control</span></span>

<span data-ttu-id="56165-117">Il codice di esempio seguente crea un controllo SysLink che visualizza due collegamenti ipertestuali.</span><span class="sxs-lookup"><span data-stu-id="56165-117">The following example code creates a SysLink control that displays two hyperlinks.</span></span> <span data-ttu-id="56165-118">Il primo collegamento ipertestuale è un URL Internet e il secondo è definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="56165-118">The first hyperlink is an Internet URL, and the second is application-defined.</span></span>


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a><span data-ttu-id="56165-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="56165-119">Remarks</span></span>

<span data-ttu-id="56165-120">Si presuppone che [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) sia già stato chiamato.</span><span class="sxs-lookup"><span data-stu-id="56165-120">It is assumed that [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) has already been called.</span></span>

<span data-ttu-id="56165-121">Specificando lo stile [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) si garantisce che l'utente sia in grado di selezionare un collegamento tramite tabulazione e premendo il tasto INVIO.</span><span class="sxs-lookup"><span data-stu-id="56165-121">Specifying the [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) style ensures that the user will be able to select a link by tabbing to it and pressing the Enter key.</span></span>

<span data-ttu-id="56165-122">La versione 6 di ComCtl32.dll supporta solo Unicode.</span><span class="sxs-lookup"><span data-stu-id="56165-122">Version 6 of ComCtl32.dll supports Unicode only.</span></span> <span data-ttu-id="56165-123">Pertanto, non è possibile creare versioni ANSI dei controlli SysLink, solo Unicode.</span><span class="sxs-lookup"><span data-stu-id="56165-123">Therefore, you cannot create ANSI versions of SysLink controls—only Unicode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56165-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56165-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56165-125">Uso di controlli SysLink</span><span class="sxs-lookup"><span data-stu-id="56165-125">Using SysLink Controls</span></span>](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

<span data-ttu-id="56165-126">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="56165-126">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 