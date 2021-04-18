---
description: Il servizio componenti in coda COM+ supporta completamente il concetto di partizioni. Ovvero, quando viene eseguito un componente in coda all'interno di una partizione, il messaggio viene accodato e il componente viene infine eseguito all'interno della partizione dei componenti.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Componenti e partizioni in coda COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589d7cb7c3e61be8ef53a248f990cde65447cf9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523282"
---
# <a name="com-queued-components-and-partitions"></a><span data-ttu-id="df1f4-104">Componenti e partizioni in coda COM+</span><span class="sxs-lookup"><span data-stu-id="df1f4-104">COM+ Queued Components and Partitions</span></span>

<span data-ttu-id="df1f4-105">Il servizio componenti in coda COM+ supporta completamente il concetto di partizioni.</span><span class="sxs-lookup"><span data-stu-id="df1f4-105">The COM+ queued components service fully supports the concept of partitions.</span></span> <span data-ttu-id="df1f4-106">Ovvero, quando viene eseguito un componente in coda all'interno di una partizione, il messaggio viene accodato e il componente viene infine eseguito all'interno della partizione del componente.</span><span class="sxs-lookup"><span data-stu-id="df1f4-106">That is, when a queued component within a partition is executed, the message is queued and the component is eventually executed within the component's partition.</span></span>

## <a name="queue-names-for-partitioned-components"></a><span data-ttu-id="df1f4-107">Nomi delle code per i componenti partizionati</span><span class="sxs-lookup"><span data-stu-id="df1f4-107">Queue Names for Partitioned Components</span></span>

<span data-ttu-id="df1f4-108">Tradizionalmente, il servizio componenti in coda usa il nome dell'applicazione come nome della coda.</span><span class="sxs-lookup"><span data-stu-id="df1f4-108">Traditionally, the queued components service uses the application name as the queue name.</span></span> <span data-ttu-id="df1f4-109">Ciò significa che in uno scenario senza partizioni, in cui esiste una sola istanza del nome di un'applicazione in un computer, il nome di ogni applicazione dispone di una propria coda di messaggi.</span><span class="sxs-lookup"><span data-stu-id="df1f4-109">This means that in a non-partitions scenario, where only one instance of an application name exists on a computer, each application name has its own message queue.</span></span>

<span data-ttu-id="df1f4-110">Nel caso di partizioni, tuttavia, in cui possono esistere più istanze dello stesso nome applicazione in un computer, il servizio componenti in coda utilizza la stessa coda per tutti i componenti in coda che condividono lo stesso nome di applicazione.</span><span class="sxs-lookup"><span data-stu-id="df1f4-110">In the case of partitions, however, where multiple instances of the same application name can exist on a computer, the queued components service uses the same queue for any queued components that share the same application name.</span></span>

## <a name="activating-queued-components"></a><span data-ttu-id="df1f4-111">Attivazione dei componenti in coda</span><span class="sxs-lookup"><span data-stu-id="df1f4-111">Activating Queued Components</span></span>

<span data-ttu-id="df1f4-112">Le stesse regole per la modalità di utilizzo dell'ID di partizione per attivare un componente non in coda si applicano a un componente in coda, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="df1f4-112">The same rules for how the partition ID is used to activate a non-queued component applies to a queued component, as follows:</span></span>

-   <span data-ttu-id="df1f4-113">Se viene usato un moniker per attivare il componente in coda e viene incluso un ID di partizione, questo ID di partizione viene usato per individuare la partizione.</span><span class="sxs-lookup"><span data-stu-id="df1f4-113">If a moniker is used to activate the queued component and a partition ID is included, this partition ID is used to locate the partition.</span></span> <span data-ttu-id="df1f4-114">Questo ID di partizione ha la precedenza su qualsiasi ID di partizione che potrebbe esistere nel contesto per il componente attivato.</span><span class="sxs-lookup"><span data-stu-id="df1f4-114">This partition ID takes precedence over any partition ID that might exist in the context for the component being activated.</span></span>
-   <span data-ttu-id="df1f4-115">Se non viene utilizzato alcun moniker per attivare il componente, viene utilizzato l'ID di partizione nel contesto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="df1f4-115">If no moniker is being used to activate the component, the partition ID that is in the object's context is used.</span></span>
-   <span data-ttu-id="df1f4-116">Se nel contesto dell'oggetto non è presente alcun ID partizione, viene utilizzato il mapping predefinito da utente a partizione all'interno Active Directory.</span><span class="sxs-lookup"><span data-stu-id="df1f4-116">If no partition ID exists in the object's context, the default user-to-partition mapping within Active Directory is used.</span></span>

> [!Note]  
> <span data-ttu-id="df1f4-117">Se un computer server è disconnesso dalla rete e se il mapping tra l'utente e il set di partizioni viene modificato mentre il server è disconnesso, la cache della partizione potrebbe contenere un mapping di set da utente a partizione obsoleto.</span><span class="sxs-lookup"><span data-stu-id="df1f4-117">If a server computer is disconnected from the network and if the user-to-partition set mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition set mapping.</span></span> <span data-ttu-id="df1f4-118">Questo potrebbe causare un errore di attivazione se il mapping del set da utente a partizione è il meccanismo utilizzato per attivare un componente.</span><span class="sxs-lookup"><span data-stu-id="df1f4-118">This could result in an activation error if user-to-partition set mapping is the mechanism used to activate a component.</span></span>

 

<span data-ttu-id="df1f4-119">Gli eventi COM+ sono completamente integrati nelle partizioni.</span><span class="sxs-lookup"><span data-stu-id="df1f4-119">COM+ events are fully integrated into partitions.</span></span> <span data-ttu-id="df1f4-120">Questo significa che un Sottoscrittore può sottoscrivere un server di pubblicazione la cui applicazione risiede all'interno di una partizione.</span><span class="sxs-lookup"><span data-stu-id="df1f4-120">This means that a subscriber can subscribe to a publisher whose application resides within a partition.</span></span> <span data-ttu-id="df1f4-121">Per consentire questa sottoscrizione, l'insieme di classi del Sottoscrittore include due proprietà correlate alle partizioni, ovvero un ID partizione della classe di evento e un ID applicazione della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="df1f4-121">To allow this subscription, the subscriber class collection includes two partition-related properties—an event class partition ID and an event class application ID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df1f4-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df1f4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df1f4-123">Limitazioni relative alla progettazione di applicazioni</span><span class="sxs-lookup"><span data-stu-id="df1f4-123">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="df1f4-124">Implementazione della partizione</span><span class="sxs-lookup"><span data-stu-id="df1f4-124">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="df1f4-125">Registrazione e attivazione di componenti nelle partizioni</span><span class="sxs-lookup"><span data-stu-id="df1f4-125">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="df1f4-126">Che cosa sono le partizioni COM+?</span><span class="sxs-lookup"><span data-stu-id="df1f4-126">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



