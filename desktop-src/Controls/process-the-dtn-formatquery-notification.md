---
title: Come elaborare la DTN_FORMATQUERY notifica
description: Questo argomento illustra come elaborare una notifica di query di formato inviata dal controllo selezione data e ora (DTP).
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c148332c36711e68b7c3b773fdb47acef202c5fd2a67f5620319f06c7fbc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696941"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a>Come elaborare la notifica DTN \_ FORMATQUERY

Questo argomento illustra come elaborare una notifica di query di formato inviata dal controllo selezione data e ora (DTP).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Un controllo DTP invia un [codice di notifica DTN \_ FORMATQUERY](dtn-formatquery.md) per richiedere informazioni sulle dimensioni massime possibili di un campo di callback all'interno del controllo. L'applicazione deve gestire questo messaggio per assicurarsi che tutti i campi siano visualizzati correttamente.

L'esempio di codice C++ seguente è una funzione definita dall'applicazione che elabora il codice di notifica [DTN \_ FORMATQUERY](dtn-formatquery.md) calcolando la larghezza della stringa più ampia possibile per un determinato campo di callback.

**Avviso di sicurezza:** **L'uso non corretto di lstrcmp** può compromettere la sicurezza dell'applicazione. Ad esempio, prima di chiamare **lstrcmp** nell'esempio di codice seguente è necessario assicurarsi che le due stringhe siano con terminazione Null. Prima di continuare, vedere Considerazioni sulla [sicurezza: Microsoft Windows Controls.](sec-comctls.md)



```C++
//  DoFormatQuery processes DTN_FORMATQUERY messages to ensure that the
//  DTP control displays callback fields properly.
//

void WINAPI DoFormatQuery(
 HWND hwndDP, 
 LPNMDATETIMEFORMATQUERY lpDTFQuery)
{
    HDC hdc;
    HFONT hFont, hOrigFont;

    //  Prepare the device context for GetTextExtentPoint32 call.
    hdc = GetDC(hwndDP);

    hFont = (HFONT) SendMessage(hwndDP, WM_GETFONT, 0L, 0L); 

    if(!hFont)
        hFont = (HFONT)GetStockObject(DEFAULT_GUI_FONT);

    hOrigFont = (HFONT) SelectObject(hdc, hFont);

    // Check to see if this is the callback segment desired. If so,
    // use the longest text segment to determine the maximum 
    // width of the callback field, and then place the information into 
    // the NMDATETIMEFORMATQUERY structure.
    if(!lstrcmp(L"XX",lpDTFQuery->pszFormat))
        GetTextExtentPoint32 (hdc,
                          L"366",  // widest date string
                          3,
                          &lpDTFQuery->szMax);

    // Reset the font in the device context; then release the context.
    SelectObject(hdc,hOrigFont);
    ReleaseDC(hwndDP, hdc);
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

 

 




