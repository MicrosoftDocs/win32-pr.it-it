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
# <a name="how-to-process-the-dtn_format-notification"></a><span data-ttu-id="5e4dc-103">Come elaborare la notifica del \_ formato DTN</span><span class="sxs-lookup"><span data-stu-id="5e4dc-103">How to Process the DTN\_FORMAT Notification</span></span>

<span data-ttu-id="5e4dc-104">In questo argomento viene illustrato come elaborare una notifica di formato inviata dal controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="5e4dc-104">This topic demonstrates how to process a format notification sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5e4dc-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="5e4dc-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5e4dc-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="5e4dc-106">Technologies</span></span>

-   [<span data-ttu-id="5e4dc-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="5e4dc-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5e4dc-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="5e4dc-108">Prerequisites</span></span>

-   <span data-ttu-id="5e4dc-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="5e4dc-109">C/C++</span></span>
-   <span data-ttu-id="5e4dc-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="5e4dc-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="5e4dc-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="5e4dc-111">Instructions</span></span>


<span data-ttu-id="5e4dc-112">Un controllo DTP Invia la notifica del [ \_ formato DTN](dtn-format.md) al testo della richiesta che verrà visualizzato in un campo di callback del controllo.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-112">A DTP control sends the [DTN\_FORMAT](dtn-format.md) notification to request text that will be displayed in a callback field of the control.</span></span> <span data-ttu-id="5e4dc-113">L'applicazione deve gestire questa notifica per consentire al controllo DTP di visualizzare le informazioni che non supportano in modo nativo.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-113">Your application must handle this notification to enable the DTP control to display information that it does not natively support.</span></span>

<span data-ttu-id="5e4dc-114">Il seguente esempio di codice C++ è una funzione definita dall'applicazione (**DoFormat**) che elabora i codici di notifica del [ \_ formato DTN](dtn-format.md) fornendo una stringa di testo per un campo di callback.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-114">The following C++ code example is an application-defined function (**DoFormat**) that processes [DTN\_FORMAT](dtn-format.md) notification codes by providing a text string for a callback field.</span></span> <span data-ttu-id="5e4dc-115">L'applicazione chiama la funzione definita dall'applicazione **GetDayNum** per richiedere il numero di giorno da usare nella stringa di callback.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-115">The application calls the **GetDayNum** application-defined function to request the day number to be used in the callback string.</span></span>


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



<span data-ttu-id="5e4dc-116">**Funzione definita dall'applicazione GetDayNum**</span><span class="sxs-lookup"><span data-stu-id="5e4dc-116">**The GetDayNum application-defined function**</span></span>

<span data-ttu-id="5e4dc-117">La funzione di esempio definita dall'applicazione **DoFormat** chiama la seguente funzione definita dall'applicazione **GetDayNum** per richiedere il numero di giorno in base alla data corrente.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-117">The application-defined sample function **DoFormat** calls the following **GetDayNum** application-defined function to request the day number based on the current date.</span></span> <span data-ttu-id="5e4dc-118">**GetDayNum** restituisce un valore **int** che rappresenta il giorno corrente dell'anno, da 0 a 366.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-118">**GetDayNum** returns an **INT** value that represents the current day of the year, from 0 to 366.</span></span> <span data-ttu-id="5e4dc-119">Questa funzione chiama un'altra funzione definita dall'applicazione, **IsLeapYr**, durante l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-119">This function calls another application-defined function, **IsLeapYr**, during processing.</span></span>


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



<span data-ttu-id="5e4dc-120">**Funzione definita dall'applicazione IsLeapYr**</span><span class="sxs-lookup"><span data-stu-id="5e4dc-120">**The IsLeapYr application-defined function**</span></span>

<span data-ttu-id="5e4dc-121">La funzione definita dall'applicazione **GetDayNum** chiama la funzione **IsLeapYr** per determinare se l'anno corrente è bisestile.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-121">The application-defined function **GetDayNum** calls the **IsLeapYr** function to determine whether the current year is a leap year.</span></span> <span data-ttu-id="5e4dc-122">**IsLeapYr** restituisce un valore **bool** che è **true** se è un anno bisestile e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5e4dc-122">**IsLeapYr** returns a **BOOL** value that is **TRUE** if it is a leap year and **FALSE** otherwise.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5e4dc-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5e4dc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e4dc-124">Uso di controlli selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="5e4dc-124">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="5e4dc-125">Riferimento al controllo selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="5e4dc-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="5e4dc-126">Selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="5e4dc-126">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




