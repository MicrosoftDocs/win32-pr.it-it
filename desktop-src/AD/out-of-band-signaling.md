---
title: Segnalazione fuori banda
description: Le applicazioni cooperating che condividono dati comuni mediante la directory possono utilizzare la segnalazione fuori banda per evitare l'asimmetria di versione e gli aggiornamenti parziali.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044103"
---
# <a name="out-of-band-signaling"></a><span data-ttu-id="d6ebb-103">Segnalazione fuori banda</span><span class="sxs-lookup"><span data-stu-id="d6ebb-103">Out-of-Band Signaling</span></span>

<span data-ttu-id="d6ebb-104">Le applicazioni cooperating che condividono dati comuni mediante la directory possono utilizzare la segnalazione fuori banda per evitare l'asimmetria di versione e gli aggiornamenti parziali.</span><span class="sxs-lookup"><span data-stu-id="d6ebb-104">Cooperating applications that share common data using the directory can use out-of-band signaling to avoid both version skew and partial updates.</span></span> <span data-ttu-id="d6ebb-105">In poche parole, le applicazioni cooperative utilizzano un meccanismo separato dalla replica di directory per informare le modifiche nei dati comuni condivisi.</span><span class="sxs-lookup"><span data-stu-id="d6ebb-105">Put simply, the cooperating applications use a mechanism separate from directory replication to inform each other of changes in the shared common data.</span></span> <span data-ttu-id="d6ebb-106">La segnalazione fuori banda è più efficace se usata in combinazione con un meccanismo di controllo delle versioni, in modo da consentire al partner di rilevare la modifica per notificare ai partner remoti la versione dei dati condivisi da attendere.</span><span class="sxs-lookup"><span data-stu-id="d6ebb-106">Out-of-band signaling is most effective when used in combination with a versioning mechanism—this allows the partner detecting the change to notify remote partners what version of the shared data to wait for.</span></span>

<span data-ttu-id="d6ebb-107">Tornando all'esempio di RPC indicato nella sezione "asimmetria della versione" del [comportamento della replica in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), il server RPC potrebbe richiamarlo nei client connessi per informare gli utenti del passaggio a un nuovo server: "lo spostamento verrà eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6ebb-107">Returning to the RPC example given in the "Version Skew" section of [Replication Behavior in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), the RPC server could call back into connected clients to inform them of the move to a new server: "I am going to move.</span></span> <span data-ttu-id="d6ebb-108">In base alla replica, il nuovo indirizzo viene portato a breve "in modo che il client possa gestire il periodo di transizione.</span><span class="sxs-lookup"><span data-stu-id="d6ebb-108">Please stand by, replication will bring you the new address shortly" so that the client can handle the transition period.</span></span>

<span data-ttu-id="d6ebb-109">Le applicazioni che richiedono criteri identici per poter comunicare tra loro possono utilizzare la segnalazione fuori banda per assicurarsi che un nuovo criterio non venga utilizzato fino a quando non tutte le parti coinvolte lo ricevono.</span><span class="sxs-lookup"><span data-stu-id="d6ebb-109">Applications that require identical policies to be in force in order to communicate with each other can use out-of-band signaling to ensure that a new policy is not employed until all involved parties have received it.</span></span> <span data-ttu-id="d6ebb-110">Se, ad esempio, i criteri di Internet Protocol Security (IPsec) tra due computer vengono modificati, un agente nel computer di origine potrebbe contattare un agente nel computer di destinazione per negoziare l'applicazione dei criteri modificati, con la macchina di origine che ritarda l'applicazione fino a quando il computer di destinazione non ha ricevuto anche il nuovo criterio.</span><span class="sxs-lookup"><span data-stu-id="d6ebb-110">For example, if the Internet Protocol security (IPsec) policy between two machines is changed, an agent on the source machine could contact an agent on the destination machine to negotiate the application of the changed policy, with the source machine delaying application until the destination machine has received the new policy as well.</span></span>

 

 




