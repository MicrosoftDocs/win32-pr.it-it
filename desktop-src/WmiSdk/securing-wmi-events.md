---
description: Gli eventi WMI vengono recapitati dal provider di eventi a un consumer temporaneo o permanente. Il sistema di eventi WMI usa il confronto dei descrittori di sicurezza per gli eventi e i SID dell'account utente per controllare l'accesso agli eventi.
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: Protezione degli eventi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226821"
---
# <a name="securing-wmi-events"></a><span data-ttu-id="058d6-104">Protezione degli eventi WMI</span><span class="sxs-lookup"><span data-stu-id="058d6-104">Securing WMI Events</span></span>

<span data-ttu-id="058d6-105">Gli eventi WMI vengono recapitati dal [*provider di eventi*](gloss-e.md) a un consumer [*temporaneo*](gloss-t.md) o [*permanente*](gloss-p.md) .</span><span class="sxs-lookup"><span data-stu-id="058d6-105">WMI events are delivered by the [*event provider*](gloss-e.md) to a [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md) consumer.</span></span> <span data-ttu-id="058d6-106">Il sistema di eventi WMI usa il confronto dei [*descrittori di sicurezza*](gloss-s.md) per gli eventi e i [*SID*](gloss-s.md) dell'account utente per controllare l'accesso agli eventi.</span><span class="sxs-lookup"><span data-stu-id="058d6-106">The WMI event system uses the comparison of [*security descriptors*](gloss-s.md) on events and user account [*SIDs*](gloss-s.md) to control event access.</span></span>

<span data-ttu-id="058d6-107">Gli eventi vengono recapitati sotto forma di istanza di una classe di evento, in genere, ma non necessariamente, derivati da un [**\_ \_ evento**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="058d6-107">Events are delivered in the form of an instance of an event class usually, but not necessarily, derived ultimately from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="058d6-108">WMI fornisce varie classi di evento generali nelle [classi di sistema WMI](wmi-system-classes.md), ad esempio [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md).</span><span class="sxs-lookup"><span data-stu-id="058d6-108">WMI supplies several general event classes in the [WMI System Classes](wmi-system-classes.md), such as [**\_\_InstanceModificationEvent**](--instancemodificationevent.md).</span></span> <span data-ttu-id="058d6-109">I provider possono anche fornire le proprie classi di evento.</span><span class="sxs-lookup"><span data-stu-id="058d6-109">Providers may also supply their own event classes.</span></span> <span data-ttu-id="058d6-110">Il [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) , ad esempio, dispone di classi di evento che segnalano la modifica di una chiave o di un valore del registro di sistema, ad esempio [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="058d6-110">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) has event classes that report the change of a registry key or value, such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="058d6-111">Negli argomenti seguenti vengono fornite informazioni sulla protezione del recapito di eventi per i provider e la ricezione di eventi in modo sicuro per gli script client e le applicazioni:</span><span class="sxs-lookup"><span data-stu-id="058d6-111">The following topics supply information about securing delivery of events for providers and receiving events securely for client scripts and applications:</span></span>

-   [<span data-ttu-id="058d6-112">Fornire eventi in modo sicuro</span><span class="sxs-lookup"><span data-stu-id="058d6-112">Providing Events Securely</span></span>](providing-events-securely.md)
-   [<span data-ttu-id="058d6-113">Ricezione di eventi in modo sicuro</span><span class="sxs-lookup"><span data-stu-id="058d6-113">Receiving Events Securely</span></span>](receiving-events-securely.md)

## <a name="related-topics"></a><span data-ttu-id="058d6-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="058d6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="058d6-115">Gestione della sicurezza WMI</span><span class="sxs-lookup"><span data-stu-id="058d6-115">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
