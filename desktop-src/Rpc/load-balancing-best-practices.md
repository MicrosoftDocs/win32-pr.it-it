---
title: Procedure consigliate per il bilanciamento del carico
description: Procedure consigliate per il bilanciamento del carico
ms.assetid: 260cf8dd-13b8-4b46-93a6-5333e794c0d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c68b85f60b75cb5a0fc75bd5ad8bd438608a9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963304"
---
# <a name="load-balancing-best-practices"></a><span data-ttu-id="76774-103">Procedure consigliate per il bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="76774-103">Load Balancing Best Practices</span></span>

<span data-ttu-id="76774-104">Quando si installa e si configura il bilanciamento del carico RPC, è necessario seguire alcune procedure consigliate.</span><span class="sxs-lookup"><span data-stu-id="76774-104">Several best practices should be followed when setting up and configuring RPC Load balancing.</span></span>

<span data-ttu-id="76774-105">Per prima cosa, è necessario impostare la sicurezza sulle chiamate in ingresso e in uscita LBS.</span><span class="sxs-lookup"><span data-stu-id="76774-105">First, security should be set on incoming and outgoing LBS calls.</span></span> <span data-ttu-id="76774-106">Ciò significa che entrambe le chiavi facoltative del registro di sistema [NoSecurity](configuring-load-balancing.md) non devono essere presenti o devono essere impostate su zero.</span><span class="sxs-lookup"><span data-stu-id="76774-106">This means both of the optional [NoSecurity](configuring-load-balancing.md) registry keys should either not be present or should be set to zero.</span></span>

<span data-ttu-id="76774-107">In secondo luogo, è necessario prestare attenzione alla soluzione front-end di bilanciamento del carico usata insieme alla soluzione di bilanciamento del carico RPC.</span><span class="sxs-lookup"><span data-stu-id="76774-107">Second, attention must be paid to the front end load balancing solution used in conjunction with the RPC Load Balancing solution.</span></span> <span data-ttu-id="76774-108">Se, ad esempio, il servizio di bilanciamento del carico front-end usa il bilanciamento del carico round robin semplice, nel server farm dovrebbe esistere un numero dispari di server.</span><span class="sxs-lookup"><span data-stu-id="76774-108">For example, if the front end load balancer uses simple round robin load balancing, an odd number of servers should exist in the server farm.</span></span> <span data-ttu-id="76774-109">Questo consente di ridurre la possibilità che tutte le connessioni vengano trasmesse e quindi gestite dallo stesso server o server.</span><span class="sxs-lookup"><span data-stu-id="76774-109">This is to mitigate the possibility of all connections being forwarded and thus serviced by the same server or servers.</span></span>

<span data-ttu-id="76774-110">Per la sicurezza, è preferibile disporre di un controllo firewall per l'accesso ai server proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="76774-110">For security, it is commonly desirable to have a firewall control access to RPC Proxy servers.</span></span> <span data-ttu-id="76774-111">Se viene utilizzata una soluzione firewall basata su porta, gli endpoint RPC devono essere statici per limitare il numero di porte aperte nel firewall.</span><span class="sxs-lookup"><span data-stu-id="76774-111">If a port based firewall solution is employed, RPC endpoints must be static in order to limit the number of ports that are opened in the firewall.</span></span> <span data-ttu-id="76774-112">In Windows Server 2008 e versioni successive di Windows, RPC fornisce un meccanismo per assegnare una porta statica agli endpoint dinamici.</span><span class="sxs-lookup"><span data-stu-id="76774-112">On Windows Server 2008 and later versions of Windows, RPC provides a mechanism to assign a static port to dynamic endpoints.</span></span> <span data-ttu-id="76774-113">Questa operazione viene eseguita tramite i comandi netsh firewall di RPC.</span><span class="sxs-lookup"><span data-stu-id="76774-113">This is achieved through the RPC netsh firewall commands.</span></span> <span data-ttu-id="76774-114">Un set di comandi di esempio per impostare l'interfaccia LBS sulla porta statica 3010 è:</span><span class="sxs-lookup"><span data-stu-id="76774-114">An example set of commands to set the LBS interface to the static port of 3010 is:</span></span>

``` syntax
netsh rpc filter add rule layer=ep_add actiontype=permit

netsh rpc filter add condition field=process_with_if_uuid matchtype=equal data=
3357951c-a1d1-47db-a278-ab945d063d03

netsh rpc filter add condition field=protocol matchtype=equal data=ncacn_ip_tcp

netsh rpc filter add condition field=ep_value matchtype=equal data=w3010

netsh rpc filter add filter
```

<span data-ttu-id="76774-115">Il comando netsh RPC può essere utilizzato per impostare un endpoint statico per qualsiasi interfaccia dinamica o statica.</span><span class="sxs-lookup"><span data-stu-id="76774-115">The RPC netsh command can be used to set a static endpoint for any dynamic or static interface.</span></span> <span data-ttu-id="76774-116">Questa operazione è utile quando si limita l'accesso a un computer che esegue una soluzione firewall basata su porte.</span><span class="sxs-lookup"><span data-stu-id="76774-116">This is useful when restricting access to a machine running a port based firewall solution.</span></span> <span data-ttu-id="76774-117">Se si utilizza la soluzione Windows Firewall, l'interfaccia RPC può essere bloccata o abilitata senza che sia necessario assegnarla a una porta specifica.</span><span class="sxs-lookup"><span data-stu-id="76774-117">If the Windows firewall solution is used, the RPC interface can be blocked or enabled without having to assign it to a specific port.</span></span> <span data-ttu-id="76774-118">Per ulteriori informazioni, vedere la Guida di [riferimento al comando RPC netsh firewall](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="76774-118">For more information, see the [RPC netsh firewall command reference](/previous-versions/windows/it-pro/windows-server-2003/cc784909(v=ws.10)).</span></span>

 

 