---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Limitazioni Schema-Imposed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc283704ea96e3303de6755a217e454b506bdc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321060"
---
# <a name="schema-imposed-limitations"></a><span data-ttu-id="dd740-104">Limitazioni Schema-Imposed</span><span class="sxs-lookup"><span data-stu-id="dd740-104">Schema-Imposed Limitations</span></span>

<span data-ttu-id="dd740-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="dd740-105">This topic is not current.</span></span> <span data-ttu-id="dd740-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dd740-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dd740-107">Lo schema PrintCapabilities fornisce agli autori PrintCapabilities un notevole livello di flessibilità ed espressività che possono essere utilizzati nelle descrizioni dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="dd740-107">The PrintCapabilities Schema provides PrintCapabilities authors with a substantial amount of flexibility and expressiveness that can be utilized in device descriptions.</span></span> <span data-ttu-id="dd740-108">Tuttavia, le dipendenze di configurazione impongono una limitazione sulla flessibilità e sull'espressività.</span><span class="sxs-lookup"><span data-stu-id="dd740-108">However, configuration dependencies impose a limitation on this flexibility and expressiveness.</span></span> <span data-ttu-id="dd740-109">Le istanze di ParameterDef, l'elenco di elementi Feature, l'elenco delle istanze di opzioni all'interno di ogni funzionalità e le istanze di ScoredProperty all'interno di ogni opzione non devono contenere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="dd740-109">ParameterDef instances, the list of Feature elements, the list of Option instances within each Feature, and the ScoredProperty instances within each Option must not contain configuration dependencies.</span></span> <span data-ttu-id="dd740-110">Il provider di documenti PrintCapabilities deve rilevare combinazioni di configurazioni non valide e deve risolverle.</span><span class="sxs-lookup"><span data-stu-id="dd740-110">The PrintCapabilities document provider must detect invalid combinations of configurations and must resolve them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd740-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dd740-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd740-112">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="dd740-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



