---
title: Pubblicazione in un contenitore di sistema di dominio
description: Il contenitore di sistema di una partizione di dominio include informazioni operative per dominio.
ms.assetid: 18bb3409-774e-42d9-8f27-6c582d74ca86
ms.tgt_platform: multiple
keywords:
- Pubblicazione in un dominio di Active Directory del contenitore di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf7d1febd91e3540c7bc2002a36d33346820344
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855390"
---
# <a name="publishing-in-a-domain-system-container"></a><span data-ttu-id="225f4-104">Pubblicazione in un contenitore di sistema di dominio</span><span class="sxs-lookup"><span data-stu-id="225f4-104">Publishing in a Domain System Container</span></span>

<span data-ttu-id="225f4-105">Il contenitore di sistema di una partizione di dominio include informazioni operative per dominio.</span><span class="sxs-lookup"><span data-stu-id="225f4-105">The System container of a domain partition holds per-domain operational information.</span></span> <span data-ttu-id="225f4-106">Sono inclusi i criteri di sicurezza locali predefiniti, il rilevamento dei collegamenti di file, le riunioni di rete e i contenitori per i punti di connessione RpcNs (registrazione e risoluzione) di Windows Sockets (RnR) e del servizio nome RPC.</span><span class="sxs-lookup"><span data-stu-id="225f4-106">This includes the default local security policy, file link tracking, network meetings, and containers for Windows Sockets registration and resolution (RnR) and RPC name service (RpcNs) connection points.</span></span> <span data-ttu-id="225f4-107">Il contenitore di sistema è nascosto, per impostazione predefinita, e rappresenta una comoda posizione per archiviare gli oggetti di interesse per gli amministratori, ma non per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="225f4-107">The system container is hidden, by default, and provides a convenient place for storing objects that are of interest to administrators, but not to end users.</span></span>

<span data-ttu-id="225f4-108">I servizi non collegati a un singolo host possono voler creare i convergenza nel contenitore di sistema di una partizione di dominio.</span><span class="sxs-lookup"><span data-stu-id="225f4-108">Services that are not tied to a single host may want to create their SCPs under the System container of a domain partition.</span></span> <span data-ttu-id="225f4-109">Questa alternativa può essere utile per i servizi con repliche installate in più host, ogni replica che fornisce servizi identici ai client di tutto il dominio.</span><span class="sxs-lookup"><span data-stu-id="225f4-109">This alternative can be useful for services with replicas installed on multiple hosts, each replica providing identical services to clients throughout the domain.</span></span> <span data-ttu-id="225f4-110">Consente di raggruppare tutti gli oggetti per il servizio replicato in un singolo contenitore.</span><span class="sxs-lookup"><span data-stu-id="225f4-110">It enables you to group all the objects for the replicated service under a single container.</span></span>

<span data-ttu-id="225f4-111">I servizi che creano oggetti specifici del servizio nel contenitore di sistema devono eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="225f4-111">Services that create service-specific objects in the System container must do the following:</span></span>

1.  <span data-ttu-id="225f4-112">Creare un sottocontenitore del **contenitore** della classe di oggetti come elemento figlio immediato del contenitore di sistema.</span><span class="sxs-lookup"><span data-stu-id="225f4-112">Create a sub-container of object class **container** as an immediate child of the System container.</span></span> <span data-ttu-id="225f4-113">Assegnare a questo sottocontenitore un nome che lo identifichi chiaramente come pertinente per il servizio.</span><span class="sxs-lookup"><span data-stu-id="225f4-113">Give this sub-container a name that clearly identifies it as pertaining to the service.</span></span>
2.  <span data-ttu-id="225f4-114">Creare gli oggetti correlati al servizio in questo sottocontenitore.</span><span class="sxs-lookup"><span data-stu-id="225f4-114">Create the service-related objects in this sub-container.</span></span> <span data-ttu-id="225f4-115">Ad esempio, NetMeeting usa il contenitore meetings per pubblicare gli oggetti della riunione di rete.</span><span class="sxs-lookup"><span data-stu-id="225f4-115">For example, NetMeeting uses the Meetings container to publish network meeting objects.</span></span>

<span data-ttu-id="225f4-116">Un fornitore con più prodotti può utilizzare una strategia simile per raggruppare gli oggetti correlati ai servizi per tutti i prodotti.</span><span class="sxs-lookup"><span data-stu-id="225f4-116">A vendor with multiple products can use a similar strategy to group service-related objects for all of its products.</span></span> <span data-ttu-id="225f4-117">In questo caso, è possibile creare un oggetto **contenitore** con un nome che identifichi chiaramente il fornitore; quindi creare oggetti **contenitore** per ogni servizio come elementi figlio del contenitore Fornitore.</span><span class="sxs-lookup"><span data-stu-id="225f4-117">In this case, you could create a **container** object with a name that clearly identifies the vendor; then create **container** objects for each service as children of the vendor container.</span></span> <span data-ttu-id="225f4-118">Creare il contenitore specifico del fornitore come figlio del contenitore di sistema.</span><span class="sxs-lookup"><span data-stu-id="225f4-118">Create the vendor-specific container as a child of the System container.</span></span>

 

 




