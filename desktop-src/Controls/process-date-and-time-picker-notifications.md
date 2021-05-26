---
title: Come elaborare le notifiche di selezione data e ora
description: Questa sezione illustra come elaborare le notifiche di selezione data e ora.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa1214ebd671b4ae222990bde4b44586e6d7b11
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424181"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a><span data-ttu-id="76b47-103">Come elaborare le notifiche di selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="76b47-103">How to Process Date and Time Picker Notifications</span></span>

<span data-ttu-id="76b47-104">Questa sezione illustra come elaborare le notifiche di selezione data e ora.</span><span class="sxs-lookup"><span data-stu-id="76b47-104">This section demonstrates how to process date and time picker notifications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="76b47-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="76b47-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="76b47-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="76b47-106">Technologies</span></span>

-   [<span data-ttu-id="76b47-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="76b47-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="76b47-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="76b47-108">Prerequisites</span></span>

-   <span data-ttu-id="76b47-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="76b47-109">C/C++</span></span>
-   <span data-ttu-id="76b47-110">Programmazione Interfaccia utente Windows</span><span class="sxs-lookup"><span data-stu-id="76b47-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="76b47-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="76b47-111">Instructions</span></span>


<span data-ttu-id="76b47-112">Un controllo di selezione data e ora (DTP) invia messaggi di notifica alla finestra padre quando si verificano eventi, in genere attivati dall'input dell'utente, nel controllo.</span><span class="sxs-lookup"><span data-stu-id="76b47-112">A date and time picker (DTP) control sends notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="76b47-113">L'applicazione deve includere codice per determinare il tipo di messaggio di notifica e rispondere in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="76b47-113">Your application must include code to determine the type of notification message and respond appropriately.</span></span>

<span data-ttu-id="76b47-114">Se si prevede di usare i campi di callback con i controlli DTP nell'applicazione, è necessario essere pronti per gestire i codici di notifica [DTN \_ FORMATQUERY,](dtn-formatquery.md) [DTN \_ FORMAT](dtn-format.md)e [DTN \_ WMKEYDOWN.](dtn-wmkeydown.md)</span><span class="sxs-lookup"><span data-stu-id="76b47-114">If you plan to use callback fields with the DTP controls in your application, you must be prepared to handle [DTN\_FORMATQUERY](dtn-formatquery.md), [DTN\_FORMAT](dtn-format.md), and [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification codes.</span></span> <span data-ttu-id="76b47-115">Per altre informazioni sui campi di callback, vedere [Campi di callback](date-and-time-picker-controls.md).</span><span class="sxs-lookup"><span data-stu-id="76b47-115">For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).</span></span>

<span data-ttu-id="76b47-116">L'esempio di codice C++ seguente identifica il messaggio di notifica inviato da un controllo DTP e chiama la funzione appropriata definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="76b47-116">The following C++ code example identifies the notification message sent by a DTP control and calls the appropriate application-defined function.</span></span> <span data-ttu-id="76b47-117">Fare riferimento agli argomenti seguenti per esempi di codice che illustrano come elaborare le notifiche visualizzate in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="76b47-117">Refer to the following topics for code examples that illustrate how to process the notifications that appear in this example.</span></span>

|   <span data-ttu-id="76b47-118">Argomenti</span><span class="sxs-lookup"><span data-stu-id="76b47-118">Topics</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76b47-119">Come elaborare la notifica DTN \_ DATETIMECHANGE</span><span class="sxs-lookup"><span data-stu-id="76b47-119">How to Process the DTN\_DATETIMECHANGE Notification</span></span>](process-the-dtn-datetimechange-notification.md) |
| [<span data-ttu-id="76b47-120">Come elaborare la notifica DTN \_ FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="76b47-120">How to Process the DTN\_FORMATQUERY Notification</span></span>](process-the-dtn-formatquery-notification.md)       |
| [<span data-ttu-id="76b47-121">Come elaborare la notifica DTN \_ FORMAT</span><span class="sxs-lookup"><span data-stu-id="76b47-121">How to Process the DTN\_FORMAT Notification</span></span>](process-the-dtn-format-notfication.md)                  |
| [<span data-ttu-id="76b47-122">Come elaborare la notifica WMKEYDOWN DTN \_</span><span class="sxs-lookup"><span data-stu-id="76b47-122">How to Process the DTN\_WMKEYDOWN Notification</span></span>](process-the-dtn-wmkeydown-notification.md)           |



 



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



## <a name="related-topics"></a><span data-ttu-id="76b47-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76b47-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76b47-124">Notifiche di selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="76b47-124">Date and Time Picker Notifications</span></span>](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[<span data-ttu-id="76b47-125">Informazioni di riferimento sul controllo Selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="76b47-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="76b47-126">Uso dei controlli selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="76b47-126">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="76b47-127">Selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="76b47-127">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




