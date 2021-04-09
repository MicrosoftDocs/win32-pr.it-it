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
# <a name="how-to-process-the-dtn_formatquery-notification"></a><span data-ttu-id="f8474-103">Come elaborare la notifica DTN \_ FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="f8474-103">How to Process the DTN\_FORMATQUERY Notification</span></span>

<span data-ttu-id="f8474-104">In questo argomento viene illustrato come elaborare una notifica di query di formato inviata dal controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="f8474-104">This topic demonstrates how to process a Format Query notification that is sent by the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f8474-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="f8474-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f8474-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="f8474-106">Technologies</span></span>

-   [<span data-ttu-id="f8474-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="f8474-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f8474-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="f8474-108">Prerequisites</span></span>

-   <span data-ttu-id="f8474-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="f8474-109">C/C++</span></span>
-   <span data-ttu-id="f8474-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="f8474-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f8474-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="f8474-111">Instructions</span></span>


<span data-ttu-id="f8474-112">Un controllo DTP Invia un codice di notifica [ \_ FORMATQUERY DTN](dtn-formatquery.md) per richiedere informazioni sulle dimensioni massime possibili di un campo di callback all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="f8474-112">A DTP control sends a [DTN\_FORMATQUERY](dtn-formatquery.md) notification code to request information about the maximum possible size of a callback field within the control.</span></span> <span data-ttu-id="f8474-113">L'applicazione deve gestire questo messaggio per assicurarsi che tutti i campi siano visualizzati correttamente.</span><span class="sxs-lookup"><span data-stu-id="f8474-113">Your application must handle this message to ensure that all fields are displayed properly.</span></span>

<span data-ttu-id="f8474-114">Il seguente esempio di codice C++ è una funzione definita dall'applicazione che elabora il codice di notifica [ \_ FORMATQUERY DTN](dtn-formatquery.md) calcolando la larghezza della stringa più ampia possibile per un campo di callback specificato.</span><span class="sxs-lookup"><span data-stu-id="f8474-114">The following C++ code example is an application-defined function that processes the [DTN\_FORMATQUERY](dtn-formatquery.md) notification code by calculating the width of the widest possible string for a given callback field.</span></span>

<span data-ttu-id="f8474-115">**Avviso di sicurezza:** L'uso errato di **lstrcmp** può compromettere la sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8474-115">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="f8474-116">Prima di chiamare **lstrcmp** nell'esempio di codice seguente, ad esempio, è necessario assicurarsi che le due stringhe abbiano terminazione null.</span><span class="sxs-lookup"><span data-stu-id="f8474-116">For example, before calling **lstrcmp** in the following code example you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="f8474-117">Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="f8474-117">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="f8474-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8474-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8474-119">Uso di controlli selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="f8474-119">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="f8474-120">Riferimento al controllo selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="f8474-120">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f8474-121">Selezione data e ora</span><span class="sxs-lookup"><span data-stu-id="f8474-121">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




