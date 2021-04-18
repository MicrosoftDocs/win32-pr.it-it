---
title: Funzionalità del modello di replica per Active Directory Domain Services
description: Il modello di replica utilizzato in Active Directory Domain Services viene definito uniformità a più master con la convergenza.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, modello di replica
- Funzionalità del modello di replica Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923c49dd648063ebd6afd086be3729f28f1e4080
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297736"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a><span data-ttu-id="a3309-105">Funzionalità del modello di replica per Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="a3309-105">Features of the Replication Model for Active Directory Domain Services</span></span>

<span data-ttu-id="a3309-106">Il modello di replica utilizzato in Active Directory Domain Services viene definito *uniformità a più master con la convergenza*.</span><span class="sxs-lookup"><span data-stu-id="a3309-106">The replication model used in Active Directory Domain Services is called *multi-master loose consistency with convergence*.</span></span> <span data-ttu-id="a3309-107">In questo modello la directory può avere molte repliche; un sistema di replica propaga le modifiche apportate in una determinata replica a tutte le altre repliche.</span><span class="sxs-lookup"><span data-stu-id="a3309-107">In this model, the directory can have many replicas; a replication system propagates changes made at any given replica to all other replicas.</span></span> <span data-ttu-id="a3309-108">Non è garantito che le repliche siano coerenti tra loro in un determinato momento ("coerenza sciolta"), in quanto le modifiche possono essere applicate a qualsiasi replica in qualsiasi momento ("multimaster").</span><span class="sxs-lookup"><span data-stu-id="a3309-108">The replicas are not guaranteed to be consistent with each other at any particular time ("loose consistency"), because changes can be applied to any replica at any time ("multi-master").</span></span> <span data-ttu-id="a3309-109">Se il sistema è autorizzato a raggiungere uno stato stabile, in cui non sono in corso nuovi aggiornamenti e tutti gli aggiornamenti precedenti sono stati completamente replicati, viene garantita la convergenza di tutte le repliche sullo stesso set di valori ("convergenza").</span><span class="sxs-lookup"><span data-stu-id="a3309-109">If the system is allowed to reach a steady state, in which no new updates are occurring and all previous updates have been completely replicated, all replicas are guaranteed to converge on the same set of values ("convergence").</span></span>

 

 




