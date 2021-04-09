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
# <a name="how-to-process-date-and-time-picker-notifications"></a><span data-ttu-id="7588b-103">Come elaborare le notifiche di selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="7588b-103">How to Process Date and Time Picker Notifications</span></span>

<span data-ttu-id="7588b-104">In questa sezione viene illustrato come elaborare le notifiche di selezione data e ora.</span><span class="sxs-lookup"><span data-stu-id="7588b-104">This section demonstrates how to process date and time picker notifications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7588b-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="7588b-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7588b-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="7588b-106">Technologies</span></span>

-   [<span data-ttu-id="7588b-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="7588b-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7588b-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="7588b-108">Prerequisites</span></span>

-   <span data-ttu-id="7588b-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="7588b-109">C/C++</span></span>
-   <span data-ttu-id="7588b-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="7588b-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7588b-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="7588b-111">Instructions</span></span>


<span data-ttu-id="7588b-112">Un controllo di selezione data e ora (DTP) Invia messaggi di notifica alla finestra padre quando gli eventi, in genere attivati dall'input dell'utente, si verificano nel controllo.</span><span class="sxs-lookup"><span data-stu-id="7588b-112">A date and time picker (DTP) control sends notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="7588b-113">L'applicazione deve includere il codice per determinare il tipo di messaggio di notifica e rispondere in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="7588b-113">Your application must include code to determine the type of notification message and respond appropriately.</span></span>

<span data-ttu-id="7588b-114">Se si prevede di usare i campi di callback con i controlli DTP nell'applicazione, è necessario essere pronti per gestire i codici di notifica [DTN \_ FORMATQUERY](dtn-formatquery.md), [DTN \_ ](dtn-format.md)e [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="7588b-114">If you plan to use callback fields with the DTP controls in your application, you must be prepared to handle [DTN\_FORMATQUERY](dtn-formatquery.md), [DTN\_FORMAT](dtn-format.md), and [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification codes.</span></span> <span data-ttu-id="7588b-115">Per ulteriori informazioni sui campi callback, vedere [campi callback](date-and-time-picker-controls.md).</span><span class="sxs-lookup"><span data-stu-id="7588b-115">For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).</span></span>

<span data-ttu-id="7588b-116">Nell'esempio di codice C++ riportato di seguito viene identificato il messaggio di notifica inviato da un controllo DTP e viene chiamata la funzione appropriata definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7588b-116">The following C++ code example identifies the notification message sent by a DTP control and calls the appropriate application-defined function.</span></span> <span data-ttu-id="7588b-117">Per esempi di codice che illustrano come elaborare le notifiche visualizzate in questo esempio, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="7588b-117">Refer to the following topics for code examples that illustrate how to process the notifications that appear in this example.</span></span>

|                                                                                                        |
|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7588b-118">Come elaborare la notifica DTN \_ DATETIMECHANGE</span><span class="sxs-lookup"><span data-stu-id="7588b-118">How to Process the DTN\_DATETIMECHANGE Notification</span></span>](process-the-dtn-datetimechange-notification.md) |
| [<span data-ttu-id="7588b-119">Come elaborare la notifica DTN \_ FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="7588b-119">How to Process the DTN\_FORMATQUERY Notification</span></span>](process-the-dtn-formatquery-notification.md)       |
| [<span data-ttu-id="7588b-120">Come elaborare la notifica del \_ formato DTN</span><span class="sxs-lookup"><span data-stu-id="7588b-120">How to Process the DTN\_FORMAT Notification</span></span>](process-the-dtn-format-notfication.md)                  |
| [<span data-ttu-id="7588b-121">Come elaborare la notifica DTN \_ WMKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="7588b-121">How to Process the DTN\_WMKEYDOWN Notification</span></span>](process-the-dtn-wmkeydown-notification.md)           |



 



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



## <a name="related-topics"></a><span data-ttu-id="7588b-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7588b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7588b-123">Notifiche selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="7588b-123">Date and Time Picker Notifications</span></span>](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[<span data-ttu-id="7588b-124">Riferimento al controllo selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="7588b-124">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7588b-125">Uso di controlli selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="7588b-125">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="7588b-126">Selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="7588b-126">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




