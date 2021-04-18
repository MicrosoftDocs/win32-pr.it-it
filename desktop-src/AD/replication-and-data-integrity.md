---
title: Replica e integrità dei dati
description: Active Directory Domain Services fornire aggiornamenti multimaster.
ms.assetid: 99d35e16-9d1e-40d9-b1b0-600966165e45
ms.tgt_platform: multiple
keywords:
- Active Directory, utilizzo, replica e integrità dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499f7e2c3193a280d009f53521e7a94fa3b89c5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297721"
---
# <a name="replication-and-data-integrity"></a><span data-ttu-id="27e42-104">Replica e integrità dei dati</span><span class="sxs-lookup"><span data-stu-id="27e42-104">Replication and Data Integrity</span></span>

<span data-ttu-id="27e42-105">Active Directory Domain Services fornire *aggiornamenti multimaster*.</span><span class="sxs-lookup"><span data-stu-id="27e42-105">Active Directory Domain Services provide *multi-master update*.</span></span> <span data-ttu-id="27e42-106">L'aggiornamento multimaster indica che tutte le repliche complete di una determinata partizione sono scrivibili (le repliche parziali nei server di catalogo globale non sono scrivibili). L'aggiornamento multimaster indica che gli aggiornamenti non vengono bloccati anche quando alcune repliche sono inutilizzabili.</span><span class="sxs-lookup"><span data-stu-id="27e42-106">Multi-master update means that all full replicas of a given partition are writable (the partial replicas on global catalog servers are not writable.) Multi-master update means that updates are not blocked even when some replicas are inoperable.</span></span> <span data-ttu-id="27e42-107">Il server di Active Directory propaga le modifiche dalla replica aggiornata a tutte le altre repliche.</span><span class="sxs-lookup"><span data-stu-id="27e42-107">The Active Directory server propagates the changes from the updated replica to all other replicas.</span></span> <span data-ttu-id="27e42-108">La replica è automatica e trasparente.</span><span class="sxs-lookup"><span data-stu-id="27e42-108">Replication is automatic and transparent.</span></span>

<span data-ttu-id="27e42-109">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="27e42-109">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="27e42-110">Il modello di replica in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="27e42-110">The Replication Model in Active Directory Domain Services</span></span>](replication-model-in-active-directory-domain-services.md)
-   [<span data-ttu-id="27e42-111">Comportamento della replica in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="27e42-111">Replication Behavior in Active Directory Domain Services</span></span>](replication-behavior-in-active-directory-domain-services.md)
-   [<span data-ttu-id="27e42-112">Rilevamento ed evitare la latenza di replica</span><span class="sxs-lookup"><span data-stu-id="27e42-112">Detecting and Avoiding Replication Latency</span></span>](detecting-and-avoiding-replication-latency.md)

 

 




