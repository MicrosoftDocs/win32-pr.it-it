---
title: Come utilizzare i codici di notifica del controllo Rich Edit
description: Una finestra padre di un controllo Rich Edit può elaborare i codici di notifica per monitorare gli eventi che influiscono sul controllo. I controlli Rich Edit supportano tutti i codici di notifica utilizzati con i controlli di modifica, oltre a diversi altri.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2020
ms.locfileid: "103956287"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a><span data-ttu-id="40eb2-104">Come utilizzare i codici di notifica del controllo Rich Edit</span><span class="sxs-lookup"><span data-stu-id="40eb2-104">How to Use Rich Edit Control Notification Codes</span></span>

<span data-ttu-id="40eb2-105">Una finestra padre di un controllo Rich Edit può elaborare i codici di notifica per monitorare gli eventi che influiscono sul controllo.</span><span class="sxs-lookup"><span data-stu-id="40eb2-105">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="40eb2-106">I controlli Rich Edit supportano tutti i codici di notifica utilizzati con i controlli di modifica, oltre a diversi altri.</span><span class="sxs-lookup"><span data-stu-id="40eb2-106">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="40eb2-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="40eb2-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="40eb2-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="40eb2-108">Technologies</span></span>

-   [<span data-ttu-id="40eb2-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="40eb2-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="40eb2-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="40eb2-110">Prerequisites</span></span>

-   <span data-ttu-id="40eb2-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="40eb2-111">C/C++</span></span>
-   <span data-ttu-id="40eb2-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="40eb2-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="40eb2-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="40eb2-113">Instructions</span></span>

### <a name="use-a-rich-edit-control-notification-code"></a><span data-ttu-id="40eb2-114">Usare un codice di notifica del controllo Rich Edit</span><span class="sxs-lookup"><span data-stu-id="40eb2-114">Use a Rich Edit Control Notification Code</span></span>

<span data-ttu-id="40eb2-115">È possibile individuare i codici di notifica che un controllo Rich Edit Invia la finestra padre impostando la relativa maschera eventi.</span><span class="sxs-lookup"><span data-stu-id="40eb2-115">You can determine which notification codes a rich edit control sends its parent window by setting its event mask.</span></span> <span data-ttu-id="40eb2-116">Per impostare la maschera eventi per un controllo Rich Edit, utilizzare il [**messaggio \_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="40eb2-116">To set the event mask for a rich edit control, use the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span> <span data-ttu-id="40eb2-117">È possibile recuperare la maschera eventi corrente per un controllo Rich Edit usando il messaggio [**\_ GETEVENTMASK em**](em-geteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="40eb2-117">You can retrieve the current event mask for a rich edit control by using the [**EM\_GETEVENTMASK**](em-geteventmask.md) message.</span></span> <span data-ttu-id="40eb2-118">Per un elenco di flag di maschera eventi, vedere [flag di maschera eventi del controllo Rich Edit](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="40eb2-118">For a list of event mask flags, see [Rich Edit Control Event Mask Flags](rich-edit-control-event-mask-flags.md).</span></span>

<span data-ttu-id="40eb2-119">Una finestra padre di un controllo Rich Edit può filtrare tutti gli input di tastiera e mouse nel controllo elaborando il codice di notifica [en \_ msgfilter](en-msgfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="40eb2-119">A rich edit control's parent window can filter all keyboard and mouse input to the control by processing the [EN\_MSGFILTER](en-msgfilter.md) notification code.</span></span> <span data-ttu-id="40eb2-120">La finestra padre può impedire l'elaborazione del messaggio della tastiera o del mouse oppure può modificare il messaggio modificando la struttura [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) specificata.</span><span class="sxs-lookup"><span data-stu-id="40eb2-120">The parent window can prevent the keyboard or mouse message from being processed or can change the message by modifying the specified [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) structure.</span></span>

<span data-ttu-id="40eb2-121">Un'applicazione può elaborare il codice di notifica [ \_ protetto it](en-protected.md) per rilevare quando l'utente tenta di modificare il testo protetto.</span><span class="sxs-lookup"><span data-stu-id="40eb2-121">An application can process the [EN\_PROTECTED](en-protected.md) notification code to detect when the user attempts to modify protected text.</span></span> <span data-ttu-id="40eb2-122">Per contrassegnare un intervallo di testo come protetto, è possibile impostare l'effetto carattere protetto.</span><span class="sxs-lookup"><span data-stu-id="40eb2-122">To mark a range of text as protected, you can set the protected character effect.</span></span>

<span data-ttu-id="40eb2-123">È possibile consentire all'utente di eliminare i file in un controllo Rich Edit elaborando il codice di notifica [en \_ DropFiles](en-dropfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="40eb2-123">You can enable the user to drop files in a rich edit control by processing the [EN\_DROPFILES](en-dropfiles.md) notification code.</span></span> <span data-ttu-id="40eb2-124">La struttura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) specificata contiene informazioni sui file che vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="40eb2-124">The specified [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure contains information about the files that are being dropped.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40eb2-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40eb2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40eb2-126">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="40eb2-126">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="40eb2-127">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="40eb2-127">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




