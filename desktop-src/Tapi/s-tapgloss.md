---
description: I termini seguenti sono utili per comprendere la tecnologia TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b4256a4a-c19e-4431-b62f-9e9fef4b5827
title: S (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f33f4d2c16110ad6c79a02401c6a63ad0fb8f4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319864"
---
# <a name="s-telephony-api"></a><span data-ttu-id="e71fa-103">S (API di telefonia)</span><span class="sxs-lookup"><span data-stu-id="e71fa-103">S (Telephony API)</span></span>

<span data-ttu-id="e71fa-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [d](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [i](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="e71fa-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="e71fa-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="e71fa-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**service provider**</span></span>
</dt> <dd>

<span data-ttu-id="e71fa-106">Libreria a collegamento dinamico che supporta le comunicazioni su una rete telefonica tramite un set di funzioni del servizio esportate.</span><span class="sxs-lookup"><span data-stu-id="e71fa-106">A dynamic-link library that supports communications over a telephone network through a set of exported service functions.</span></span> <span data-ttu-id="e71fa-107">Il provider di servizi risponde alle richieste di telefonia, inviate dalla libreria a collegamento dinamico TAPI, eseguendo le attività di basso livello necessarie per comunicare attraverso la rete telefonica.</span><span class="sxs-lookup"><span data-stu-id="e71fa-107">The service provider responds to telephony requests, sent to it by the TAPI dynamic-link library, by carrying out the low-level tasks necessary to communicate over the telephone network.</span></span> <span data-ttu-id="e71fa-108">In questo modo, il provider di servizi, insieme a TAPI, protegge le applicazioni dal servizio e dai dettagli dipendenti dalla tecnologia della comunicazione di rete telefonica.</span><span class="sxs-lookup"><span data-stu-id="e71fa-108">In this way, the service provider, in conjunction with TAPI, shields applications from the service- and technology-dependent details of the telephone network communication.</span></span>

</dd> <dt>

<span data-ttu-id="e71fa-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**sottoindirizzo**</span><span class="sxs-lookup"><span data-stu-id="e71fa-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**subaddressing**</span></span>
</dt> <dd>

<span data-ttu-id="e71fa-110">Funzionalità fornita su linee ISDN che consente di ottenere più informazioni rispetto a un singolo numero di telefono da usare per la composizione.</span><span class="sxs-lookup"><span data-stu-id="e71fa-110">A capability provided on ISDN lines that allows more information than just a single telephone number to be used when dialing.</span></span>

</dd> <dt>

<span data-ttu-id="e71fa-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Telefonia supplementare**</span><span class="sxs-lookup"><span data-stu-id="e71fa-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Supplementary Telephony**</span></span>
</dt> <dd>

<span data-ttu-id="e71fa-112">Livello di servizio che fornisce funzionalità avanzate di commutatore, ad esempio in attesa, trasferimento e così via.</span><span class="sxs-lookup"><span data-stu-id="e71fa-112">Level of service that provides advanced switch features such as hold, transfer, and so on.</span></span> <span data-ttu-id="e71fa-113">Tutti i servizi supplementari sono facoltativi. ovvero, il provider di servizi non è necessario per supportarli.</span><span class="sxs-lookup"><span data-stu-id="e71fa-113">All supplementary services are optional; that is, the service provider is not required to support them.</span></span> <span data-ttu-id="e71fa-114">Vedere [*telefonia assistita*](a-tapgloss.md), [*telefonia di base*](b-tapgloss.md), [*telefonia estesa*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span><span class="sxs-lookup"><span data-stu-id="e71fa-114">See [*Assisted Telephony*](a-tapgloss.md), [*Basic Telephony*](b-tapgloss.md), [*Extended Telephony*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span></span>

</dd> <dt>

<span data-ttu-id="e71fa-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Switched 56**</span><span class="sxs-lookup"><span data-stu-id="e71fa-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Switched 56**</span></span>
</dt> <dd>

<span data-ttu-id="e71fa-116">Un servizio dati con commutazione che consente all'utente di comporre un altro utente e di trasmettere a un massimo di 56 Kbps per il prezzo di una telefonata.</span><span class="sxs-lookup"><span data-stu-id="e71fa-116">A switched data service that lets the user dial someone else and transmit at full duplex, digital synchronous 56 Kbps for the price of a phone call.</span></span>

</dd> <dt>

<span data-ttu-id="e71fa-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**sincrono**</span><span class="sxs-lookup"><span data-stu-id="e71fa-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**synchronous**</span></span>
</dt> <dd>

<span data-ttu-id="e71fa-118">Metodo di trasmissione dei dati in cui è presente un tempo costante tra i bit successivi, i caratteri o gli eventi.</span><span class="sxs-lookup"><span data-stu-id="e71fa-118">Data transmission method in which there is constant time between successive bits, characters, or events.</span></span> <span data-ttu-id="e71fa-119">La temporizzazione viene eseguita dalla condivisione di un singolo clock.</span><span class="sxs-lookup"><span data-stu-id="e71fa-119">The timing is achieved by the sharing of a single clock.</span></span> <span data-ttu-id="e71fa-120">Ogni estremità della trasmissione si sincronizza con l'uso di clock e informazioni inviate insieme ai dati trasmessi.</span><span class="sxs-lookup"><span data-stu-id="e71fa-120">Each end of the transmission synchronizes itself with the use of clocks and information sent along with the transmitted data.</span></span> <span data-ttu-id="e71fa-121">I caratteri sono spaziati dal tempo, non dai bit di avvio e di arresto.</span><span class="sxs-lookup"><span data-stu-id="e71fa-121">Characters are spaced by time, not by start and stop bits.</span></span> <span data-ttu-id="e71fa-122">Vedere [*asincrono*](a-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="e71fa-122">See [*asynchronous*](a-tapgloss.md).</span></span>

</dd> </dl>

 

 



