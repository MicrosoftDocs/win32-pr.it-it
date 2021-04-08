---
description: L'ordine di installazione iniziale dei provider di servizi di trasporto determina l'ordine in cui vengono enumerate tramite WSCEnumProtocols e WSCEnumProtocols32 nell'interfaccia del provider di servizi o tramite WSAEnumProtocols nell'interfaccia dell'applicazione. In particolare, questo ordine regola anche l'ordine in cui i protocolli e i provider di servizi vengono considerati quando un client richiede la creazione di un socket in base alla famiglia di indirizzi, al tipo e all'identificatore del protocollo.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Ordinamento del provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c23d9357d30c94b084bf6288013c38a2d46a4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880454"
---
# <a name="service-provider-ordering"></a><span data-ttu-id="cfd90-104">Ordinamento del provider di servizi</span><span class="sxs-lookup"><span data-stu-id="cfd90-104">Service Provider Ordering</span></span>

<span data-ttu-id="cfd90-105">L'ordine di installazione iniziale dei provider di servizi di trasporto determina l'ordine in cui vengono enumerate tramite [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) e [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) nell'interfaccia del provider di servizi o tramite [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) nell'interfaccia dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cfd90-105">The order in which transport service providers are initially installed governs the order in which they are enumerated through [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) and [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) at the service provider interface, or through [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) at the application interface.</span></span> <span data-ttu-id="cfd90-106">In particolare, questo ordine regola anche l'ordine in cui i protocolli e i provider di servizi vengono considerati quando un client richiede la creazione di un socket in base alla famiglia di indirizzi, al tipo e all'identificatore del protocollo.</span><span class="sxs-lookup"><span data-stu-id="cfd90-106">More importantly, this order also governs the order in which protocols and service providers are considered when a client requests creation of a socket based on its address family, type, and protocol identifier.</span></span>

<span data-ttu-id="cfd90-107">Windows Sockets 2 include un'applet denominata Sporder.exe che consente di riordinare i protocolli installati in modo interattivo dopo che i protocolli sono già stati installati.</span><span class="sxs-lookup"><span data-stu-id="cfd90-107">Windows Sockets 2 includes an applet called Sporder.exe that allows the catalog of installed protocols to be reordered interactively after protocols have already been installed.</span></span> <span data-ttu-id="cfd90-108">Winsock include anche una DLL ausiliaria, Sporder.dll, che esporta un'interfaccia procedurale per i protocolli di riordinamento.</span><span class="sxs-lookup"><span data-stu-id="cfd90-108">Winsock also includes an auxiliary DLL, Sporder.dll, that exports a procedural interface for reordering protocols.</span></span> <span data-ttu-id="cfd90-109">Questa interfaccia procedurale è costituita da una singola procedura denominata [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).</span><span class="sxs-lookup"><span data-stu-id="cfd90-109">This procedural interface consists of a single procedure called [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).</span></span>

<span data-ttu-id="cfd90-110">La definizione dell'interfaccia può essere importata in un programma C o C++ per mezzo del file di inclusione sporder. h.</span><span class="sxs-lookup"><span data-stu-id="cfd90-110">The interface definition may be imported into a C or C++ program by means of the include file Sporder.h.</span></span> <span data-ttu-id="cfd90-111">Il punto di ingresso può essere collegato tramite il file lib sporder. lib.</span><span class="sxs-lookup"><span data-stu-id="cfd90-111">The entry point may be linked by means of the lib file Sporder.lib.</span></span>

 

 



