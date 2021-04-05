---
title: Motivi per cui Active Directory Domain Services utilizza questo modello di replica
description: In questo argomento vengono illustrati i motivi del sistema in formato libero utilizzato da Active Directory Domain Services per un modello di replica.
ms.assetid: 202df900-6d03-4aa8-9099-016238059ef4
ms.tgt_platform: multiple
keywords:
- Modello di replica Active Directory, vantaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538fe291a04953d373ff3cd45cbd4693d3dafab4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855373"
---
# <a name="why-active-directory-domain-services-uses-this-replication-model"></a><span data-ttu-id="4d5cc-104">Motivi per cui Active Directory Domain Services utilizza questo modello di replica</span><span class="sxs-lookup"><span data-stu-id="4d5cc-104">Why Active Directory Domain Services Uses This Replication Model</span></span>

<span data-ttu-id="4d5cc-105">In questo argomento vengono illustrati i motivi del sistema in formato libero utilizzato da Active Directory Domain Services per un modello di replica.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-105">This topic explains the reasons for the free-form system used by Active Directory Domain Services for a replication model.</span></span>

<span data-ttu-id="4d5cc-106">Active Directory Domain Services sono un sistema in formato libero per i motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d5cc-106">Active Directory Domain Services are a free-form system for the following reasons:</span></span>

-   <span data-ttu-id="4d5cc-107">I clienti richiedono una soluzione altamente distribuita in cui le parti della directory possono essere distribuite tra le reti e gestite localmente.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-107">Customers require a highly distributed solution in which parts of the directory can be spread across their networks and administered locally.</span></span>
-   <span data-ttu-id="4d5cc-108">I clienti di grandi dimensioni crescono spesso fino a milioni di oggetti, centinaia o migliaia di repliche o entrambi.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-108">Large customers often grow to millions of objects, hundreds or thousands of replicas, or both.</span></span>
-   <span data-ttu-id="4d5cc-109">Molte reti clienti forniscono solo la connettività intermittente ad alcune località; ad esempio, le piattaforme di drill-Oil remoto e vengono fornite in mare, quindi il sistema deve essere a tolleranza di operazioni parzialmente connesse o disconnesse.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-109">Many customer networks provide only intermittent connectivity to some locations; for example, remote oil drilling platforms and ships at sea, so the system must be tolerant of partly connected or disconnected operations.</span></span>

<span data-ttu-id="4d5cc-110">Non esiste alcun modo per garantire la consapevolezza completa dello stato corrente o futuro di un sistema distribuito, perché la conoscenza delle modifiche di stato deve essere propagata e la propagazione richiede tempo, durante il quale possono verificarsi più modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-110">There is no way to guarantee complete awareness of the current or future state of a distributed system because knowledge of state changes must be propagated and propagation takes time, during which more state changes may occur.</span></span>

<span data-ttu-id="4d5cc-111">I sistemi strettamente collegati gestiscono l'incertezza tentando di eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-111">Tightly coupled systems handle uncertainty by attempting to eliminate it.</span></span> <span data-ttu-id="4d5cc-112">Questa operazione viene eseguita tramite vincoli sugli aggiornamenti, che richiedono che tutti i nodi o la maggior parte dei nodi siano disponibili prima di poter eseguire gli aggiornamenti, usando schemi di blocco distribuiti o un singolo master per le risorse critiche, vincolando la correttezza di tutti i nodi o una combinazione di queste tecniche.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-112">This is accomplished through constraints on updates, requiring all nodes or some majority of nodes to be available before updates can be performed, using distributed locking schemes or single-mastering for critical resources, constraining all nodes to be well-connected, or some combination of these techniques.</span></span> <span data-ttu-id="4d5cc-113">I nodi di calcolo più strettamente collegati in un sistema distribuito sono, minore è il limite di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-113">The more tightly coupled the computing nodes in a distributed system are, the lower the scaling limit.</span></span>

<span data-ttu-id="4d5cc-114">I sistemi a formato libero gestiscono l'incertezza grazie alla tolleranza.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-114">Free-form systems handle uncertainty by tolerating it.</span></span> <span data-ttu-id="4d5cc-115">Un sistema in formato libero consente ai nodi di avere visualizzazioni diverse dello stato generale del sistema e fornisce gli algoritmi per la risoluzione dei conflitti.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-115">A free-form system enables the nodes to have differing views of the overall system state and provides algorithms for resolving conflicts.</span></span>

<span data-ttu-id="4d5cc-116">Le soluzioni strettamente associate sono state rifiutate come non idonee per Active Directory Domain Services a causa dei requisiti per l'amministrazione locale, l'operazione disconnessa e la scalabilità a un numero molto elevato di nodi.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-116">Tightly coupled solutions were rejected as unsuitable for Active Directory Domain Services because of the requirements for local administration, disconnected operation, and scalability to very large numbers of nodes.</span></span> <span data-ttu-id="4d5cc-117">Il modello a regime di controllo libero scelto, la coerenza di più master sciolto con la convergenza, soddisfa tutti i requisiti.</span><span class="sxs-lookup"><span data-stu-id="4d5cc-117">The loosely coupled model chosen, multi-master loose consistency with convergence, satisfies all requirements.</span></span>

 

 




