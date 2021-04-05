---
title: Client Gestione gruppi multicast
description: Un client è un'entità che chiama una funzione MGM, ad esempio un protocollo di routing o un'applicazione amministrativa.
ms.assetid: 98d13b48-9f1d-4649-a5a3-03926c7facee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5f2a8ba63903c084547e3d04ea04474171651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714065"
---
# <a name="multicast-group-manager-client"></a><span data-ttu-id="6525f-103">Client Gestione gruppi multicast</span><span class="sxs-lookup"><span data-stu-id="6525f-103">Multicast Group Manager Client</span></span>

<span data-ttu-id="6525f-104">Un client è un'entità che chiama una funzione MGM, ad esempio un protocollo di routing o un'applicazione amministrativa.</span><span class="sxs-lookup"><span data-stu-id="6525f-104">A client is an entity that calls an MGM function, such as a routing protocol or an administrative application.</span></span>

<span data-ttu-id="6525f-105">L'API MGM viene utilizzata principalmente dai protocolli di routing multicast.</span><span class="sxs-lookup"><span data-stu-id="6525f-105">The MGM API is used primarily by multicast routing protocols.</span></span> <span data-ttu-id="6525f-106">Gli sviluppatori di protocolli di routing multicast usano l'API MGM per:</span><span class="sxs-lookup"><span data-stu-id="6525f-106">Developers of multicast routing protocols use the MGM API to:</span></span>

-   <span data-ttu-id="6525f-107">Mantieni l'appartenenza al gruppo</span><span class="sxs-lookup"><span data-stu-id="6525f-107">Maintain group membership</span></span>
-   <span data-ttu-id="6525f-108">Controllare la proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="6525f-108">Control interface ownership</span></span>
-   <span data-ttu-id="6525f-109">Ricevere notifiche da Gestione gruppi multicast per le richieste di altri protocolli di routing multicast per i dati multicast</span><span class="sxs-lookup"><span data-stu-id="6525f-109">Receive notifications from the multicast group manager regarding other multicast routing protocols' requests for multicast data</span></span>

<span data-ttu-id="6525f-110">Le applicazioni amministrative specifiche che devono monitorare le voci di inoltri multicast (MFE) possono eseguire questa operazione senza aggiungere o rimuovere l'appartenenza al gruppo.</span><span class="sxs-lookup"><span data-stu-id="6525f-110">Specific administrative applications that must monitor multicast forwarding entries (MFEs) can do so without adding or removing group membership.</span></span> <span data-ttu-id="6525f-111">Gli sviluppatori di applicazioni amministrative utilizzano funzioni MGM specifiche per esaminare le informazioni in MFE.</span><span class="sxs-lookup"><span data-stu-id="6525f-111">Administrative application developers use specific MGM functions to review information in MFEs.</span></span>

> [!Note]  
> <span data-ttu-id="6525f-112">I protocolli di routing multicast accedono anche a MFE.</span><span class="sxs-lookup"><span data-stu-id="6525f-112">Multicast routing protocols also access MFEs.</span></span>

 

<span data-ttu-id="6525f-113">Un MFE sta inviando informazioni di cui il gestore del gruppo multicast crea in base all'appartenenza al gruppo.</span><span class="sxs-lookup"><span data-stu-id="6525f-113">An MFE is forwarding information that the multicast group manager creates based on group membership.</span></span> <span data-ttu-id="6525f-114">I MFE recuperati dal gestore del gruppo multicast possono fornire informazioni statistiche.</span><span class="sxs-lookup"><span data-stu-id="6525f-114">The MFEs that are retrieved from the multicast group manager can provide statistical information.</span></span> <span data-ttu-id="6525f-115">Un'applicazione amministrativa può quindi utilizzare queste informazioni per determinare le azioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="6525f-115">An administrative application can then use this information to determine the appropriate actions.</span></span> <span data-ttu-id="6525f-116">Ad esempio, un'applicazione amministrativa può eseguire azioni basate sul volume di pacchetti in un'interfaccia specifica.</span><span class="sxs-lookup"><span data-stu-id="6525f-116">For example, an administrative application could perform actions that are based on the volume of packets on a specific interface.</span></span>

 

 




