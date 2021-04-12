---
title: Configurazione di RPC per SPX/IPX
description: Quando si usano i \_ trasporti IPX ncacn SPX e ncadg \_ , il nome del server è esattamente uguale al nome del server in Windows.
ms.assetid: b2543046-8cdc-4cba-94e4-40188701fad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90fa82c216413f1ea745b90ae03749ede4331310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471507"
---
# <a name="configuring-rpc-for-spxipx"></a><span data-ttu-id="10e7b-103">Configurazione di RPC per SPX/IPX</span><span class="sxs-lookup"><span data-stu-id="10e7b-103">Configuring RPC for SPX/IPX</span></span>

<span data-ttu-id="10e7b-104">Quando si usano i trasporti **\_ IPX** **ncacn \_ SPX** e ncadg, il nome del server è esattamente uguale al nome del server in Windows.</span><span class="sxs-lookup"><span data-stu-id="10e7b-104">When using the **ncacn\_spx** and **ncadg\_ipx** transports, the server name is exactly the same as the server name on Windows.</span></span> <span data-ttu-id="10e7b-105">Tuttavia, poiché i nomi vengono distribuiti usando i protocolli Novell, devono essere conformi alle convenzioni di denominazione Novell.</span><span class="sxs-lookup"><span data-stu-id="10e7b-105">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="10e7b-106">Se il nome di un server non è un nome Novell valido, i server non saranno in grado di creare endpoint con i trasporti **\_ IPX** **ncacn \_ SPX** o ncadg.</span><span class="sxs-lookup"><span data-stu-id="10e7b-106">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** or **ncadg\_ipx** transports.</span></span>

<span data-ttu-id="10e7b-107">Un nome di server Novell valido contiene solo i caratteri compresi tra 0x20 e 0x7F.</span><span class="sxs-lookup"><span data-stu-id="10e7b-107">A valid Novell server name contains only the characters between 0x20 and 0x7f.</span></span> <span data-ttu-id="10e7b-108">I caratteri minuscoli vengono modificati in maiuscolo.</span><span class="sxs-lookup"><span data-stu-id="10e7b-108">Lowercase characters are changed to uppercase.</span></span> <span data-ttu-id="10e7b-109">Non è possibile usare i caratteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="10e7b-109">The following characters cannot be used:</span></span>

<span data-ttu-id="10e7b-110">" \* ,./:; <=>?\[\]\\\|\]</span><span class="sxs-lookup"><span data-stu-id="10e7b-110">"\*,./:;<=>?\[\]\\\|\]</span></span>

<span data-ttu-id="10e7b-111">Per mantenere la compatibilità con la prima versione di Windows NT, **ncacn \_ SPX** e **ncadg \_ IPX** consentono anche di usare un formato speciale del nome del server noto come nome tilde.</span><span class="sxs-lookup"><span data-stu-id="10e7b-111">To maintain compatibility with the first version of Windows NT, **ncacn\_spx** and **ncadg\_ipx** also enable you to use a special format of the server name known as the tilde name.</span></span> <span data-ttu-id="10e7b-112">Il nome della tilde è costituito da una tilde (~), seguita dal numero di rete di otto cifre del server e quindi da un indirizzo Ethernet a 12 cifre.</span><span class="sxs-lookup"><span data-stu-id="10e7b-112">The tilde name consists of a tilde (~), followed by the server's eight-digit network number, and then followed by its 12-digit Ethernet address.</span></span> <span data-ttu-id="10e7b-113">I nomi tilde hanno un vantaggio nel fatto che non richiedono funzionalità di servizio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="10e7b-113">Tilde names have an advantage in that they do not require any name service capabilities.</span></span> <span data-ttu-id="10e7b-114">Pertanto, se si è connessi a un server, il nome della tilde funzionerà.</span><span class="sxs-lookup"><span data-stu-id="10e7b-114">Thus, if you are connected to a server, the tilde name will work.</span></span>

<span data-ttu-id="10e7b-115">Le tabelle seguenti contengono due configurazioni di esempio che illustrano i punti descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="10e7b-115">The following tables contain two sample configurations that illustrate the points previously described.</span></span>



| <span data-ttu-id="10e7b-116">Componente</span><span class="sxs-lookup"><span data-stu-id="10e7b-116">Component</span></span>                            | <span data-ttu-id="10e7b-117">Configurato come</span><span class="sxs-lookup"><span data-stu-id="10e7b-117">Configured as</span></span>      |
|--------------------------------------|--------------------|
| <span data-ttu-id="10e7b-118">Windows Server</span><span class="sxs-lookup"><span data-stu-id="10e7b-118">Windows server</span></span>                       | <span data-ttu-id="10e7b-119">NWCS</span><span class="sxs-lookup"><span data-stu-id="10e7b-119">NWCS</span></span>               |
| <span data-ttu-id="10e7b-120">Client Windows</span><span class="sxs-lookup"><span data-stu-id="10e7b-120">Windows client</span></span>                       | <span data-ttu-id="10e7b-121">NWCS</span><span class="sxs-lookup"><span data-stu-id="10e7b-121">NWCS</span></span>               |
| <span data-ttu-id="10e7b-122">client Windows a 16 bit, client MS-DOS</span><span class="sxs-lookup"><span data-stu-id="10e7b-122">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="10e7b-123">Redirector NetWare</span><span class="sxs-lookup"><span data-stu-id="10e7b-123">NetWare Redirector</span></span> |



 

