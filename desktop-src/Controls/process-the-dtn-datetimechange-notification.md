---
title: Come elaborare la DTN_DATETIMECHANGE notifica
description: Questo argomento illustra come elaborare la notifica delle modifiche apportate dall'utente al controllo selezione data e ora (DTP).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9490059a202eff69a05b34a086e74d6df52758713fd5b66d899d1ab114a31040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829922"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a>Come elaborare la notifica DTN \_ DATETIMECHANGE

Questo argomento illustra come elaborare la notifica delle modifiche apportate dall'utente al controllo selezione data e ora (DTP).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Un controllo DTP invia il [codice di notifica DTN \_ DATETIMECHANGE](dtn-datetimechange.md) ogni volta che si verifica una modifica. Ad esempio, questa notifica verrà generata quando l'utente modifica uno dei campi nel controllo o, nel caso in cui il controllo sia impostato sullo stile [**DTS \_ SHOWNONE,**](date-and-time-picker-control-styles.md) quando l'utente modifica lo stato della casella di controllo del controllo.

L'applicazione deve includere il codice per elaborare i messaggi \_ DTN DATETIMECHANGE inviati dal controllo DTP.

L'esempio di codice C++ seguente è una funzione definita dall'applicazione progettata per indicare lo stato di un controllo DTP impostato sullo stile **DTS \_ SHOWNONE.**



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
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

 

 




