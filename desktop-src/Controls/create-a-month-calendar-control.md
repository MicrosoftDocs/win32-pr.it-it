---
title: Come creare un controllo calendario mensile
description: In questo argomento viene illustrato come creare dinamicamente un controllo calendario mensile utilizzando la funzione CreateWindowEx.
ms.assetid: 35ADDA85-5D7D-46F4-A637-99FEE4592B3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f3824618e9801b68eb67b13c64c638a5057481
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734914"
---
# <a name="how-to-create-a-month-calendar-control"></a><span data-ttu-id="14264-103">Come creare un controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="14264-103">How to Create a Month Calendar Control</span></span>

<span data-ttu-id="14264-104">In questo argomento viene illustrato come creare dinamicamente un controllo calendario mensile utilizzando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="14264-104">This topic demonstrates how to dynamically create a month calendar control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="14264-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="14264-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="14264-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="14264-106">Technologies</span></span>

-   [<span data-ttu-id="14264-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="14264-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="14264-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="14264-108">Prerequisites</span></span>

-   <span data-ttu-id="14264-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="14264-109">C/C++</span></span>
-   <span data-ttu-id="14264-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="14264-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="14264-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="14264-111">Instructions</span></span>


<span data-ttu-id="14264-112">Per creare un controllo calendario mensile, usare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la [**\_ classe MONTHCAL**](common-control-window-classes.md) come classe Window.</span><span class="sxs-lookup"><span data-stu-id="14264-112">To create a month calendar control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying [**MONTHCAL\_CLASS**](common-control-window-classes.md) as the window class.</span></span> <span data-ttu-id="14264-113">È necessario prima registrare la classe della finestra chiamando la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , specificando il bit delle **\_ \_ classi di data ICC** nella struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) associata.</span><span class="sxs-lookup"><span data-stu-id="14264-113">You must first register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the **ICC\_DATE\_CLASSES** bit in the accompanying [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

<span data-ttu-id="14264-114">Nell'esempio seguente viene illustrato come creare un controllo calendario mensile in una finestra di dialogo non modale esistente.</span><span class="sxs-lookup"><span data-stu-id="14264-114">The following example demonstrates how to create a month calendar control in an existing modeless dialog box.</span></span> <span data-ttu-id="14264-115">Si noti che i valori delle dimensioni passati a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) sono tutti zeri.</span><span class="sxs-lookup"><span data-stu-id="14264-115">Note that the size values passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) are all zeros.</span></span> <span data-ttu-id="14264-116">Poiché la dimensione minima richiesta dipende dal tipo di carattere utilizzato dal controllo, nell'esempio viene utilizzata la macro [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) per richiedere informazioni sulle dimensioni e quindi ridimensionare il controllo chiamando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="14264-116">Because the minimum required size depends on the font that the control uses, the example uses the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro to request size information and then resizes the control by calling [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="14264-117">Se successivamente si modifica il tipo di carattere con [**WM \_ sefont**](/windows/desktop/winmsg/wm-setfont), le dimensioni del controllo non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="14264-117">If you subsequently change the font with [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont), the dimensions of the control will not change.</span></span> <span data-ttu-id="14264-118">È necessario chiamare di nuovo **MonthCal \_ GetMinReqRect** e ridimensionare il controllo in modo da adattarlo al nuovo tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="14264-118">You must call **MonthCal\_GetMinReqRect** again and resize the control to fit the new font.</span></span>



```C++
// Child window identifier of the month calendar.
#define IDC_MONTHCAL 101

// Symbols used by SetWindowPos function (arbitrary values).
#define LEFT 35
#define TOP  40

// Description:
//   Creates a month calendar control in a dialog box.  
// Parameters:
//   hwndOwner - handle of the owner window.
// Nonlocal variables:
//   MonthCalDlgProc - window procedure of the dialog box that 
//     contains the month calendar.
//   g_hInst - global instance handle.
//
HRESULT CreateMonthCalDialog(HWND hwndOwner)
{
    RECT rc;
    INITCOMMONCONTROLSEX icex;
    HWND hwndDlg = NULL;
    HWND hwndMonthCal = NULL;

    // Return an error code if the owner handle is invalid.
    if (hwndOwner == NULL)
        return E_INVALIDARG;

    // Load the window class.
    icex.dwSize = sizeof(icex);
    icex.dwICC  = ICC_DATE_CLASSES;
    InitCommonControlsEx(&icex);

    // Create a modeless dialog box to hold the control.
    hwndDlg = CreateDialog(g_hInst,
                    MAKEINTRESOURCE(IDD_DATE_PICKER),
                    hwndOwner,
                    MonthCalDlgProc);
   
    // Return if creating the dialog box failed. 
    if (hwndDlg == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                        
    // Create the month calendar.
    hwndMonthCal  = CreateWindowEx(0,
                    MONTHCAL_CLASS,
                    L"",
                    WS_BORDER | WS_CHILD | WS_VISIBLE | MCS_DAYSTATE,
                    0,0,0,0, // resize it later
                    hwndDlg,
                    (HMENU) IDC_MONTHCAL,
                    g_hInst,
                    NULL);

    // Return if creating the month calendar failed. 
    if (hwndMonthCal == NULL)
        return HRESULT_FROM_WIN32(GetLastError()); 
                     
    // Get the size required to show an entire month.
    MonthCal_GetMinReqRect(hwndMonthCal, &rc);

    // Resize the control now that the size values have been obtained.
    SetWindowPos(hwndMonthCal, NULL, LEFT, TOP, 
        rc.right, rc.bottom, SWP_NOZORDER);

    // Set the calendar to the annual view.
    MonthCal_SetCurrentView(hwndMonthCal, MCMV_YEAR);

    // Make the window visible.
    ShowWindow(hwndDlg, SW_SHOW);

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="14264-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14264-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14264-120">Riferimento al controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="14264-120">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="14264-121">Informazioni sui controlli calendario mensile</span><span class="sxs-lookup"><span data-stu-id="14264-121">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="14264-122">Utilizzo di controlli calendario mensile</span><span class="sxs-lookup"><span data-stu-id="14264-122">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 