<span data-ttu-id="10e7b-124">Per la configurazione nella tabella precedente è necessario che nella rete siano presenti file server o router NetWare.</span><span class="sxs-lookup"><span data-stu-id="10e7b-124">The configuration in the previous table requires that you have NetWare file servers or routers on your network.</span></span> <span data-ttu-id="10e7b-125">In quanto i nomi dei server vengono archiviati nell'associazione NetWare.</span><span class="sxs-lookup"><span data-stu-id="10e7b-125">It will produce the best performance because the server names are stored in the NetWare Bindery.</span></span>



| <span data-ttu-id="10e7b-126">Componente</span><span class="sxs-lookup"><span data-stu-id="10e7b-126">Component</span></span>                            | <span data-ttu-id="10e7b-127">Configurato come</span><span class="sxs-lookup"><span data-stu-id="10e7b-127">Configured as</span></span> |
|--------------------------------------|---------------|
| <span data-ttu-id="10e7b-128">Windows Server</span><span class="sxs-lookup"><span data-stu-id="10e7b-128">Windows server</span></span>                       | <span data-ttu-id="10e7b-129">Agente SAP</span><span class="sxs-lookup"><span data-stu-id="10e7b-129">SAP Agent</span></span>     |
| <span data-ttu-id="10e7b-130">Client Windows</span><span class="sxs-lookup"><span data-stu-id="10e7b-130">Windows client</span></span>                       | <span data-ttu-id="10e7b-131">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="10e7b-131">IPX/SPX</span></span>       |
| <span data-ttu-id="10e7b-132">client Windows a 16 bit, client MS-DOS</span><span class="sxs-lookup"><span data-stu-id="10e7b-132">16-bit Windows client, MS-DOS client</span></span> | <span data-ttu-id="10e7b-133">IPX/SPX</span><span class="sxs-lookup"><span data-stu-id="10e7b-133">IPX/SPX</span></span>       |



 

<span data-ttu-id="10e7b-134">La seconda configurazione funziona in un ambiente che non contiene file server o router NetWare, ad esempio una rete di due computer: un server Windows e un client MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="10e7b-134">The second configuration works in an environment that does not contain NetWare file servers or routers (for example, a network of two computers: a Windows server and an MS-DOS client).</span></span> <span data-ttu-id="10e7b-135">La risoluzione dei nomi, eseguita durante la prima chiamata su un handle di binding, sarà leggermente più lenta rispetto alla prima configurazione.</span><span class="sxs-lookup"><span data-stu-id="10e7b-135">Name resolution, which is accomplished during the first call over a binding handle, will be slightly slower than in the first configuration.</span></span> <span data-ttu-id="10e7b-136">Inoltre, la seconda configurazione comporta un maggiore traffico generato sulla rete.</span><span class="sxs-lookup"><span data-stu-id="10e7b-136">In addition, the second configuration results in more traffic generated over the network.</span></span>

<span data-ttu-id="10e7b-137">Per implementare la risoluzione dei nomi, quando un server RPC utilizza un endpoint SPX o IPX, il nome del server e l'endpoint vengono registrati come Server Service Advertising Protocol (SAP) di tipo 640 (esadecimale).</span><span class="sxs-lookup"><span data-stu-id="10e7b-137">To implement name resolution, when an RPC server uses an SPX or IPX endpoint, the server name and endpoint are registered as a Service Advertising Protocol (SAP) server of type 640 (hexadecimal).</span></span> <span data-ttu-id="10e7b-138">Per risolvere il nome di un server, il client RPC invia una richiesta SAP per tutti i servizi dello stesso tipo e quindi analizza l'elenco di risposte per il nome del server.</span><span class="sxs-lookup"><span data-stu-id="10e7b-138">To resolve a server name, the RPC client sends a SAP request for all services of the same type, and then scans the list of responses for the name of the server.</span></span> <span data-ttu-id="10e7b-139">Questo processo si verifica durante la prima chiamata RPC su ogni handle di binding.</span><span class="sxs-lookup"><span data-stu-id="10e7b-139">This process occurs during the first RPC call over each binding handle.</span></span> <span data-ttu-id="10e7b-140">Per ulteriori informazioni sul protocollo SAP per Novell, vedere la documentazione di NetWare.</span><span class="sxs-lookup"><span data-stu-id="10e7b-140">For additional information on the SAP protocol for Novell, see your NetWare documentation.</span></span>

> [!Note]  
> <span data-ttu-id="10e7b-141">Le applicazioni client Windows a 16 bit che usano i trasporti **\_ IPX** **ncacn \_ SPX** o ncadg richiedono che il file Nwipxspx.dll sia installato per l'esecuzione nel sottosistema WOW.</span><span class="sxs-lookup"><span data-stu-id="10e7b-141">The 16-bit Windows client applications that use the **ncacn\_spx** or **ncadg\_ipx** transports require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="10e7b-142">Per ottenere questo file, contattare Novell.</span><span class="sxs-lookup"><span data-stu-id="10e7b-142">Contact Novell to obtain this file.</span></span>

 

 

 




