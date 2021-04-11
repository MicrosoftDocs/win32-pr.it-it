---
description: Utilizzo di COM+ CRM in un ambiente cluster
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Utilizzo di COM+ CRM in un ambiente cluster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a05ff281748c35128349ef5d0d0f43d7beae86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342241"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a><span data-ttu-id="ac8db-103">Utilizzo di COM+ CRM in un ambiente cluster</span><span class="sxs-lookup"><span data-stu-id="ac8db-103">Using the COM+ CRM in a Cluster Environment</span></span>

<span data-ttu-id="ac8db-104">Quando si sviluppano COM+ dispongono per lavorare negli ambienti cluster, il fattore principale da considerare è se un CRM specifico è interessato da quale nodo del cluster sta operando.</span><span class="sxs-lookup"><span data-stu-id="ac8db-104">When developing COM+ CRMs to work in cluster environments, the main factor to consider is whether a specific CRM cares which node of the cluster it is operating on.</span></span> <span data-ttu-id="ac8db-105">Ad esempio, se la risorsa gestita da CRM è il computer file system o il registro di sistema, tutte le modifiche sono specifiche del nodo in cui è in esecuzione l'applicazione del server CRM.</span><span class="sxs-lookup"><span data-stu-id="ac8db-105">For example, if the resource managed by the CRM is the machine file system or registry, any changes are specific to the node that the CRM server application is running on at the time.</span></span> <span data-ttu-id="ac8db-106">In questo caso, non è consigliabile eseguire il failover dell'applicazione server CRM in un altro nodo.</span><span class="sxs-lookup"><span data-stu-id="ac8db-106">In this case, failover of the CRM server application to another node would not be desirable.</span></span> <span data-ttu-id="ac8db-107">In un caso diverso, in cui il CRM gestisce alcune risorse comuni al cluster, è utile eseguire il failover dell'applicazione server CRM in un altro nodo.</span><span class="sxs-lookup"><span data-stu-id="ac8db-107">In a different case, where the CRM is managing some resource common to the cluster, failover of the CRM server application to another node is useful.</span></span>

<span data-ttu-id="ac8db-108">Il percorso predefinito della directory per i file di log di CRM è la stessa directory del file di log DTC.</span><span class="sxs-lookup"><span data-stu-id="ac8db-108">The default directory location for CRM log files is the same directory as the DTC log file.</span></span> <span data-ttu-id="ac8db-109">Nei cluster, il file di log DTC si trova su un disco condiviso di cui è stato eseguito il failover tra i nodi del cluster.</span><span class="sxs-lookup"><span data-stu-id="ac8db-109">On clusters, the DTC log file is placed on a shared disk that is failed over between the nodes of the cluster.</span></span> <span data-ttu-id="ac8db-110">Questo significa che il comportamento predefinito per le applicazioni server CRM consiste nel failover tra i nodi del cluster.</span><span class="sxs-lookup"><span data-stu-id="ac8db-110">This means that the default behavior for CRM server applications is to failover between nodes of the cluster.</span></span> <span data-ttu-id="ac8db-111">Di conseguenza, se un CRM specifico richiede il comportamento alternativo del failover tra i nodi, è necessario modificare il percorso del file di log CRM per quella particolare applicazione del server CRM.</span><span class="sxs-lookup"><span data-stu-id="ac8db-111">Therefore, if a specific CRM requires the alternative behavior of not failing over between nodes, the location of the CRM log file for that particular CRM server application should be changed.</span></span>

<span data-ttu-id="ac8db-112">Se, inoltre, è necessario il failover per l'applicazione CRM, è necessario configurarlo come applicazione generica in un gruppo di cluster.</span><span class="sxs-lookup"><span data-stu-id="ac8db-112">In addition, if failover is required for the CRM application, it should be configured as a generic application in a cluster group.</span></span> <span data-ttu-id="ac8db-113">La dipendenza deve essere DTC.</span><span class="sxs-lookup"><span data-stu-id="ac8db-113">Its dependency should be DTC.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac8db-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ac8db-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac8db-115">Concetti Gestione risorse di compensazione COM+</span><span class="sxs-lookup"><span data-stu-id="ac8db-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



