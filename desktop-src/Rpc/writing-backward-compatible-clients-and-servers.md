---
title: Scrittura di client e server compatibili con le versioni precedenti
description: In teoria, lo schema di controllo delle versioni di RPC consente di impedire la comunicazione non consentita tra server e client modificati e le relative controparti distribuite.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- RPC, procedure consigliate, compatibilità con le versioni precedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116781"
---
# <a name="writing-backward-compatible-clients-and-servers"></a><span data-ttu-id="7db8e-104">Scrittura di client e server compatibili con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="7db8e-104">Writing Backward Compatible Clients and Servers</span></span>

<span data-ttu-id="7db8e-105">In teoria, lo schema di controllo delle versioni di RPC consente di impedire la comunicazione non consentita tra server e client modificati e le relative controparti distribuite.</span><span class="sxs-lookup"><span data-stu-id="7db8e-105">In theory, the versioning scheme of RPC helps prevent miscommunication between modified servers and clients and their deployed counterparts.</span></span> <span data-ttu-id="7db8e-106">In pratica, tuttavia, gli sviluppatori devono spesso introdurre modifiche alle interfacce esistenti senza modificare la versione, perché i client e i server precedenti devono essere in grado di comunicare con quelli nuovi.</span><span class="sxs-lookup"><span data-stu-id="7db8e-106">In practice, however, developers frequently must introduce changes to existing interfaces without modifying the version, because previous clients and servers must be able to communicate with new ones.</span></span> <span data-ttu-id="7db8e-107">Si tratta di un problema di dimensioni maggiori per RPC standard rispetto a COM; l'esecuzione di query è un metodo naturale per la ricerca di interfacce supportate in COM, mentre nella gestione delle eccezioni RPC deve essere utilizzato per la copertura equivalente.</span><span class="sxs-lookup"><span data-stu-id="7db8e-107">This is a larger issue for standard RPC than for COM; querying is a natural way of searching for supported interfaces in COM, while in RPC exception handling must be used for equivalent coverage.</span></span>

<span data-ttu-id="7db8e-108">In questa sezione vengono descritte le procedure di programmazione RPC migliori per risolvere queste situazioni.</span><span class="sxs-lookup"><span data-stu-id="7db8e-108">This section discusses the best RPC programming practices for addressing these situations.</span></span> <span data-ttu-id="7db8e-109">Questa sezione è divisa negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7db8e-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="7db8e-110">Teoria del controllo delle versioni per RPC e COM</span><span class="sxs-lookup"><span data-stu-id="7db8e-110">The Versioning Theory for RPC and COM</span></span>](the-versioning-theory-for-rpc-and-com.md)
-   [<span data-ttu-id="7db8e-111">Modifica delle interfacce in modo compatibile con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="7db8e-111">Changing Interfaces in a Backward Compatible Manner</span></span>](changing-interfaces-in-a-backward-compatible-manner.md)
-   [<span data-ttu-id="7db8e-112">Esempi di modifiche incompatibili</span><span class="sxs-lookup"><span data-stu-id="7db8e-112">Examples of Incompatible Changes</span></span>](examples-of-incompatible-changes.md)

 

 




