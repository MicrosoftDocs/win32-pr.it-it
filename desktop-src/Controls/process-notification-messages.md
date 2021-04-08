---
title: Come elaborare i messaggi di notifica
description: Una finestra delle proprietà Invia \_ messaggi WM Notify per recuperare le informazioni dalle pagine e per notificare le pagine delle azioni dell'utente.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724275"
---
# <a name="how-to-process-notification-messages"></a><span data-ttu-id="64d4a-103">Come elaborare i messaggi di notifica</span><span class="sxs-lookup"><span data-stu-id="64d4a-103">How to Process Notification Messages</span></span>

<span data-ttu-id="64d4a-104">Una finestra delle proprietà Invia messaggi [**WM \_ Notify**](wm-notify.md) per recuperare le informazioni dalle pagine e per notificare le pagine delle azioni dell'utente.</span><span class="sxs-lookup"><span data-stu-id="64d4a-104">A property sheet sends [**WM\_NOTIFY**](wm-notify.md) messages to retrieve information from the pages and to notify the pages of user actions.</span></span>

<span data-ttu-id="64d4a-105">Il parametro *lParam* del messaggio è l'indirizzo di una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , che contiene l'handle per la finestra di dialogo della finestra delle proprietà, l'handle per la finestra di dialogo della pagina e un codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="64d4a-105">The *lParam* parameter of the message is the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, which contains the handle to the property sheet dialog box, the handle to the page dialog box, and a notification code.</span></span> <span data-ttu-id="64d4a-106">La pagina deve rispondere ad alcuni messaggi di notifica impostando il \_ valore DWL MSGRESULT della pagina su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="64d4a-106">The page must respond to some notification messages by setting the DWL\_MSGRESULT value of the page to either **TRUE** or **FALSE**.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="64d4a-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="64d4a-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="64d4a-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="64d4a-108">Technologies</span></span>

-   [<span data-ttu-id="64d4a-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="64d4a-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="64d4a-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="64d4a-110">Prerequisites</span></span>

-   <span data-ttu-id="64d4a-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="64d4a-111">C/C++</span></span>
-   <span data-ttu-id="64d4a-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="64d4a-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="64d4a-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="64d4a-113">Instructions</span></span>

### <a name="process-notification-messages"></a><span data-ttu-id="64d4a-114">Elaborare i messaggi di notifica</span><span class="sxs-lookup"><span data-stu-id="64d4a-114">Process Notification Messages</span></span>

<span data-ttu-id="64d4a-115">Nell'esempio seguente è riportato un frammento di codice della routine della finestra di dialogo per una pagina.</span><span class="sxs-lookup"><span data-stu-id="64d4a-115">The following example is a code fragment from the dialog box procedure for a page.</span></span> <span data-ttu-id="64d4a-116">Viene illustrato come elaborare il codice di notifica della [ \_ Guida di PSN](psn-help.md) .</span><span class="sxs-lookup"><span data-stu-id="64d4a-116">It shows how to process the [PSN\_HELP](psn-help.md) notification code.</span></span>


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a><span data-ttu-id="64d4a-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="64d4a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64d4a-118">Utilizzo delle finestre delle proprietà</span><span class="sxs-lookup"><span data-stu-id="64d4a-118">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

<span data-ttu-id="64d4a-119">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="64d4a-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




