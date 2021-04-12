---
title: Criteri per le voci del servizio dei nomi
description: Criteri per le voci del servizio di denominazione con RPC (Remote Procedure Call).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471454"
---
# <a name="criteria-for-name-service-entries"></a><span data-ttu-id="b78f0-103">Criteri per le voci del servizio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b78f0-103">Criteria for Name Service Entries</span></span>

<span data-ttu-id="b78f0-104">Quando si elaborano le voci del servizio di nome, vengono usati i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b78f0-104">The following criteria are used when processing name service entries:</span></span>

-   <span data-ttu-id="b78f0-105">Se si specifica un nome di voce non **null** per [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), tale voce sarà l'unica voce cercata per gli handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="b78f0-105">If you provide a non-**NULL** entry name for [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), that entry will be the only entry searched for binding handles.</span></span> <span data-ttu-id="b78f0-106">Se si passa **null**, verrà eseguita una ricerca in tutte le voci del dominio di accesso.</span><span class="sxs-lookup"><span data-stu-id="b78f0-106">If you pass **NULL**, all entries in your logon domain will be searched.</span></span> <span data-ttu-id="b78f0-107">Si noti che questo non include domini trusted.</span><span class="sxs-lookup"><span data-stu-id="b78f0-107">Note that this does not include trusted domains.</span></span>
-   <span data-ttu-id="b78f0-108">Se si fornisce un handle di interfaccia, gli handle di associazione vengono restituiti da una voce solo se la sezione dell'interfaccia della voce contiene una versione compatibile di tale UUID dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b78f0-108">If you provide an interface handle, binding handles are returned from an entry only if the interface section of the entry contains a compatible version of that interface UUID.</span></span> <span data-ttu-id="b78f0-109">Questo significa che il numero di versione principale deve essere uguale a quello dell'interfaccia UUID, mentre il numero di versione secondario deve essere uguale o maggiore di quello dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b78f0-109">That is, the major version number must be the same as your interface UUID, while the minor version number must be equal to or greater than yours.</span></span>
-   <span data-ttu-id="b78f0-110">Se si specifica un UUID per l'oggetto, gli handle di associazione vengono restituiti da una voce solo se la sezione UUID dell'oggetto della voce contiene tale UUID dell'oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="b78f0-110">If you provide an object UUID, binding handles are returned from an entry only if the object UUID section of the entry contains that particular object UUID.</span></span>

<span data-ttu-id="b78f0-111">Se una voce del servizio nome sopravvive ai criteri descritti in precedenza, vengono raccolti tutti gli handle di binding da tali voci.</span><span class="sxs-lookup"><span data-stu-id="b78f0-111">If a name service entry survives the criteria described above, all the binding handles from those entries are gathered.</span></span> <span data-ttu-id="b78f0-112">Gli handle con una sequenza di protocollo non supportata dal client vengono rimossi e gli handle rimanenti vengono restituiti all'utente come output di [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span><span class="sxs-lookup"><span data-stu-id="b78f0-112">Handles with a protocol sequence that is unsupported by the client are discarded and the remaining handles are returned to you as the output from [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span></span>

 

 




