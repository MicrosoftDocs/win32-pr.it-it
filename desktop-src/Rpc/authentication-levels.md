---
title: Livelli di autenticazione
description: Microsoft RPC offre più livelli di autenticazione.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221381"
---
# <a name="authentication-levels"></a><span data-ttu-id="1ea11-103">Livelli di autenticazione</span><span class="sxs-lookup"><span data-stu-id="1ea11-103">Authentication Levels</span></span>

<span data-ttu-id="1ea11-104">Microsoft RPC offre più livelli di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="1ea11-104">Microsoft RPC provides multiple levels of authentication.</span></span> <span data-ttu-id="1ea11-105">A seconda del livello di autenticazione, è possibile verificare l'origine del traffico (l'entità di sicurezza che ha inviato il traffico) quando viene stabilita la connessione, quando il client avvia una nuova chiamata di procedura remota o durante ogni scambio di pacchetti tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="1ea11-105">Depending on the authentication level, the origin of the traffic (which security principal sent the traffic) can be verified when the connection is established, when the client starts a new remote procedure call, or during each packet exchange between the client and server.</span></span>

<span data-ttu-id="1ea11-106">Anche quando viene verificato il mittente del traffico, la protezione è ancora debole, dal momento che tale verifica non garantisce che il pacchetto non sia stato modificato o danneggiato in Route; verifica solo che il pacchetto provenga dal principale specificato.</span><span class="sxs-lookup"><span data-stu-id="1ea11-106">Even when the sender of the traffic is verified, security is still weak, since such verification does not ensure the packet was not modified or corrupted en route; it only verifies that the packet came from the given principal.</span></span> <span data-ttu-id="1ea11-107">Per una maggiore sicurezza, le applicazioni distribuite possono impostare la libreria di runtime RPC per verificare che nessuno dei dati scambiati tra il client e il server venga modificato.</span><span class="sxs-lookup"><span data-stu-id="1ea11-107">For greater security, distributed applications can set the RPC run-time library to verify that none of the data exchanged between the client and server is modified.</span></span> <span data-ttu-id="1ea11-108">La libreria RPC può inoltre crittografare il contenuto di ogni pacchetto prima di inviarlo.</span><span class="sxs-lookup"><span data-stu-id="1ea11-108">The RPC library can also encrypt the contents of every packet before sending it.</span></span> <span data-ttu-id="1ea11-109">In generale, le applicazioni che vogliono proteggere il traffico devono usare solo gli ultimi due livelli: integrità e privacy.</span><span class="sxs-lookup"><span data-stu-id="1ea11-109">In general, applications that want to secure their traffic should use only the last two levels—integrity and privacy.</span></span>

<span data-ttu-id="1ea11-110">Tenere presente che i livelli più elevati di autenticazione richiedono un sovraccarico computazionale più elevato.</span><span class="sxs-lookup"><span data-stu-id="1ea11-110">Be aware that higher levels of authentication require higher computational overhead.</span></span> <span data-ttu-id="1ea11-111">Gli sviluppatori devono decidere quale sia l'aspetto più importante per l'applicazione, ad esempio velocità o sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1ea11-111">You, as the developer, must decide which is more important for your application—speed or security.</span></span> <span data-ttu-id="1ea11-112">La maggior parte degli sviluppatori ritiene che, con alcuni test delle prestazioni, possano ottenere livelli di prestazioni accettabili mantenendo una sicurezza adeguata.</span><span class="sxs-lookup"><span data-stu-id="1ea11-112">Most developers find that with some performance testing, they can achieve acceptable performance levels while maintaining adequate security.</span></span>

<span data-ttu-id="1ea11-113">Il client e le parti del server dell'applicazione distribuita devono utilizzare lo stesso livello di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="1ea11-113">The client and the server portions of the distributed application must use the same authentication level.</span></span> <span data-ttu-id="1ea11-114">Per un elenco dei livelli di autenticazione RPC, vedere [costanti a livello di autenticazione](authentication-level-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1ea11-114">For a list of RPC authentication levels, see [Authentication-Level Constants](authentication-level-constants.md).</span></span>

 

 




