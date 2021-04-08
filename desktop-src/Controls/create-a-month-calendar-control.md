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
# <a name="how-to-create-a-month-calendar-control"></a>Come creare un controllo calendario mensile

In questo argomento viene illustrato come creare dinamicamente un controllo calendario mensile utilizzando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Per creare un controllo calendario mensile, usare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la [**\_ classe MONTHCAL**](common-control-window-classes.md) come classe Window. È necessario prima registrare la classe della finestra chiamando la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , specificando il bit delle **\_ \_ classi di data ICC** nella struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) associata.

Nell'esempio seguente viene illustrato come creare un controllo calendario mensile in una finestra di dialogo non modale esistente. Si noti che i valori delle dimensioni passati a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) sono tutti zeri. Poiché la dimensione minima richiesta dipende dal tipo di carattere utilizzato dal controllo, nell'esempio viene utilizzata la macro [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) per richiedere informazioni sulle dimensioni e quindi ridimensionare il controllo chiamando [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos). Se successivamente si modifica il tipo di carattere con [**WM \_ sefont**](/windows/desktop/winmsg/wm-setfont), le dimensioni del controllo non vengono modificate. È necessario chiamare di nuovo **MonthCal \_ GetMinReqRect** e ridimensionare il controllo in modo da adattarlo al nuovo tipo di carattere.



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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo calendario mensile](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Informazioni sui controlli calendario mensile](month-calendar-controls.md)
</dt> <dt>

[Utilizzo di controlli calendario mensile](using-month-calendar-controls.md)
</dt> </dl>

 

 