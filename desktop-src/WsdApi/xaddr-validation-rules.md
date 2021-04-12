---
description: Gli indirizzi di trasporto (XAddrs) inclusi nei messaggi ProbeMatches e ResolveMatches sono soggetti alla convalida di base prima che WSDAPI invii un messaggio HTTP, ad esempio una richiesta di metadati.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Regole di convalida XAddr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226797"
---
# <a name="xaddr-validation-rules"></a><span data-ttu-id="d2138-103">Regole di convalida XAddr</span><span class="sxs-lookup"><span data-stu-id="d2138-103">XAddr Validation Rules</span></span>

<span data-ttu-id="d2138-104">Gli indirizzi di trasporto (XAddrs) inclusi nei messaggi [ProbeMatches](probematches-message.md) e [ResolveMatches](resolvematches-message.md) sono soggetti alla convalida di base prima che WSDAPI invii un messaggio http, ad esempio una richiesta di metadati.</span><span class="sxs-lookup"><span data-stu-id="d2138-104">Transport addresses (XAddrs) included in [ProbeMatches](probematches-message.md) and [ResolveMatches](resolvematches-message.md) messages are subject to basic validation before WSDAPI sends an HTTP message, such as a metadata request.</span></span>

<span data-ttu-id="d2138-105">Per assicurarsi che XAddrs si trovino nella stessa subnet del client.</span><span class="sxs-lookup"><span data-stu-id="d2138-105">This is in order to ensure that the XAddrs are on the same subnet as the client.</span></span>

<span data-ttu-id="d2138-106">Nel codice XML seguente viene illustrato un elemento XAddrs di esempio.</span><span class="sxs-lookup"><span data-stu-id="d2138-106">The following XML shows a sample XAddrs element.</span></span> <span data-ttu-id="d2138-107">Il prefisso WSD si riferisce allo spazio dei nomi `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="d2138-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

<span data-ttu-id="d2138-108">Tutte le condizioni seguenti devono essere soddisfatte prima che il messaggio HTTP venga spostato in transito.</span><span class="sxs-lookup"><span data-stu-id="d2138-108">All of the following conditions must be met before the HTTP message will go out over the wire.</span></span>

-   <span data-ttu-id="d2138-109">XAddrs deve essere un indirizzo HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d2138-109">XAddrs must be HTTP or HTTPS addresses.</span></span> <span data-ttu-id="d2138-110">XAddrs di altri schemi vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="d2138-110">XAddrs of other schemes are ignored.</span></span>
-   <span data-ttu-id="d2138-111">Se sono presenti XAddrs HTTPS, tutti i XAddrs devono essere HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d2138-111">If any HTTPS XAddrs are present, all XAddrs must be HTTPS.</span></span> <span data-ttu-id="d2138-112">Le sezioni XAddr che includono indirizzi HTTP e HTTPS vengono completamente ignorate.</span><span class="sxs-lookup"><span data-stu-id="d2138-112">XAddr sections which include both HTTP and HTTPS addresses are completely ignored.</span></span> <span data-ttu-id="d2138-113">Inoltre, l'indirizzo endpoint del dispositivo deve corrispondere esattamente a HTTPS XAddrs.</span><span class="sxs-lookup"><span data-stu-id="d2138-113">Additionally, the device's endpoint address must match the HTTPS XAddrs exactly.</span></span>
-   <span data-ttu-id="d2138-114">XAddrs deve essere costituito da indirizzi IP o nomi host risolvibili tramite DNS.</span><span class="sxs-lookup"><span data-stu-id="d2138-114">XAddrs must be IP addresses or hostnames resolvable through DNS.</span></span> <span data-ttu-id="d2138-115">In genere, vengono usati gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="d2138-115">Usually, IP addresses are used.</span></span>
-   <span data-ttu-id="d2138-116">Almeno un indirizzo IP incluso in XAddrs (o indirizzo IP risolto da un nome host incluso in XAddrs) deve trovarsi nella stessa subnet dell'adapter su cui è stato ricevuto il messaggio [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="d2138-116">At least one IP address included in the XAddrs (or IP address resolved from a hostname included in the XAddrs) must be on the same subnet as the adapter over which the [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message was received.</span></span>
-   <span data-ttu-id="d2138-117">L'indirizzo e la porta specificati nel primo XAddr devono essere accessibili.</span><span class="sxs-lookup"><span data-stu-id="d2138-117">The address and port specified in the first XAddr must be accessible.</span></span> <span data-ttu-id="d2138-118">WSDAPI tenta di connettersi a questo indirizzo quando si stabilisce una connessione HTTP.</span><span class="sxs-lookup"><span data-stu-id="d2138-118">WSDAPI attempts to connect to this address when establishing an HTTP connection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2138-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2138-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2138-120">ProbeMatches</span><span class="sxs-lookup"><span data-stu-id="d2138-120">ProbeMatches</span></span>](probematches-message.md)
</dt> <dt>

[<span data-ttu-id="d2138-121">ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="d2138-121">ResolveMatches</span></span>](resolvematches-message.md)
</dt> <dt>

[<span data-ttu-id="d2138-122">Modelli di messaggi di individuazione e scambio di metadati</span><span class="sxs-lookup"><span data-stu-id="d2138-122">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



