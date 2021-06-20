---
description: Questa panoramica descrive lo schema di stampa e i collegamenti agli argomenti di riferimento sullo schema di stampa. Lo schema di stampa include le parole chiave dello schema di stampa e il framework.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Riferimento allo schema di stampa legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a8f417d20913563cfd4a52ba51d21b516e73f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407134"
---
# <a name="legacy-print-schema-reference"></a><span data-ttu-id="91528-104">Riferimento allo schema di stampa legacy</span><span class="sxs-lookup"><span data-stu-id="91528-104">Legacy Print Schema Reference</span></span>

<span data-ttu-id="91528-105">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="91528-105">This topic is not current.</span></span> <span data-ttu-id="91528-106">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="91528-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="91528-107">Lo schema di stampa e le tecnologie correlate sono disponibili in Microsoft .NET Framework 3.0, Microsoft Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="91528-107">The Print Schema and related technologies are available in the Microsoft .NET Framework 3.0, Microsoft Windows Vista, and later releases.</span></span>

<span data-ttu-id="91528-108">Lo schema di stampa fornisce un formato basato su XML per esprimere e organizzare un ampio set di proprietà che descrivono un formato di processo o PrintCapabilities in modo strutturato gerarchicamente.</span><span class="sxs-lookup"><span data-stu-id="91528-108">The Print Schema provides an XML-based format for expressing and organizing a large set of properties that describe either a job format or PrintCapabilities in a hierarchically structured manner.</span></span>

<span data-ttu-id="91528-109">Lo schema di stampa è un termine generico che include due componenti, Print Schema Keywords e Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="91528-109">The Print Schema is an umbrella term that includes two components, the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="91528-110">Il documento Print Schema Keywords (Parole chiave dello schema di stampa) è uno schema pubblico che definisce un set di istanze di elementi che possono essere usate per descrivere gli attributi del dispositivo e la formattazione del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="91528-110">The Print Schema Keywords document is a public schema that defines a set of element instances that can be used to describe device attributes and print job formatting.</span></span> <span data-ttu-id="91528-111">Print Schema Framework è uno schema pubblico che definisce una raccolta strutturata gerarchicamente di tipi di elementi XML e specifica come i tipi di elemento possono essere usati insieme.</span><span class="sxs-lookup"><span data-stu-id="91528-111">The Print Schema Framework is a public schema that defines a hierarchically structured collection of XML element types, and specifies how the element types can be used together.</span></span>

<span data-ttu-id="91528-112">Le parole chiave dello schema di stampa e il framework dello schema di stampa sono alla base di due tecnologie correlate allo schema di stampa, lo schema PrintCapabilities e lo schema PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="91528-112">The Print Schema Keywords and the Print Schema Framework form the foundation for two Print Schema-related technologies, the PrintCapabilities Schema, and the PrintTicket Schema.</span></span>

<span data-ttu-id="91528-113">È importante tenere presente che uno degli obiettivi dello schema di stampa è il supporto delle estensioni dello schema da parte dei provider.</span><span class="sxs-lookup"><span data-stu-id="91528-113">It is important to keep in mind that one of the goals of the Print Schema is to support schema extensions by providers.</span></span> <span data-ttu-id="91528-114">Ciò significa che i provider non sono limitati all'uso solo delle istanze Property, Feature, Option o ParameterInit definite nelle parole chiave dello schema di stampa nelle tecnologie compilate in Print Schema Framework.</span><span class="sxs-lookup"><span data-stu-id="91528-114">That is, providers are not restricted to using only those Property, Feature, Option, or ParameterInit instances defined in the Print Schema Keywords in the technologies built on the Print Schema Framework.</span></span> <span data-ttu-id="91528-115">Le istanze di elemento specifiche del provider possono essere liberamente intercambiate all'interno di istanze di elemento definite nelle parole chiave dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="91528-115">Provider-specific element instances may be freely interspersed within element instances defined in the Print Schema Keywords.</span></span> <span data-ttu-id="91528-116">L'unico requisito è che le istanze di proprietà specifiche del provider (ovvero private) appartengano a uno spazio dei nomi chiaramente associato al provider.</span><span class="sxs-lookup"><span data-stu-id="91528-116">The only requirement is that provider-specific (that is, private) Property instances must belong to a namespace that is clearly associated with the provider.</span></span>

-   [<span data-ttu-id="91528-117">Stampare lo sfondo dello schema</span><span class="sxs-lookup"><span data-stu-id="91528-117">Print Schema Background</span></span>](print-schema-background.md)

-   [<span data-ttu-id="91528-118">Tecnologie di Schema-Related stampa</span><span class="sxs-lookup"><span data-stu-id="91528-118">Print Schema-Related Technologies</span></span>](print-schema-related-technologies.md)

-   [<span data-ttu-id="91528-119">Termini usati nello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="91528-119">Terms Used in the Print Schema</span></span>](terms-used-in-the-print-schema.md)

-   [<span data-ttu-id="91528-120">Sintassi dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="91528-120">Syntax of the Print Schema</span></span>](syntax-of-the-print-schema.md)

-   [<span data-ttu-id="91528-121">Riepilogo dei tipi di elemento</span><span class="sxs-lookup"><span data-stu-id="91528-121">Summary of Element Types</span></span>](summary-of-element-types.md)

-   [<span data-ttu-id="91528-122">Framework dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="91528-122">Print Schema Framework</span></span>](print-schema-framework.md)

-   [<span data-ttu-id="91528-123">Parole chiave pubbliche dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="91528-123">Print Schema Public Keywords</span></span>](print-schema-public-keywords.md)

-   [<span data-ttu-id="91528-124">Schema PrintCapabilities e costruzione di documenti</span><span class="sxs-lookup"><span data-stu-id="91528-124">PrintCapabilities Schema and Document Construction</span></span>](printcapabilities-schema-and-document-construction.md)

-   [<span data-ttu-id="91528-125">Schema PrintTicket e costruzione di documenti</span><span class="sxs-lookup"><span data-stu-id="91528-125">PrintTicket Schema and Document Construction</span></span>](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a><span data-ttu-id="91528-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91528-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91528-127">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="91528-127">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



