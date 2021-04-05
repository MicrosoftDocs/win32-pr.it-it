---
title: Elenco di ascolto IP
description: Le API del server HTTP non vengono associate ad alcuna coppia di indirizzi IP e porte TCP fino a quando un utente non registra un UrlPrefix.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955794"
---
# <a name="ip-listen-list"></a><span data-ttu-id="e04fc-103">Elenco di ascolto IP</span><span class="sxs-lookup"><span data-stu-id="e04fc-103">IP Listen List</span></span>

<span data-ttu-id="e04fc-104">Le API del server HTTP non vengono associate ad alcuna coppia di indirizzi IP e porte TCP fino a quando un utente non registra un UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="e04fc-104">The HTTP Server APIs do not bind to any IP address and TCP port pairs until a user registers a UrlPrefix.</span></span> <span data-ttu-id="e04fc-105">Per impostazione predefinita, dopo aver immesso una registrazione nella coda di richieste, l'API del server HTTP viene associata alla porta specificata in UrlPrefix (ad esempio, la porta 80) per tutti gli indirizzi IP (tutti i \_ o INADDR6 \_ ) disponibili nel computer.</span><span class="sxs-lookup"><span data-stu-id="e04fc-105">By default, once a registration is entered in the request queue, the HTTP Server API binds to the port specified in the UrlPrefix (for example port 80) for all IP addresses (INADDR\_ANY or INADDR6\_ANY) available on the machine.</span></span> <span data-ttu-id="e04fc-106">I problemi si verificano quando le applicazioni di terze parti (che non usano le API del server HTTP) si associano alle coppie di indirizzi IP e porte 80 nel computer.</span><span class="sxs-lookup"><span data-stu-id="e04fc-106">Problems arise when third party applications (not using the HTTP Server APIs) bind to IP address and port 80 pairs on the machine.</span></span> <span data-ttu-id="e04fc-107">L'API server HTTP consente di configurare l'elenco di indirizzi IP che associa e risolve questo problema di coesistenza.</span><span class="sxs-lookup"><span data-stu-id="e04fc-107">The HTTP Server API provides a way to configure the list of IP addresses that it binds and solves this coexistence issue.</span></span> <span data-ttu-id="e04fc-108">L'amministratore di sistema chiama la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con il parametro *ConfigId* impostato sul valore HttpServiceConfigIPListenList per specificare l'elenco di ascolto IP.</span><span class="sxs-lookup"><span data-stu-id="e04fc-108">The system administrator calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the *ConfigId* parameter set to the HttpServiceConfigIPListenList value to specify the IP listen list.</span></span> <span data-ttu-id="e04fc-109">Gli indirizzi IPv4 e IPv6 possono essere aggiunti all'elenco.</span><span class="sxs-lookup"><span data-stu-id="e04fc-109">Both IPv4 and IPv6 addresses can be added to the list.</span></span> <span data-ttu-id="e04fc-110">Gli indirizzi IP immessi si applicano a tutte le applicazioni nel computer che usano l'API del server HTTP e vengono mantenuti tra i riavvii del computer.</span><span class="sxs-lookup"><span data-stu-id="e04fc-110">The IP addresses entered apply to all applications on the machine using the HTTP Server API and persist across reboots of the machine.</span></span> <span data-ttu-id="e04fc-111">Tuttavia, qualsiasi modifica alla configurazione dell'elenco di ascolto IP non viene eseguita in modo dinamico; nella maggior parte dei casi, potrebbe essere necessario un riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="e04fc-111">However, any changes to the IP listen list configuration do not take place dynamically; in most cases, a system reboot may be necessary.</span></span>

 

 




