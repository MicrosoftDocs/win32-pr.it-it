---
description: I provider PrintCapabilities devono supportare un set minimo di funzionalità, implicite nell'interfaccia del provider PrintTicket/PrintCapabilities.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilità dei provider PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc04137eacdd2395205b96233db3c53964bc02
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404914"
---
# <a name="responsibilities-of-printcapabilities-providers"></a><span data-ttu-id="17a45-103">Responsabilità dei provider PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="17a45-103">Responsibilities of PrintCapabilities Providers</span></span>

<span data-ttu-id="17a45-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="17a45-104">This topic is not current.</span></span> <span data-ttu-id="17a45-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="17a45-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="17a45-106">I provider PrintCapabilities devono supportare un set minimo di funzionalità, implicite nell'interfaccia del provider PrintTicket/PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="17a45-106">PrintCapabilities providers must support a minimum set of capabilities, which are implied by the PrintTicket/PrintCapabilities Provider Interface.</span></span> <span data-ttu-id="17a45-107">Queste funzionalità sono elencate qui.</span><span class="sxs-lookup"><span data-stu-id="17a45-107">These capabilities are listed here.</span></span>

-   <span data-ttu-id="17a45-108">Devono seguire la direzione della propagazione?? Attributo XML, quando viene visualizzato nel contesto appropriato e contiene un valore valido per tale contesto.</span><span class="sxs-lookup"><span data-stu-id="17a45-108">They must follow the direction of the propagate??XML attribute, when it appears in the appropriate context and contains a valid value for that context.</span></span>

-   <span data-ttu-id="17a45-109">Devono generare un documento PrintCapabilities conforme allo schema PrintCapabilities e soddisfano i requisiti specificati nello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="17a45-109">They must generate a PrintCapabilities document that conforms to the PrintCapabilities Schema and satisfies the requirements specified in the Print Schema.</span></span>

-   <span data-ttu-id="17a45-110">Devono essere in grado di riconoscere un PrintTicket valido.</span><span class="sxs-lookup"><span data-stu-id="17a45-110">They must be able to recognize a valid PrintTicket.</span></span>

-   <span data-ttu-id="17a45-111">Devono essere in grado di interpretare un PrintTicket e comprendere la configurazione specifica che rappresenta.</span><span class="sxs-lookup"><span data-stu-id="17a45-111">They must be able to interpret a PrintTicket and understand the specific configuration it represents.</span></span>

-   <span data-ttu-id="17a45-112">Devono essere in grado di determinare se tale configurazione contiene conflitti di vincoli.</span><span class="sxs-lookup"><span data-stu-id="17a45-112">They must be able to determine whether that configuration contains constraint conflicts.</span></span>

-   <span data-ttu-id="17a45-113">Devono essere in grado di modificare un PrintTicket non valido o in conflitto apportando la modifica meno significativa necessaria per renderla valida e senza conflitti.</span><span class="sxs-lookup"><span data-stu-id="17a45-113">They must be able to modify an invalid or conflicting PrintTicket by making the least significant change necessary to make it both valid and without conflicts.</span></span>

-   <span data-ttu-id="17a45-114">Devono essere in grado di generare un documento PrintCapabilities per una particolare configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="17a45-114">They must be able to generate a PrintCapabilities document for a particular device configuration.</span></span>

-   <span data-ttu-id="17a45-115">Devono essere in grado di generare una configurazione predefinita o PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="17a45-115">They must be able to generate a default configuration or PrintTicket.</span></span>

-   <span data-ttu-id="17a45-116">Devono essere in grado di generare un documento PrintCapabilities corrispondente alla configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="17a45-116">They must be able to generate a PrintCapabilities document that corresponds to the default configuration.</span></span>

-   <span data-ttu-id="17a45-117">Devono implementare un processo di assegnazione dei punteggi delle opzioni definito dal driver di dispositivo in grado di determinare la vicinanza della corrispondenza tra due istanze option che appartengono alla stessa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="17a45-117">They must implement an Option-scoring process defined by the device driver capable of determining the closeness of match between two Option instances that belong to the same Feature.</span></span> <span data-ttu-id="17a45-118">Questo algoritmo viene usato nel processo di convalida PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="17a45-118">This algorithm is used in the PrintTicket validation process.</span></span>

<span data-ttu-id="17a45-119">Oltre ai requisiti, il documento PrintCapabilities deve contenere valori validi e corretti per ogni attributo XML ,ad esempio vincolato, di ogni opzione.</span><span class="sxs-lookup"><span data-stu-id="17a45-119">In addition to the foregoing requirements, the PrintCapabilities document must contain valid and correct values for each XML attribute (for example, constrained) of each Option.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17a45-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17a45-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17a45-121">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="17a45-121">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



