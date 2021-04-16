---
title: Come creare un controllo selezione data e ora
description: In questo argomento viene illustrato come creare dinamicamente un controllo di selezione data e ora (DTP).
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1253a2972b8d858a7440b3e472d5b3aa347b8175
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104224028"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a><span data-ttu-id="dbcbf-103">Come creare un controllo selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="dbcbf-103">How to Create a Date and Time Picker Control</span></span>

<span data-ttu-id="dbcbf-104">In questo argomento viene illustrato come creare dinamicamente un controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="dbcbf-104">This topic demonstrates how to dynamically create a date and time picker (DTP) control.</span></span> <span data-ttu-id="dbcbf-105">Nell'esempio di codice C++ associato viene creato un controllo DTP in una finestra di dialogo non modale.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-105">The accompanying C++ code example creates a DTP control in a modeless dialog box.</span></span> <span data-ttu-id="dbcbf-106">USA lo stile [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) per consentire all'utente di simulare la disattivazione della data all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-106">It uses the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style to enable the user to simulate deactivation of the date within the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="dbcbf-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="dbcbf-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="dbcbf-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="dbcbf-108">Technologies</span></span>

-   [<span data-ttu-id="dbcbf-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="dbcbf-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="dbcbf-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="dbcbf-110">Prerequisites</span></span>

-   <span data-ttu-id="dbcbf-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="dbcbf-111">C/C++</span></span>
-   <span data-ttu-id="dbcbf-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="dbcbf-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="dbcbf-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="dbcbf-113">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="dbcbf-114">Passaggio 1:</span><span class="sxs-lookup"><span data-stu-id="dbcbf-114">Step 1:</span></span>

<span data-ttu-id="dbcbf-115">Registrare la classe della finestra chiamando la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e specificando il \_ bit delle classi di data ICC \_ nella struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) associata.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-115">Register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the ICC\_DATE\_CLASSES bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a><span data-ttu-id="dbcbf-116">Passaggio 2:</span><span class="sxs-lookup"><span data-stu-id="dbcbf-116">Step 2:</span></span>

<span data-ttu-id="dbcbf-117">Per creare il controllo DTP, utilizzare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="dbcbf-117">To create the DTP control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="dbcbf-118">Specificare [**la \_ classe DATETIMEPICK**](common-control-window-classes.md) come classe della finestra e passare l'handle alla finestra di dialogo padre.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-118">Specify [**DATETIMEPICK\_CLASS**](common-control-window-classes.md) as the window class, and pass the handle to the parent dialog box.</span></span>

<span data-ttu-id="dbcbf-119">Nell'esempio di codice C++ riportato di seguito viene usata la funzione [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) per creare una finestra di dialogo non modale.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-119">The following C++ code example uses the [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) function to create a modeless dialog box.</span></span> <span data-ttu-id="dbcbf-120">Chiama quindi **CreateWindowEx** per creare il controllo DTP.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-120">It then calls **CreateWindowEx** to create the DTP control.</span></span>


```C++
  hwndDlg = CreateDialog  (g_hinst,
                           MAKEINTRESOURCE(IDD_DIALOG1),
                           hwndMain,
                           DlgProc);

  if(hwndDlg)
      hwndDP = CreateWindowEx(0,
                           DATETIMEPICK_CLASS,
                           TEXT("DateTime"),
                           WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                           20,50,220,20,
                           hwndDlg,
                           NULL,
                           g_hinst,
                           NULL);
```



## <a name="complete-example"></a><span data-ttu-id="dbcbf-121">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="dbcbf-121">Complete example</span></span>


```C++
//  CreateDatePick creates a DTP control within a dialog box.
//  Returns the handle to the new DTP control if successful, or NULL 
//  otherwise.
// 
//    hwndMain - The handle to the main window.
//    g_hinst  - global handle to the program instance.

HWND WINAPI CreateDatePick(HWND hwndMain)
{
    HWND hwndDP = NULL;
    HWND hwndDlg = NULL;

    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(icex);
    icex.dwICC = ICC_DATE_CLASSES;

    InitCommonControlsEx(&icex);

    hwndDlg = CreateDialog  (g_hinst,
                             MAKEINTRESOURCE(IDD_DIALOG1),
                             hwndMain,
                             DlgProc);

    if(hwndDlg)
        hwndDP = CreateWindowEx(0,
                             DATETIMEPICK_CLASS,
                             TEXT("DateTime"),
                             WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                             20,50,220,20,
                             hwndDlg,
                             NULL,
                             g_hinst,
                             NULL);

    return (hwndDP);
}

```



## <a name="related-topics"></a><span data-ttu-id="dbcbf-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dbcbf-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbcbf-123">Uso di controlli selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="dbcbf-123">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="dbcbf-124">Riferimento al controllo selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="dbcbf-124">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="dbcbf-125">Selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="dbcbf-125">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 