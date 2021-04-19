---
description: L'oggetto call rappresenta una connessione di indirizzi tra l'indirizzo locale e uno o più indirizzi.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Chiama oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b8ea40b7b2cadece9c89a45f9296995ad92fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319883"
---
# <a name="call-object"></a><span data-ttu-id="1d19e-103">Chiama oggetto</span><span class="sxs-lookup"><span data-stu-id="1d19e-103">Call Object</span></span>

<span data-ttu-id="1d19e-104">L'oggetto call rappresenta la connessione di un indirizzo tra l'indirizzo locale e uno o più indirizzi.</span><span class="sxs-lookup"><span data-stu-id="1d19e-104">The Call object represents an address's connection between the local address and one or more other addresses.</span></span> <span data-ttu-id="1d19e-105">Tutto il controllo delle chiamate viene eseguito tramite l'oggetto call.</span><span class="sxs-lookup"><span data-stu-id="1d19e-105">All call control is done through the Call object.</span></span> <span data-ttu-id="1d19e-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) e [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) sono le interfacce usate più di frequente nell'oggetto call.</span><span class="sxs-lookup"><span data-stu-id="1d19e-106">[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) are the most frequently used interfaces on the call object.</span></span> <span data-ttu-id="1d19e-107">Queste interfacce implementano una serie di operazioni e query, ad esempio l'acquisizione di puntatori di interfaccia per flussi multimediali o l'ottenimento dell'ID chiamante.</span><span class="sxs-lookup"><span data-stu-id="1d19e-107">These interfaces implement a variety of operations and queries, such as acquiring interface pointers for media streams or getting the caller ID.</span></span> <span data-ttu-id="1d19e-108">Vedere le sezioni principali della panoramica sulle [operazioni di sessione](session-operations-ovr.md) e informazioni di [sessione](session-information-ovr.md) per le verifiche di quelle supportate da TAPI.</span><span class="sxs-lookup"><span data-stu-id="1d19e-108">See the main overview sections on [Session Operations](session-operations-ovr.md) and [Session Information](session-information-ovr.md) for reviews of those supported by TAPI.</span></span>

<span data-ttu-id="1d19e-109">Un provider di servizi multimediali può implementare [interfacce specifiche del provider](provider-specific-interfaces.md), che vengono aggregate in un oggetto chiamata da TAPI.</span><span class="sxs-lookup"><span data-stu-id="1d19e-109">A media service provider can implement [provider-specific interfaces](provider-specific-interfaces.md), which are aggregated on a call object by TAPI.</span></span> <span data-ttu-id="1d19e-110">Per informazioni dettagliate sull'implementazione di un provider, vedere la documentazione del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="1d19e-110">For detailed information on what a provider has implemented, see the service provider's documentation.</span></span>

<span data-ttu-id="1d19e-111">Gli esempi [effettuare una chiamata](make-a-call.md) e [ricevere un](receive-a-call.md) codice di chiamata mostrano alcune illustrazioni sull'uso di un oggetto call.</span><span class="sxs-lookup"><span data-stu-id="1d19e-111">The [Make a Call](make-a-call.md) and [Receive a Call](receive-a-call.md) code examples show some illustrations of using a Call object.</span></span>

<span data-ttu-id="1d19e-112">Vedere [chiamare le interfacce dell'oggetto](call-object-interfaces.md) per un elenco di tutte le interfacce associate all'oggetto chiamata.</span><span class="sxs-lookup"><span data-stu-id="1d19e-112">See [Call Object Interfaces](call-object-interfaces.md) for a list of all interfaces associated with the Call object.</span></span>

 

 



