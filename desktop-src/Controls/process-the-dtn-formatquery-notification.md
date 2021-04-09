---
title: Come elaborare la notifica di DTN_FORMATQUERY
description: In questo argomento viene illustrato come elaborare una notifica di query di formato inviata dal controllo di selezione data e ora (DTP).
ms.assetid: 74E29438-2F50-4ADD-B0C4-DB3450BF08D7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e8de1e1a80d04f9a7f9e9d0cfcda198118e67c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963594"
---
# <a name="how-to-process-the-dtn_formatquery-notification"></a>Come elaborare la notifica DTN \_ FORMATQUERY

In questo argomento viene illustrato come elaborare una notifica di query di formato inviata dal controllo di selezione data e ora (DTP).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Un controllo DTP Invia un codice di notifica [ \_ FORMATQUERY DTN](dtn-formatquery.md) per richiedere informazioni sulle dimensioni massime possibili di un campo di callback all'interno del controllo. L'applicazione deve gestire questo messaggio per assicurarsi che tutti i campi siano visualizzati correttamente.

Il seguente esempio di codice C++ è una funzione definita dall'applicazione che elabora il codice di notifica [ \_ FORMATQUERY DTN](dtn-formatquery.md) calcolando la larghezza della stringa più ampia possibile per un campo di callback specificato.

**Avviso di sicurezza:** L'uso errato di **lstrcmp** può compromettere la sicurezza dell'applicazione. Prima di chiamare **lstrcmp** nell'esempio di codice seguente, ad esempio, è necessario assicurarsi che le due stringhe abbiano terminazione null. Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .



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

[Uso di controlli selezione data e ora](using-date-and-time-picker.md)
</dt> <dt>

[Riferimento al controllo selezione data e ora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selezione data e ora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




