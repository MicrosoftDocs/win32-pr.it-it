---
title: L'interfaccia utente di Edge viene eliminato negli scenari "in-out-in" e "inerzia"
description: L'interfaccia utente di Edge viene eliminato negli scenari "in-out-in" e "inerzia"
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221986"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a><span data-ttu-id="51f3f-103">L'interfaccia utente di Edge viene eliminato negli scenari "in-out-in" e "inerzia"</span><span class="sxs-lookup"><span data-stu-id="51f3f-103">Edge UI is suppressed in “in-out-in” and “inertia” scenarios</span></span>

## <a name="platform"></a><span data-ttu-id="51f3f-104">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="51f3f-104">Platform</span></span>

<dl> <span data-ttu-id="51f3f-105">Client-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="51f3f-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="51f3f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51f3f-106">Description</span></span>

<span data-ttu-id="51f3f-107">Ci sono casi in cui gli utenti possono richiamare inavvertitamente l'interfaccia utente Edge (Charm, barra dell'app, cambio di app).</span><span class="sxs-lookup"><span data-stu-id="51f3f-107">There are some cases where users may unintentionally invoke Edge UI (Charms, App Bar, app switching).</span></span> <span data-ttu-id="51f3f-108">È stata introdotta una funzionalità che consente agli sviluppatori di progettare l'interfaccia utente per l'intero schermo senza apportare affordances (ad esempio, bordi) per impedire all'utente di raggiungere accidentalmente i bordi.</span><span class="sxs-lookup"><span data-stu-id="51f3f-108">We have introduced a feature to allow developers to design their UI for the whole screen without making affordances (for example, borders) to prevent the user from accidentally hitting the edges.</span></span>

<span data-ttu-id="51f3f-109">Esistono due casi che potrebbero condurre più spesso a inavvertitamente i bordi del bordo:</span><span class="sxs-lookup"><span data-stu-id="51f3f-109">There are two cases that might lead most often to inadvertent edge swipes:</span></span>

-   <span data-ttu-id="51f3f-110">In una rapida panoramica, la velocità e l'imprecisione dell'interazione possono occasionalmente comportarne il ritorno dal bordo dello schermo</span><span class="sxs-lookup"><span data-stu-id="51f3f-110">In fast panning, the speed and imprecision of the interaction can occasionally cause them to come in from the edge of the screen</span></span>
-   <span data-ttu-id="51f3f-111">Se gli utenti lasciano e rientrano rapidamente nell'area dello schermo mentre Inking con il dito, ad esempio, in un'app per la creazione di un disegno, questo comportamento in uscita può attivare erroneamente l'interfaccia utente di Edge e interrompere l'esperienza utente</span><span class="sxs-lookup"><span data-stu-id="51f3f-111">If users rapidly leave and re-enter the screen area while inking with their finger, for example, in a painting app, this in-out-in behavior can mistakenly trigger the Edge UI and interrupt the user experience</span></span>

<span data-ttu-id="51f3f-112">Per migliorare l'esperienza degli utenti e degli sviluppatori, l'interfaccia utente di Edge verrà ora rilevata in due istanze specifiche:</span><span class="sxs-lookup"><span data-stu-id="51f3f-112">To improve the user and developer experience, the Edge UI will now be suppressed in two specific instances:</span></span>

-   <span data-ttu-id="51f3f-113">Quando un utente esegue la panoramica in un'applicazione che supporta l'inerzia DManip e scorre all'esterno dello schermo mentre è in corso l'inerzia, l'interfaccia utente perimetrale non verrà richiamata entro una finestra di timeout</span><span class="sxs-lookup"><span data-stu-id="51f3f-113">When a user is panning in an application that supports DManip Inertia and swipes outside of the screen while inertia is occurring, the Edge UI will not be invoked within a timeout window</span></span>
-   <span data-ttu-id="51f3f-114">Nei dispositivi certificati, quando un utente scorre rapidamente dall'interno dello schermo all'esterno dello schermo e torna all'interno (movimento in uscita) all'interno di determinati parametri, l'interfaccia utente di Edge non verrà richiamata</span><span class="sxs-lookup"><span data-stu-id="51f3f-114">On certified devices, when a user quickly swipes from within the screen to outside the screen and back inside (in-out-in motion) within certain parameters, the Edge UI will not be invoked</span></span>

## <a name="manifestations"></a><span data-ttu-id="51f3f-115">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="51f3f-115">Manifestations</span></span>

<span data-ttu-id="51f3f-116">Quando si usa un'app, gli utenti possono scorrere rapidamente i dispositivi con una riduzione della chiamata al bordo involontario.</span><span class="sxs-lookup"><span data-stu-id="51f3f-116">Users quickly swiping against the edge while using an app will see a decrease in unintentional edge invocation.</span></span>

## <a name="solution"></a><span data-ttu-id="51f3f-117">Soluzione</span><span class="sxs-lookup"><span data-stu-id="51f3f-117">Solution</span></span>

<span data-ttu-id="51f3f-118">Gli sviluppatori devono tenere presenti queste mitigazioni e dovrebbero essere in grado di usare l'intero schermo senza temere che gli utenti inneschino accidentalmente l'interfaccia utente di Edge mentre interagiscono con l'applicazione lungo il perimetro.</span><span class="sxs-lookup"><span data-stu-id="51f3f-118">Developers should keep these mitigations in mind and should be able to use the full screen without fear that users will accidentally trigger the Edge UI while interacting with the application along the edge.</span></span>

 

 




