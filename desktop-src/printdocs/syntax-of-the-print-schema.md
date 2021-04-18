---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Sintassi dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2503b3f44ff8b4bdda41f0feefe374c27d78bd41
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321033"
---
# <a name="syntax-of-the-print-schema"></a><span data-ttu-id="8b681-104">Sintassi dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="8b681-104">Syntax of the Print Schema</span></span>

<span data-ttu-id="8b681-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="8b681-105">This topic is not current.</span></span> <span data-ttu-id="8b681-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8b681-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8b681-107">Lo schema di stampa è espresso in sintassi XML.</span><span class="sxs-lookup"><span data-stu-id="8b681-107">The Print Schema is expressed in XML syntax.</span></span> <span data-ttu-id="8b681-108">È quindi previsto che i lettori abbiano familiarità con la sintassi XML e con termini quali elemento, tag dell'elemento, contenuto dell'elemento, attributo e spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="8b681-108">Readers are therefore expected to be familiar with XML syntax and terms such as element, element tag, element content, attribute, and namespace.</span></span> <span data-ttu-id="8b681-109">Il Framework dello schema di stampa è costituito da un numero ridotto di tipi di elementi. ogni tipo di elemento svolge uno scopo specifico nelle tecnologie basate sullo schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="8b681-109">The Print Schema Framework is composed of a small number of element types; each element type serves a specific purpose in the technologies built on the Print Schema.</span></span>

<span data-ttu-id="8b681-110">I tipi di elemento sono distinti in base al tag dell'elemento XML.</span><span class="sxs-lookup"><span data-stu-id="8b681-110">Element types are distinguished by their XML element tag.</span></span> <span data-ttu-id="8b681-111">Il Framework dello schema di stampa definisce la struttura complessiva e l'organizzazione delle tecnologie dipendenti, indicando per ogni tipo di elemento quali tipi di elemento sono consentiti come elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="8b681-111">The Print Schema Framework defines the overall structure and organization of the dependent technologies, by denoting for each element type which element types are allowed as child elements.</span></span>

<span data-ttu-id="8b681-112">Molti tipi di elementi sono differenziati rispetto ad altri dello stesso tipo dall'attributo Name, che svolge un ruolo significativo nello schema.</span><span class="sxs-lookup"><span data-stu-id="8b681-112">Many element types are differentiated from others of the same type by the name attribute, which plays a significant role in the schema.</span></span> <span data-ttu-id="8b681-113">L'attributo Name serve a identificare le istanze di ogni tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="8b681-113">The name attribute serves to identify instances of each element type.</span></span> <span data-ttu-id="8b681-114">Le parole chiave Print Schema definiscono un set di valori per l'attributo Name per molti tipi di elemento.</span><span class="sxs-lookup"><span data-stu-id="8b681-114">The Print Schema Keywords defines a set of values for the name attribute for many of the element types.</span></span> <span data-ttu-id="8b681-115">Nella maggior parte dei casi, i provider possono assegnare i propri valori all'attributo Name.</span><span class="sxs-lookup"><span data-stu-id="8b681-115">In most cases, providers can assign their own values to the name attribute.</span></span> <span data-ttu-id="8b681-116">Sono necessarie solo per assicurarsi che i valori siano QName XML qualificati con uno spazio dei nomi univoco per il provider.</span><span class="sxs-lookup"><span data-stu-id="8b681-116">They need only ensure the values are XML QNames qualified with a namespace that is unique to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b681-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8b681-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b681-118">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="8b681-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



