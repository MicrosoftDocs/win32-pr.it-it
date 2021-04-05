---
title: Come elaborare la notifica di DTN_FORMAT
description: In questo argomento viene illustrato come elaborare una notifica di formato inviata dal controllo di selezione data e ora (DTP).
ms.assetid: 7B559846-FE52-4181-B25D-888BE90EB038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25271ff33ee6978ebcb0bc474492f884ed7faaa2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103873122"
---
# <a name="how-to-process-the-dtn_format-notification"></a>Come elaborare la notifica del \_ formato DTN

In questo argomento viene illustrato come elaborare una notifica di formato inviata dal controllo di selezione data e ora (DTP).

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Un controllo DTP Invia la notifica del [ \_ formato DTN](dtn-format.md) al testo della richiesta che verrà visualizzato in un campo di callback del controllo. L'applicazione deve gestire questa notifica per consentire al controllo DTP di visualizzare le informazioni che non supportano in modo nativo.

Il seguente esempio di codice C++ è una funzione definita dall'applicazione (**DoFormat**) che elabora i codici di notifica del [ \_ formato DTN](dtn-format.md) fornendo una stringa di testo per un campo di callback. L'applicazione chiama la funzione definita dall'applicazione **GetDayNum** per richiedere il numero di giorno da usare nella stringa di callback.


```C++
//  DoFormat processes DTN_FORMAT to provide the text for a callback
//  field in a DTP control. In this example, the callback field
//  contains a value for the day of year. The function calls the 
//  application-defined function GetDayNum (below) to retrieve
//  the correct value. StringCchPrintf truncates the formatted string if
//  the entire string will not fit into the destination buffer. 

void WINAPI DoFormat(HWND hwndDP, LPNMDATETIMEFORMAT lpDTFormat)
{
HRESULT hr = StringCchPrintf(lpDTFormat->szDisplay,
                sizeof(lpDTFormat->szDisplay)/sizeof(lpDTFormat->szDisplay[0]),
                L"%d",GetDayNum(&lpDTFormat->st));
if(SUCCEEDED(hr))
 {
   // Insert code here to handle the case when the function succeeds.      
 }
else
 {
   // Insert code here to handle the case when the function fails or the string 
   // is truncated.
 }
}
```



**Funzione definita dall'applicazione GetDayNum**

La funzione di esempio definita dall'applicazione **DoFormat** chiama la seguente funzione definita dall'applicazione **GetDayNum** per richiedere il numero di giorno in base alla data corrente. **GetDayNum** restituisce un valore **int** che rappresenta il giorno corrente dell'anno, da 0 a 366. Questa funzione chiama un'altra funzione definita dall'applicazione, **IsLeapYr**, durante l'elaborazione.


```C++
//  GetDayNum is an application-defined function that retrieves the 
//  correct day of year value based on the contents of a given 
//  SYSTEMTIME structure. This function calls the IsLeapYr function to 
//  check if the current year is a leap year. The function returns an 
//  integer value that represents the day of year.

int WINAPI GetDayNum(SYSTEMTIME *st)
{
    int iNormYearAccum[ ] = {31,59,90,120,151,181,
                            212,243,273,304,334,365};
    int iLeapYearAccum[ ] = {31,60,91,121,152,182,
                            213,244,274,305,335,366};
    int iDayNum;

    if(IsLeapYr(st->wYear))
        iDayNum=iLeapYearAccum[st->wMonth-2]+st->wDay;
    else
        iDayNum=iNormYearAccum[st->wMonth-2]+st->wDay;

    return (iDayNum);
}        
```



**Funzione definita dall'applicazione IsLeapYr**

La funzione definita dall'applicazione **GetDayNum** chiama la funzione **IsLeapYr** per determinare se l'anno corrente è bisestile. **IsLeapYr** restituisce un valore **bool** che è **true** se è un anno bisestile e **false** in caso contrario.


```C++
//  IsLeapYr determines if a given year value is a leap year. The
//  function returns TRUE if the current year is a leap year, and 
//  FALSE otherwise.

BOOL WINAPI IsLeapYr(int iYear)
{
    BOOL fLeapYr = FALSE;

    // If the year is evenly divisible by 4 and not by 100, but is 
    // divisible by 400, it is a leap year.
    if ((!(iYear % 4))             // each even fourth year
            && ((iYear % 100)      // not each even 100 year
            || (!(iYear % 400))))  // but each even 400 year
        fLeapYr = TRUE;

    return (fLeapYr);
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

 

 




