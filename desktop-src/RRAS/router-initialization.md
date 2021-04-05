---
title: Inizializzazione router
description: Le informazioni di configurazione per il router, i gestori del router e i protocolli/client di routing sono divise in informazioni globali e per informazioni sull'interfaccia e vengono archiviate nel registro di sistema e nel file di rubrica del router, router. pbk.
ms.assetid: c54541c1-6508-448a-a211-5fca634a184a
keywords:
- router RRAS, inizializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f4d45c10ef7b44b6dfe9d2d84149c77c81c5752
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707048"
---
# <a name="router-initialization"></a><span data-ttu-id="fac93-104">Inizializzazione router</span><span class="sxs-lookup"><span data-stu-id="fac93-104">Router Initialization</span></span>

<span data-ttu-id="fac93-105">Le informazioni di configurazione per il router, i gestori del router e i protocolli/client di routing sono divise in informazioni globali e per informazioni sull'interfaccia e vengono archiviate nel registro di sistema e nel file di rubrica del router, router. pbk.</span><span class="sxs-lookup"><span data-stu-id="fac93-105">Configuration information for the router, the router managers and the routing protocols/clients is divided into global information and per interface information and is stored in the registry and the router's phone-book file, Router.pbk.</span></span>

<span data-ttu-id="fac93-106">All'avvio del processo del router, DIM (Dynamic Interface Manager) legge la configurazione del router dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fac93-106">When the router process starts, DIM (Dynamic Interface Manager) reads the router configuration from the registry.</span></span> <span data-ttu-id="fac93-107">DIM crea le interfacce specificate dalle informazioni sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fac93-107">DIM creates the interfaces that are specified by the interface information.</span></span>

<span data-ttu-id="fac93-108">DIM consente inoltre di recuperare le informazioni di gestione router globali.</span><span class="sxs-lookup"><span data-stu-id="fac93-108">DIM also retrieves the global router manager information.</span></span> <span data-ttu-id="fac93-109">DIM avvia le gestioni router corrispondenti a queste informazioni e le passa alle informazioni.</span><span class="sxs-lookup"><span data-stu-id="fac93-109">DIM starts the router managers that correspond to this information, and passes them the information.</span></span> <span data-ttu-id="fac93-110">Se, ad esempio, DIM trova le informazioni globali per gestione router IP nel registro di sistema, DIM avvia Gestione router IP e le passa alle informazioni globali.</span><span class="sxs-lookup"><span data-stu-id="fac93-110">For example, if DIM finds global information for the IP router manager in the registry, DIM starts the IP router manager and passes it the global information.</span></span> <span data-ttu-id="fac93-111">Se nel registro di sistema non sono presenti informazioni globali per un determinato gestore di router, DIM non avvia tale gestore di router.</span><span class="sxs-lookup"><span data-stu-id="fac93-111">If no global information is present in the registry for a particular router manager, DIM does not start that router manager.</span></span>

<span data-ttu-id="fac93-112">I gestori di router esaminano le informazioni globali ricevute da DIM.</span><span class="sxs-lookup"><span data-stu-id="fac93-112">The router managers examine the global information received from DIM.</span></span> <span data-ttu-id="fac93-113">Se Gestione router trova informazioni specifiche per un particolare client all'interno delle informazioni globali, gestione router carica la DLL per il client (ad esempio IpNAT.dll) e inizializza il client chiamando le funzioni [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) e [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) del client.</span><span class="sxs-lookup"><span data-stu-id="fac93-113">If the router manager finds information specific to a particular client within the global information, the router manager loads the DLL for the client (for example IpNAT.dll) and initializes the client by calling the client's [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol) and [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) functions.</span></span> <span data-ttu-id="fac93-114">Gestione router passa al client le informazioni globali specifiche del client nella chiamata a [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span><span class="sxs-lookup"><span data-stu-id="fac93-114">The router manager passes the client-specific global information to the client in the call to [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol).</span></span>

<span data-ttu-id="fac93-115">In ogni fase, le informazioni passate all'entità successiva sono opache per l'entità che lo precede.</span><span class="sxs-lookup"><span data-stu-id="fac93-115">At each stage, the information being passed to the next entity is opaque to the entity preceding it.</span></span> <span data-ttu-id="fac93-116">Ovvero DIM non interpreta le informazioni globali per gestione router IP, oltre al fatto che le informazioni sono destinate a gestione router IP.</span><span class="sxs-lookup"><span data-stu-id="fac93-116">That is, DIM does not interpret the global information for the IP Router Manager, beyond the fact that the information is meant for the IP Router Manager.</span></span> <span data-ttu-id="fac93-117">Analogamente, gestione router IP non interpreta le informazioni specifiche di OSPF oltre al fatto che si tratta di informazioni OSPF.</span><span class="sxs-lookup"><span data-stu-id="fac93-117">Similarly, the IP Router Manager does not interpret the OSPF specific information beyond the fact that it is OSPF information.</span></span>

 

 




