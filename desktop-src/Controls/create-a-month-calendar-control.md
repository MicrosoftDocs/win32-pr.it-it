---
title: Come creare un controllo calendario mensile
description: Questo argomento illustra come creare dinamicamente un controllo calendario mensile usando la funzione CreateWindowEx.
ms.assetid: 35ADDA85-5D7D-46F4-A637-99FEE4592B3B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f0fbc819a79b05842db75c1871e8150b311444e6055d076a9831b0bc42486b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831817"
---
# <a name="how-to-create-a-month-calendar-control"></a>Come creare un controllo calendario mensile

Questo argomento illustra come creare dinamicamente un controllo calendario mensile usando la [**funzione CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Per creare un controllo calendario mensile, usare [**la funzione CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) specificando [**MONTHCAL \_ CLASS**](common-control-window-classes.md) come classe window. È prima necessario registrare la classe della finestra chiamando la [**funzione InitCommonControlsEx,**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) specificando il bit **ICC \_ DATE \_ CLASSES** nella struttura [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) che lo accompagna.

Nell'esempio seguente viene illustrato come creare un controllo calendario mensile in una finestra di dialogo non modabile esistente. Si noti che i valori delle dimensioni [**passati a CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) sono tutti zeri. Poiché le dimensioni minime richieste dipendono dal tipo di carattere utilizzato dal controllo, nell'esempio viene utilizzata la macro [**\_ MonthCal GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) per richiedere informazioni sulle dimensioni e quindi il controllo viene ridimensionato chiamando [**SetWindowPos.**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) Se successivamente si modifica il tipo di carattere [**con WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont), le dimensioni del controllo non verranno modificate. È necessario chiamare **di nuovo MonthCal \_ GetMinReqRect e** ridimensionare il controllo per adattarlo al nuovo tipo di carattere.



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

[Informazioni di riferimento sul controllo Calendario mensile](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Informazioni sui controlli calendario mensile](month-calendar-controls.md)
</dt> <dt>

[Uso dei controlli calendario mensile](using-month-calendar-controls.md)
</dt> </dl>

 

 