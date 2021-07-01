---
description: Informazioni su come supportare diverse versioni di Print Schema Framework. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: fc89dd2d-9a5d-400b-aee9-a1e4cf7d83da
title: Supporto delle versioni dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eac627d3dd711bc952d881efd393720af128e7f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120596"
---
# <a name="supporting-schema-versions"></a><span data-ttu-id="bd33d-105">Supporto delle versioni dello schema</span><span class="sxs-lookup"><span data-stu-id="bd33d-105">Supporting Schema Versions</span></span>

<span data-ttu-id="bd33d-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="bd33d-106">This topic is not current.</span></span> <span data-ttu-id="bd33d-107">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bd33d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bd33d-108">Print Schema Framework è soggetto a modifiche in futuro in base alle nuove esigenze.</span><span class="sxs-lookup"><span data-stu-id="bd33d-108">The Print Schema Framework is subject to change in the future as new needs arise.</span></span> <span data-ttu-id="bd33d-109">Si prevede che tali modifiche siano molto poco frequenti, perché la modifica più comune è l'introduzione di nuovi nomi di istanza.</span><span class="sxs-lookup"><span data-stu-id="bd33d-109">Such changes are expected to be very infrequent, because the most common change is the introduction of new instance names.</span></span> <span data-ttu-id="bd33d-110">Questa modifica non influisce sulla struttura del framework e deve essere trasparente per client e provider.</span><span class="sxs-lookup"><span data-stu-id="bd33d-110">This change does not affect the structure of the Framework, and should be transparent to clients and providers.</span></span> <span data-ttu-id="bd33d-111">Eventuali modifiche alla struttura e all'organizzazione di Print Schema Framework verranno identificate da incrementi al relativo numero di versione.</span><span class="sxs-lookup"><span data-stu-id="bd33d-111">Any changes to the structure and organization of the Print Schema Framework will be identified by increments to its version number.</span></span> <span data-ttu-id="bd33d-112">Le aggiunte alle parole chiave dello schema di stampa non verranno identificate.</span><span class="sxs-lookup"><span data-stu-id="bd33d-112">Additions to the Print Schema Keywords will not be identified.</span></span> <span data-ttu-id="bd33d-113">I provider PrintTicket devono essere in grado di supportare la versione corrente di Print Schema Framework, nonché qualsiasi versione precedente.</span><span class="sxs-lookup"><span data-stu-id="bd33d-113">PrintTicket providers must be capable of supporting the current Print Schema Framework version, as well as any prior version.</span></span> <span data-ttu-id="bd33d-114">La versione di Print Schema Framework viene identificata usando l'attributo XML: Version visualizzato nell'elemento radice di PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="bd33d-114">The Print Schema Framework version is identified using the XML Attribute: Version that appears at the root element of the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd33d-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd33d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd33d-116">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="bd33d-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



