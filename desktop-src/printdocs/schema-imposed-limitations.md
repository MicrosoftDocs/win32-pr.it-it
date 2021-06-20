---
description: Informazioni sulle limitazioni imposte dallo schema PrintCapabilities. Il provider PrintCapabilities deve rilevare le configurazioni non valide e risolverle.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Schema-Imposed limitazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2911d4b90ebc194aa245f398f71575496c877
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404924"
---
# <a name="schema-imposed-limitations"></a><span data-ttu-id="b36a2-104">Schema-Imposed limitazioni</span><span class="sxs-lookup"><span data-stu-id="b36a2-104">Schema-Imposed Limitations</span></span>

<span data-ttu-id="b36a2-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="b36a2-105">This topic is not current.</span></span> <span data-ttu-id="b36a2-106">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b36a2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b36a2-107">Lo schema PrintCapabilities offre agli autori PrintCapabilities una notevole quantità di flessibilità ed espressività che possono essere utilizzate nelle descrizioni dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b36a2-107">The PrintCapabilities Schema provides PrintCapabilities authors with a substantial amount of flexibility and expressiveness that can be utilized in device descriptions.</span></span> <span data-ttu-id="b36a2-108">Tuttavia, le dipendenze di configurazione impongono una limitazione a questa flessibilità ed espressività.</span><span class="sxs-lookup"><span data-stu-id="b36a2-108">However, configuration dependencies impose a limitation on this flexibility and expressiveness.</span></span> <span data-ttu-id="b36a2-109">Le istanze ParameterDef, l'elenco di elementi Feature, l'elenco di istanze Option all'interno di ogni feature e le istanze ScoredProperty all'interno di ogni opzione non devono contenere dipendenze di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b36a2-109">ParameterDef instances, the list of Feature elements, the list of Option instances within each Feature, and the ScoredProperty instances within each Option must not contain configuration dependencies.</span></span> <span data-ttu-id="b36a2-110">Il provider di documenti PrintCapabilities deve rilevare combinazioni di configurazioni non valide e risolverle.</span><span class="sxs-lookup"><span data-stu-id="b36a2-110">The PrintCapabilities document provider must detect invalid combinations of configurations and must resolve them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b36a2-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b36a2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b36a2-112">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="b36a2-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



