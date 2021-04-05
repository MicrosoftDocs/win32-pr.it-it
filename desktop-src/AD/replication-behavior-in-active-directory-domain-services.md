---
title: Comportamento della replica in Active Directory Domain Services
description: Il comportamento della replica è coerente e prevedibile. dato un set di modifiche a una determinata replica, il risultato può essere stimato \ 8212; le modifiche verranno propagate a tutte le altre repliche.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, replica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41009a733f99366e499a25baca989f4f28794aea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855386"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a><span data-ttu-id="ebef4-104">Comportamento della replica in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="ebef4-104">Replication Behavior in Active Directory Domain Services</span></span>

<span data-ttu-id="ebef4-105">Il comportamento della replica è coerente e prevedibile. dato un set di modifiche a una determinata replica, il risultato può essere stimato: le modifiche verranno propagate a tutte le altre repliche.</span><span class="sxs-lookup"><span data-stu-id="ebef4-105">Replication behavior is consistent and predictable; given a set of changes to a given replica, the outcome can be predicted—the changes will be propagated to all other replicas.</span></span> <span data-ttu-id="ebef4-106">La definizione di un modello generale affidabile per la stima del momento in cui le modifiche verranno applicate a tutte le altre repliche o a una particolare replica non è possibile, perché lo stato futuro del sistema distribuito nel suo complesso non è noto.</span><span class="sxs-lookup"><span data-stu-id="ebef4-106">Devising a reliable general model for predicting when the changes will be applied at all other replicas, or at a particular replica, is impossible, because the future state of the distributed system as a whole cannot be known.</span></span> <span data-ttu-id="ebef4-107">Questa operazione viene definita "latenza non deterministica" e le applicazioni che usano la directory devono comprenderle e consentirne l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="ebef4-107">This is called "nondeterministic latency," and applications that use the directory must understand and allow for it.</span></span>

<span data-ttu-id="ebef4-108">La situazione non è così complessa in quanto potrebbe essere visualizzata.</span><span class="sxs-lookup"><span data-stu-id="ebef4-108">The situation is not as complex at it might appear.</span></span> <span data-ttu-id="ebef4-109">È necessario che un'applicazione soddisfi solo tre stati:</span><span class="sxs-lookup"><span data-stu-id="ebef4-109">There are only three states that an application must accommodate:</span></span>

-   <span data-ttu-id="ebef4-110">Sfasamento della versione: nessuna delle modifiche applicate a una determinata replica di origine è stata propagata a una replica di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="ebef4-110">Version Skew: None of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="ebef4-111">Un'applicazione che legge la replica di origine Visualizza la nuova versione delle informazioni, mentre un'applicazione che legge la destinazione Visualizza la versione precedente (o nulla se le nuove informazioni sono state aggiunte per la prima volta).</span><span class="sxs-lookup"><span data-stu-id="ebef4-111">An application reading the source replica sees the new version of the information, while an application reading the destination sees the old version (or nothing, if the new information was added for the first time).</span></span> <span data-ttu-id="ebef4-112">Lo sfasamento della versione si applica a tutti i consumer del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="ebef4-112">Version skew applies to all directory service consumers.</span></span>
-   <span data-ttu-id="ebef4-113">Aggiornamento parziale: alcune delle modifiche applicate a una determinata replica di origine sono state propagate a una determinata replica di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ebef4-113">Partial Update: Some of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="ebef4-114">Un'applicazione che legge la replica di origine Visualizza le nuove informazioni, mentre un'applicazione che legge la destinazione vede una combinazione di informazioni obsolete e nuove (o solo alcune delle nuove informazioni, se le nuove informazioni sono state aggiunte per la prima volta).</span><span class="sxs-lookup"><span data-stu-id="ebef4-114">An application reading the source replica sees the new information, while an application reading the destination sees a mix of old and new information (or only some of the new information, if the new information was added for the first time).</span></span> <span data-ttu-id="ebef4-115">L'aggiornamento parziale si applica ai consumer del servizio directory che usano due o più oggetti correlati per archiviare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="ebef4-115">Partial update applies to directory service consumers that use two or more related objects to store their information.</span></span>
-   <span data-ttu-id="ebef4-116">Stato completamente replicato: tutte le modifiche applicate a una determinata replica di origine sono state propagate a una determinata replica di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ebef4-116">Fully Replicated State: All of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="ebef4-117">Le applicazioni presenti nelle repliche di origine e di destinazione visualizzano le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="ebef4-117">Applications at the source and destination replicas see the same information.</span></span>

 

 




