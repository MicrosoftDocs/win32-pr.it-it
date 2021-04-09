---
title: Come elaborare la notifica di DTN_DATETIMECHANGE
description: In questo argomento viene illustrato come elaborare la notifica delle modifiche apportate dall'utente al controllo di selezione data e ora (DTP).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434c7ebbda673f76a757375e9a3d23504483d42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963603"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a>Come elaborare la notifica DTN \_ DATETIMECHANGE

In questo argomento viene illustrato come elaborare la notifica delle modifiche apportate dall'utente al controllo di selezione data e ora (DTP).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Un controllo DTP invia il codice di notifica [ \_ DATETIMECHANGE di DTN](dtn-datetimechange.md) ogni volta che si verifica una modifica. Questa notifica, ad esempio, verrà generata quando l'utente modifica uno dei campi del controllo o, nel caso in cui il controllo sia impostato sullo stile [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) , quando l'utente modifica lo stato della casella di controllo del controllo.

L'applicazione deve includere il codice per elaborare \_ i messaggi DATETIMECHANGE di DTN inviati dal controllo DTP.

Il seguente esempio di codice C++ è una funzione definita dall'applicazione progettata per indicare lo stato di un controllo DTP impostato sullo stile **\_ SHOWNONE DTS** .



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

[Uso di controlli selezione data e ora](using-date-and-time-picker.md)
</dt> <dt>

[Riferimento al controllo selezione data e ora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selezione data e ora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




