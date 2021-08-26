---
title: Come creare un controllo selezione data e ora
description: In questo argomento viene illustrato come creare dinamicamente un controllo di selezione data e ora.
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa3f18e6033d3764e385280da383d74c351201694969266dcc383654a4372ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920891"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a>Come creare un controllo selezione data e ora

In questo argomento viene illustrato come creare dinamicamente un controllo di selezione data e ora. L'esempio di codice C++ associato crea un controllo DTP in una finestra di dialogo non modabile. Usa lo stile [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) per consentire all'utente di simulare la disattivazione della data all'interno del controllo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Registrare la classe della finestra chiamando [**la funzione InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e specificando il bit ICC DATE CLASSES nella struttura \_ \_ [**INITCOMMONCONTROLSEX.**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a>Passaggio 2:

Per creare il controllo DTP, usare la [**funzione CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Specificare [**DATETIMEPICK \_ CLASS**](common-control-window-classes.md) come classe della finestra e passare l'handle alla finestra di dialogo padre.

Nell'esempio di codice C++ seguente viene utilizzata [**la funzione CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) per creare una finestra di dialogo non modabile. Chiama quindi **CreateWindowEx per** creare il controllo DTP.


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



## <a name="complete-example"></a>Esempio completo


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei controlli selezione data e ora](using-date-and-time-picker.md)
</dt> <dt>

[Informazioni di riferimento sul controllo Selezione data e ora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selezione data e ora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 