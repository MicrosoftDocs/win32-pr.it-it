---
description: TAPI 3 supporta l'integrazione di interfacce specifiche del provider di servizi negli oggetti standard, consentendo alle applicazioni di sfruttare le funzionalità specifiche del provider.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Interfacce di Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058060"
---
# <a name="provider-specific-interfaces"></a><span data-ttu-id="19660-103">Interfacce di Provider-Specific</span><span class="sxs-lookup"><span data-stu-id="19660-103">Provider-Specific Interfaces</span></span>

<span data-ttu-id="19660-104">TAPI 3 supporta l'integrazione di interfacce specifiche del provider di servizi negli oggetti standard, consentendo alle applicazioni di sfruttare le funzionalità specifiche del provider.</span><span class="sxs-lookup"><span data-stu-id="19660-104">TAPI 3 supports integration of service provider-specific interfaces into the standard objects, allowing applications to take advantage of provider-specific functionality.</span></span> <span data-ttu-id="19660-105">Inoltre, TAPI 3 consente ai provider di servizi di fornire eventi specifici del fornitore alle applicazioni come oggetti COM sulla stessa interfaccia in cui l'applicazione riceve gli eventi standard.</span><span class="sxs-lookup"><span data-stu-id="19660-105">Additionally, TAPI 3 allows service providers to deliver vendor-specific events to applications as COM objects over the same interface on which the application receives standard events.</span></span>

<span data-ttu-id="19660-106">TAPI realizza questa integrazione aggregando oggetti specifici del provider con gli oggetti standard, ovvero TAPI, Address, Terminal, Call e CallHub, e inviando o delegando metodi sconosciuti a questi oggetti specifici del provider.</span><span class="sxs-lookup"><span data-stu-id="19660-106">TAPI achieves this integration by aggregating provider-specific objects with the standard objects – TAPI, Address, Terminal, Call, and CallHub – and dispatching or delegating unknown methods to these provider-specific objects.</span></span>

<span data-ttu-id="19660-107">Un provider di servizi, ad esempio, può consentire alle applicazioni di ottenere informazioni su una chiamata oltre a quelle esposte dall'interfaccia [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="19660-107">For example, a service provider may allow applications to obtain information about a call beyond what is exposed by the [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) interface.</span></span> <span data-ttu-id="19660-108">Il fornitore deve definire un'interfaccia che consente alle applicazioni di eseguire queste query aggiuntive e di implementare tale interfaccia in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="19660-108">The vendor must define an interface that allows applications to make these extra queries and implement that interface on an object.</span></span> <span data-ttu-id="19660-109">Questo oggetto implementa anche un'interfaccia di query sul fornitore, in modo che un'applicazione possa individuare quali tipi di funzioni specifiche del provider potrebbero essere disponibili.</span><span class="sxs-lookup"><span data-stu-id="19660-109">This object also implements a vendor information-querying interface so that an application can discover what sorts of provider-specific functions might be available.</span></span>

<span data-ttu-id="19660-110">Quando l'applicazione ottiene un riferimento a un oggetto chiamata, l'applicazione può usare la nuova interfaccia specifica del provider e i relativi metodi come se fossero implementati dall'oggetto chiamata stesso.</span><span class="sxs-lookup"><span data-stu-id="19660-110">When the application obtains a reference to a call object, the application can use the new provider-specific interface and its methods as if they were implemented by the call object itself.</span></span>

<span data-ttu-id="19660-111">Per un elenco di tutte le interfacce MSP standard, vedere informazioni di [riferimento sull'interfaccia del provider di servizi multimediali (MSPI)](media-service-provider-interface-mspi-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="19660-111">See [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md) for a list of all standard MSP interfaces.</span></span>

<span data-ttu-id="19660-112">Vedere [IPConf msp Interfaces](ipconf-msp-interfaces.md) per un elenco di tutte le interfacce specifiche di IPConf msp.</span><span class="sxs-lookup"><span data-stu-id="19660-112">See [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a list of all interfaces specific to the IPConf MSP.</span></span>

 

 



