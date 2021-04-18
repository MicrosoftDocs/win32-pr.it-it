---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Riferimento allo schema di stampa legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881e986501950108c06e1e92303d13dc06265aae
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320956"
---
# <a name="legacy-print-schema-reference"></a><span data-ttu-id="ecf7c-104">Riferimento allo schema di stampa legacy</span><span class="sxs-lookup"><span data-stu-id="ecf7c-104">Legacy Print Schema Reference</span></span>

<span data-ttu-id="ecf7c-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ecf7c-105">This topic is not current.</span></span> <span data-ttu-id="ecf7c-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ecf7c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ecf7c-107">Lo schema di stampa e le tecnologie correlate sono disponibili in Microsoft .NET Framework 3,0, Microsoft Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ecf7c-107">The Print Schema and related technologies are available in the Microsoft .NET Framework 3.0, Microsoft Windows Vista, and later releases.</span></span>

<span data-ttu-id="ecf7c-108">Lo schema di stampa fornisce un formato basato su XML per esprimere e organizzare un ampio set di proprietà che descrivono un formato di processo o PrintCapabilities in modo gerarchico.</span><span class="sxs-lookup"><span data-stu-id="ecf7c-108">The Print Schema provides an XML-based format for expressing and organizing a large set of properties that describe either a job format or PrintCapabilities in a hierarchically structured manner.</span></span>

<span data-ttu-id="ecf7c-109">Lo schema di stampa è un termine che include due componenti, ovvero le parole chiave dello schema di stampa e il Framework dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="ecf7c-109">The Print Schema is an umbrella term that includes two components, the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="ecf7c-110">Il documento parole chiave di Print Schema è uno schema pubblico che definisce un set di istanze di elementi che possono essere usate per descrivere gli attributi del dispositivo e la formattazione del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="ecf7c-110">The Print Schema Keywords document is a public schema that defines a set of element instances that can be used to describe device attributes and print job formatting.</span></span> <span data-ttu-id="ecf7c-111">Print Schema Framework è uno schema pubblico che definisce una raccolta strutturata gerarchica di tipi di elemento XML e specifica come i tipi di elemento possono essere utilizzati insieme.</span><span class="sxs-lookup"><span data-stu-id="ecf7c-111">The Print Schema Framework is a public schema that defines a hierarchically structured collection of XML element types, and specifies how the element types can be used together.</span></span>

<span data-ttu-id="ecf7c-112">Le parole chiave dello schema di stampa e il Framework dello schema di stampa costituiscono la base per due tecnologie correlate allo schema di stampa, lo schema PrintCapabilities e lo schema PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="ecf7c-112">The Print Schema Keywords and the Print Schema Framework form the foundation for two Print Schema-related technologies, the PrintCapabilities Schema, and the PrintTicket Schema.</span></span>

<span data-ttu-id="ecf7c-113">È importante tenere presente che uno degli obiettivi dello schema di stampa è quello di supportare le estensioni dello schema per provider.</span><span class="sxs-lookup"><span data-stu-id="ecf7c-113">It is important to keep in mind that one of the goals of the Print Schema is to support schema extensions by providers.</span></span> <span data-ttu-id="ecf7c-114">Ovvero i provider non sono limitati all'utilizzo solo delle istanze di proprietà, funzionalità, opzione o ParameterInit definite nelle parole chiave dello schema di stampa nelle tecnologie compilate nel Framework dello schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="ecf7c-114">That is, providers are not restricted to using only those Property, Feature, Option, or ParameterInit instances defined in the Print Schema Keywords in the technologies built on the Print Schema Framework.</span></span> <span data-ttu-id="ecf7c-115">Le istanze degli elementi specifiche del provider possono essere liberamente sparpagliate nelle istanze degli elementi definite nelle parole chiave Print Schema.</span><span class="sxs-lookup"><span data-stu-id="ecf7c-115">Provider-specific element instances may be freely interspersed within element instances defined in the Print Schema Keywords.</span></span> <span data-ttu-id="ecf7c-116">L'unico requisito è che le istanze di proprietà specifiche del provider (ovvero private) devono appartenere a uno spazio dei nomi che è chiaramente associato al provider.</span><span class="sxs-lookup"><span data-stu-id="ecf7c-116">The only requirement is that provider-specific (that is, private) Property instances must belong to a namespace that is clearly associated with the provider.</span></span>

-   [<span data-ttu-id="ecf7c-117">Sfondo dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ecf7c-117">Print Schema Background</span></span>](print-schema-background.md)

-   [<span data-ttu-id="ecf7c-118">Tecnologie Schema-Related di stampa</span><span class="sxs-lookup"><span data-stu-id="ecf7c-118">Print Schema-Related Technologies</span></span>](print-schema-related-technologies.md)

-   [<span data-ttu-id="ecf7c-119">Termini usati nello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ecf7c-119">Terms Used in the Print Schema</span></span>](terms-used-in-the-print-schema.md)

-   [<span data-ttu-id="ecf7c-120">Sintassi dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ecf7c-120">Syntax of the Print Schema</span></span>](syntax-of-the-print-schema.md)

-   [<span data-ttu-id="ecf7c-121">Riepilogo dei tipi di elemento</span><span class="sxs-lookup"><span data-stu-id="ecf7c-121">Summary of Element Types</span></span>](summary-of-element-types.md)

-   [<span data-ttu-id="ecf7c-122">Print Schema Framework</span><span class="sxs-lookup"><span data-stu-id="ecf7c-122">Print Schema Framework</span></span>](print-schema-framework.md)

-   [<span data-ttu-id="ecf7c-123">Parole chiave pubbliche dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ecf7c-123">Print Schema Public Keywords</span></span>](print-schema-public-keywords.md)

-   [<span data-ttu-id="ecf7c-124">Struttura del documento e dello schema PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="ecf7c-124">PrintCapabilities Schema and Document Construction</span></span>](printcapabilities-schema-and-document-construction.md)

-   [<span data-ttu-id="ecf7c-125">Schema e costruzione di documenti PrintTicket</span><span class="sxs-lookup"><span data-stu-id="ecf7c-125">PrintTicket Schema and Document Construction</span></span>](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a><span data-ttu-id="ecf7c-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ecf7c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecf7c-127">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="ecf7c-127">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



