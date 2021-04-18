---
description: Il Distributed Transaction Coordinator (DTC) consente transazioni distribuite o transazioni controllate da più gestori di risorse in uno o più sistemi. Per eseguire questa operazione, KTM e DTC interagiscono tra loro.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interoperabilità con altre funzionalità di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3aeac3d920b408a9a18c32eab83cf747525e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314306"
---
# <a name="interoperability-with-other-windows-features"></a><span data-ttu-id="06e08-104">Interoperabilità con altre funzionalità di Windows</span><span class="sxs-lookup"><span data-stu-id="06e08-104">Interoperability With Other Windows Features</span></span>

<span data-ttu-id="06e08-105">Il [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) consente *transazioni distribuite* o transazioni controllate da più gestori di risorse in uno o più sistemi.</span><span class="sxs-lookup"><span data-stu-id="06e08-105">The [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) enables *distributed transactions*, or transactions that are under the control of multiple resource managers on one or more systems.</span></span> <span data-ttu-id="06e08-106">Per eseguire questa operazione, KTM e DTC interagiscono tra loro.</span><span class="sxs-lookup"><span data-stu-id="06e08-106">KTM and DTC work closely together to accomplish this.</span></span>

<span data-ttu-id="06e08-107">COM+ espone un modello dichiarativo per la programmazione transazionale.</span><span class="sxs-lookup"><span data-stu-id="06e08-107">COM+ exposes a declarative model for transactional programming.</span></span> <span data-ttu-id="06e08-108">In altre parole, il programmatore dichiara la misura in cui un oggetto può sfruttare le transazioni e il runtime COM+ gestisce le transazioni per conto dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="06e08-108">In other words, the programmer declares the extent to which an object can take advantage of transactions, and the COM+ runtime manages the transactions on the object's behalf.</span></span> <span data-ttu-id="06e08-109">Un oggetto, ad esempio, può essere dichiarato per partecipare a una transazione solo se ne esiste già uno, per richiedere una transazione (ne viene creato uno se non esiste già), per richiedere una nuova transazione (uno viene creato indipendentemente dal fatto che ne esista già uno) oppure non è transazionale.</span><span class="sxs-lookup"><span data-stu-id="06e08-109">For example, an object can be declared to participate in a transaction only if one already exists, to require a transaction (one is created if it does not already exist), to require a new transaction (one is created regardless of whether one already exists), or is not transactional.</span></span> <span data-ttu-id="06e08-110">Queste transazioni gestite in modo dichiarativo vengono utilizzate automaticamente per le connessioni al database create da oggetti COM+ che sono in esecuzione nel contesto di una transazione.</span><span class="sxs-lookup"><span data-stu-id="06e08-110">These declaratively-managed transactions are automatically used on database connections created by COM+ objects that are executing in the context of a transaction.</span></span>

 

 
