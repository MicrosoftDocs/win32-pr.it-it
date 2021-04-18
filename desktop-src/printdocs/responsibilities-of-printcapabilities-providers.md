---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilità dei provider PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bbf355f7b62f8f9c8b3f3b0c59714cdd6ade5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320952"
---
# <a name="responsibilities-of-printcapabilities-providers"></a><span data-ttu-id="7a0fe-104">Responsabilità dei provider PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="7a0fe-104">Responsibilities of PrintCapabilities Providers</span></span>

<span data-ttu-id="7a0fe-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-105">This topic is not current.</span></span> <span data-ttu-id="7a0fe-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7a0fe-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7a0fe-107">I provider PrintCapabilities devono supportare un set minimo di funzionalità, che sono implicite dall'interfaccia del provider PrintTicket/PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-107">PrintCapabilities providers must support a minimum set of capabilities, which are implied by the PrintTicket/PrintCapabilities Provider Interface.</span></span> <span data-ttu-id="7a0fe-108">Queste funzionalità sono elencate qui.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-108">These capabilities are listed here.</span></span>

-   <span data-ttu-id="7a0fe-109">Devono seguire la direzione della propagazione? Attributo XML, quando viene visualizzato nel contesto appropriato e contiene un valore valido per tale contesto.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-109">They must follow the direction of the propagate??XML attribute, when it appears in the appropriate context and contains a valid value for that context.</span></span>

-   <span data-ttu-id="7a0fe-110">Devono generare un documento PrintCapabilities conforme allo schema PrintCapabilities e soddisfa i requisiti specificati nello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-110">They must generate a PrintCapabilities document that conforms to the PrintCapabilities Schema and satisfies the requirements specified in the Print Schema.</span></span>

-   <span data-ttu-id="7a0fe-111">Devono essere in grado di riconoscere un oggetto PrintTicket valido.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-111">They must be able to recognize a valid PrintTicket.</span></span>

-   <span data-ttu-id="7a0fe-112">Devono essere in grado di interpretare un oggetto PrintTicket e comprendere la configurazione specifica che rappresenta.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-112">They must be able to interpret a PrintTicket and understand the specific configuration it represents.</span></span>

-   <span data-ttu-id="7a0fe-113">Devono essere in grado di determinare se la configurazione contiene conflitti di vincolo.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-113">They must be able to determine whether that configuration contains constraint conflicts.</span></span>

-   <span data-ttu-id="7a0fe-114">Devono essere in grado di modificare un oggetto PrintTicket non valido o in conflitto eseguendo la modifica meno significativa necessaria per renderlo sia valido che senza conflitti.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-114">They must be able to modify an invalid or conflicting PrintTicket by making the least significant change necessary to make it both valid and without conflicts.</span></span>

-   <span data-ttu-id="7a0fe-115">Devono essere in grado di generare un documento PrintCapabilities per una particolare configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-115">They must be able to generate a PrintCapabilities document for a particular device configuration.</span></span>

-   <span data-ttu-id="7a0fe-116">Devono essere in grado di generare una configurazione predefinita o un oggetto PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-116">They must be able to generate a default configuration or PrintTicket.</span></span>

-   <span data-ttu-id="7a0fe-117">Devono essere in grado di generare un documento PrintCapabilities che corrisponde alla configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-117">They must be able to generate a PrintCapabilities document that corresponds to the default configuration.</span></span>

-   <span data-ttu-id="7a0fe-118">Devono implementare un processo di assegnazione dei punteggi delle opzioni definito dal driver di dispositivo in grado di determinare la chiusura della corrispondenza tra due istanze di opzioni che appartengono alla stessa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-118">They must implement an Option-scoring process defined by the device driver capable of determining the closeness of match between two Option instances that belong to the same Feature.</span></span> <span data-ttu-id="7a0fe-119">Questo algoritmo viene utilizzato nel processo di convalida PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-119">This algorithm is used in the PrintTicket validation process.</span></span>

<span data-ttu-id="7a0fe-120">Oltre ai requisiti precedenti, il documento PrintCapabilities deve contenere valori validi e corretti per ogni attributo XML (ad esempio, vincolato) di ogni opzione.</span><span class="sxs-lookup"><span data-stu-id="7a0fe-120">In addition to the foregoing requirements, the PrintCapabilities document must contain valid and correct values for each XML attribute (for example, constrained) of each Option.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a0fe-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a0fe-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a0fe-122">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="7a0fe-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



