---
title: Come elaborare le notifiche di selezione data e ora
description: Questa sezione illustra come elaborare le notifiche di selezione data e ora.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81846d22f3c946d1bfdf661823429fd092b78647cf0ebcb0d683d2600ddcaf17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540480"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a>Come elaborare le notifiche di selezione data e ora

Questa sezione illustra come elaborare le notifiche di selezione data e ora.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Un controllo di selezione data e ora (DTP) invia messaggi di notifica alla finestra padre quando si verificano eventi, in genere attivati dall'input dell'utente, nel controllo. L'applicazione deve includere codice per determinare il tipo di messaggio di notifica e rispondere in modo appropriato.

Se si prevede di usare i campi di callback con i controlli DTP nell'applicazione, è necessario essere pronti a gestire i codici di notifica [DTN \_ FORMATQUERY,](dtn-formatquery.md) [DTN \_ FORMAT](dtn-format.md)e [DTN \_ WMKEYDOWN.](dtn-wmkeydown.md) Per altre informazioni sui campi di callback, vedere [Campi di callback.](date-and-time-picker-controls.md)

L'esempio di codice C++ seguente identifica il messaggio di notifica inviato da un controllo DTP e chiama la funzione appropriata definita dall'applicazione. Fare riferimento agli argomenti seguenti per esempi di codice che illustrano come elaborare le notifiche visualizzate in questo esempio.

|   Argomenti                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [Come elaborare la notifica DTN \_ DATETIMECHANGE](process-the-dtn-datetimechange-notification.md) |
| [Come elaborare la notifica DTN \_ FORMATQUERY](process-the-dtn-formatquery-notification.md)       |
| [Come elaborare la notifica DTN \_ FORMAT](process-the-dtn-format-notfication.md)                  |
| [Come elaborare la notifica WMKEYDOWN DTN \_](process-the-dtn-wmkeydown-notification.md)           |



 



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

[Notifiche di selezione data e ora](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[Informazioni di riferimento sul controllo Selezione data e ora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Uso dei controlli selezione data e ora](using-date-and-time-picker.md)
</dt> <dt>

[Selezione data e ora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




