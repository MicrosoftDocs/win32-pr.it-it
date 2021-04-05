---
title: Infrastruttura WinEvents
description: Il sistema operativo Microsoft Windows include una funzionalità, denominata WinEvents, che consente ai processi e alle applicazioni in esecuzione sul desktop di Windows di scambiare determinati tipi di informazioni.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "103720016"
---
# <a name="winevents"></a><span data-ttu-id="bf77c-103">WinEvents</span><span class="sxs-lookup"><span data-stu-id="bf77c-103">WinEvents</span></span>

<span data-ttu-id="bf77c-104">Il sistema operativo Microsoft Windows include una funzionalità, denominata *winEvents*, che consente ai processi e alle applicazioni in esecuzione sul desktop di Windows di scambiare determinati tipi di informazioni.</span><span class="sxs-lookup"><span data-stu-id="bf77c-104">The Microsoft Windows operating system includes a feature, called *WinEvents*, that enables processes and applications running on the Windows desktop to exchange certain types of information.</span></span> <span data-ttu-id="bf77c-105">Gli strumenti di accessibilità che usano automazione interfaccia utente Microsoft e Microsoft Active Accessibility sono tra gli utenti principali del WinEvents.</span><span class="sxs-lookup"><span data-stu-id="bf77c-105">Accessibility tools that use Microsoft UI Automation and Microsoft Active Accessibility are among the primary users of the WinEvents.</span></span>

<span data-ttu-id="bf77c-106">Nel contesto dell'accessibilità, i provider di automazione interfaccia utente e i server Microsoft Active Accessibility usano WinEvents per notificare ai client le modifiche apportate all'interfaccia utente di un'applicazione, ad esempio quando un elemento dell'interfaccia utente è stato creato o eliminato definitivamente oppure quando il nome, lo stato o il valore di un elemento è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="bf77c-106">In the context of accessibility, UI Automation providers and Microsoft Active Accessibility servers use WinEvents to notify clients of changes in an application UI, such as when a UI element has been created or destroyed, or when an element name, state, or value has changed.</span></span>

<span data-ttu-id="bf77c-107">In questa sezione vengono forniti suggerimenti, linee guida ed esempi per aiutare i client a gestire WinEvents e a consentire ai server di determinare quando attivare il WinEvent appropriato.</span><span class="sxs-lookup"><span data-stu-id="bf77c-107">This section provides suggestions, guidelines, and examples to help clients handle WinEvents and to help servers determine when to trigger the appropriate WinEvent.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bf77c-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="bf77c-108">In this section</span></span>

-   [<span data-ttu-id="bf77c-109">Che cosa sono WinEvents?</span><span class="sxs-lookup"><span data-stu-id="bf77c-109">What Are WinEvents?</span></span>](what-are-winevents.md)
-   [<span data-ttu-id="bf77c-110">Registrazione di una funzione hook</span><span class="sxs-lookup"><span data-stu-id="bf77c-110">Registering a Hook Function</span></span>](registering-a-hook-function.md)
-   [<span data-ttu-id="bf77c-111">Eventi a livello di sistema e di Object-Level</span><span class="sxs-lookup"><span data-stu-id="bf77c-111">System-Level and Object-Level Events</span></span>](system-level-and-object-level-events.md)
-   [<span data-ttu-id="bf77c-112">Funzioni hook nel contesto e out-of-context</span><span class="sxs-lookup"><span data-stu-id="bf77c-112">In-Context and Out-of-Context Hook Functions</span></span>](in-context-and-out-of-context-hook-functions.md)
-   [<span data-ttu-id="bf77c-113">Protezione contro la rientranza nelle funzioni hook</span><span class="sxs-lookup"><span data-stu-id="bf77c-113">Guarding Against Reentrancy in Hook Functions</span></span>](guarding-against-reentrancy-in-hook-functions.md)
-   [<span data-ttu-id="bf77c-114">Allocazione di ID WinEvent</span><span class="sxs-lookup"><span data-stu-id="bf77c-114">Allocation of WinEvent IDs</span></span>](allocation-of-winevent-ids.md)

<span data-ttu-id="bf77c-115">Per una panoramica del processo di notifica degli eventi in Microsoft Active Accessibility, vedere [winEvents](winevents-overview.md) nella [Panoramica tecnica](technical-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bf77c-115">For an overview of the event notification process in Microsoft Active Accessibility, see [WinEvents](winevents-overview.md) in the [Technical Overview](technical-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf77c-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf77c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf77c-117">Infrastruttura comune</span><span class="sxs-lookup"><span data-stu-id="bf77c-117">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




