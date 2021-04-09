---
title: Come elaborare le notifiche di selezione data e ora
description: In questa sezione viene illustrato come elaborare le notifiche di selezione data e ora.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b904c464677a81151b03e3ae89085847e4e8bdf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047627"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a>Come elaborare le notifiche di selezione data e ora

In questa sezione viene illustrato come elaborare le notifiche di selezione data e ora.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Un controllo di selezione data e ora (DTP) Invia messaggi di notifica alla finestra padre quando gli eventi, in genere attivati dall'input dell'utente, si verificano nel controllo. L'applicazione deve includere il codice per determinare il tipo di messaggio di notifica e rispondere in modo appropriato.

Se si prevede di usare i campi di callback con i controlli DTP nell'applicazione, è necessario essere pronti per gestire i codici di notifica [DTN \_ FORMATQUERY](dtn-formatquery.md), [DTN \_ ](dtn-format.md)e [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) . Per ulteriori informazioni sui campi callback, vedere [campi callback](date-and-time-picker-controls.md).

Nell'esempio di codice C++ riportato di seguito viene identificato il messaggio di notifica inviato da un controllo DTP e viene chiamata la funzione appropriata definita dall'applicazione. Per esempi di codice che illustrano come elaborare le notifiche visualizzate in questo esempio, vedere gli argomenti seguenti.

|                                                                                                        |
|--------------------------------------------------------------------------------------------------------|
| [Come elaborare la notifica DTN \_ DATETIMECHANGE](process-the-dtn-datetimechange-notification.md) |
| [Come elaborare la notifica DTN \_ FORMATQUERY](process-the-dtn-formatquery-notification.md)       |
| [Come elaborare la notifica del \_ formato DTN](process-the-dtn-format-notfication.md)                  |
| [Come elaborare la notifica DTN \_ WMKEYDOWN](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Notifiche selezione data e ora](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[Riferimento al controllo selezione data e ora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Uso di controlli selezione data e ora](using-date-and-time-picker.md)
</dt> <dt>

[Selezione data e ora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




