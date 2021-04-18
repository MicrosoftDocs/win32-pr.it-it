---
description: Descrizione delle tecniche di sottostandard per l'esposizione di controlli personalizzati.
ms.assetid: 107968c6-c3b3-462d-b488-96c69f2b3b14
title: Tecniche sottostandard per l'esposizione di controlli personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194614474596b55e0b1cf0530a07f9b3c411f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315549"
---
# <a name="substandard-techniques-for-exposing-custom-controls"></a><span data-ttu-id="7c354-103">Tecniche sottostandard per l'esposizione di controlli personalizzati</span><span class="sxs-lookup"><span data-stu-id="7c354-103">Substandard Techniques for Exposing Custom Controls</span></span>

<span data-ttu-id="7c354-104">Se un'applicazione non supporta Microsoft Active Accessibility, potrebbe non essere completamente accessibile.</span><span class="sxs-lookup"><span data-stu-id="7c354-104">If an application does not support Microsoft Active Accessibility, it may not be fully accessible.</span></span> <span data-ttu-id="7c354-105">Le tecniche seguenti eseguono il rendering dei controlli parzialmente compatibili:</span><span class="sxs-lookup"><span data-stu-id="7c354-105">The following techniques render controls partially compatible:</span></span>

-   <span data-ttu-id="7c354-106">Restituisce una stringa descrittiva quando viene eseguita una query sul controllo utilizzando il \_ messaggio WM gettext.</span><span class="sxs-lookup"><span data-stu-id="7c354-106">Return a descriptive string when the control is queried by using the WM\_GETTEXT message.</span></span> <span data-ttu-id="7c354-107">Ad esempio, consentire a un equivalente personalizzato di un controllo Button denominato "Print" di restituire la stringa "Print button".</span><span class="sxs-lookup"><span data-stu-id="7c354-107">For example, allow a custom equivalent of a button control labeled "Print" to return the string "Print button."</span></span> <span data-ttu-id="7c354-108">Identifica sia il tipo di controllo che l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="7c354-108">This identifies both control type and label.</span></span> <span data-ttu-id="7c354-109">La stessa stringa è appropriata per un pulsante con un'etichetta diversa dal testo, ad esempio un grafico di una stampante.</span><span class="sxs-lookup"><span data-stu-id="7c354-109">The same string is appropriate for a button with a label that is something other than text, such as a graphic of a printer.</span></span> <span data-ttu-id="7c354-110">Analogamente, consentire a un controllo personalizzato che si comporta come una casella di controllo di restituire la stringa della didascalia "stampa abilitata, selezionata".</span><span class="sxs-lookup"><span data-stu-id="7c354-110">Similarly, allow a custom control that behaves like a check box to return the caption string "Printing Enabled check box, checked."</span></span>
-   <span data-ttu-id="7c354-111">Supporto del \_ messaggio WM GETDLGCODE, che identifica l'input da tastiera supportato.</span><span class="sxs-lookup"><span data-stu-id="7c354-111">Support the WM\_GETDLGCODE message, identifying the keyboard input that is supported.</span></span> <span data-ttu-id="7c354-112">Ad esempio, consentire a un equivalente personalizzato di un controllo di modifica di gestire WM \_ GETDLGCODE restituendo DLGC \_ HASSETSEL se gestisce i messaggi per impostare la selezione, DLGC \_ WANTARROWS se usa i tasti di direzione e DLGC \_ WANTCHARS per indicare che usa l'input di caratteri.</span><span class="sxs-lookup"><span data-stu-id="7c354-112">For example, allow a custom equivalent of an edit control to handle WM\_GETDLGCODE by returning DLGC\_HASSETSEL if it handles messages to set the selection, DLGC\_WANTARROWS if it uses arrow keys, and DLGC\_WANTCHARS to indicate that it uses character input.</span></span>
    > [!Note]  
    > <span data-ttu-id="7c354-113">Solo i controlli con i rispettivi handle di finestra possono rispondere ai \_ messaggi WM GetText e WM \_ GETDLGCODE.</span><span class="sxs-lookup"><span data-stu-id="7c354-113">Only controls that have their own window handles can respond to the WM\_GETTEXT and WM\_GETDLGCODE messages.</span></span>

     

<span data-ttu-id="7c354-114">Per evitare problemi di compatibilità con gli strumenti di accessibilità, è necessario seguire attentamente Active Accessibility linee guida per la progettazione di controlli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="7c354-114">To avoid compatibility problems with accessibility aids, you should follow Active Accessibility guidelines closely when designing custom controls.</span></span> <span data-ttu-id="7c354-115">Per ulteriori informazioni su come evitare problemi di compatibilità con gli strumenti di accessibilità, vedere la sezione relativa all' [accessibilità](../accessibility/accessibility.md) .</span><span class="sxs-lookup"><span data-stu-id="7c354-115">For more information about how to avoid compatibility problems with accessibility aids, see the [Accessibility](../accessibility/accessibility.md) section.</span></span>

 

 
