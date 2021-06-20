---
description: Informazioni sulla sintassi dello schema di stampa, espressa nella sintassi XML ed è costituita da un numero ridotto di tipi di elementi.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Sintassi dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef52dbdbdfacc2d3cc947b46558319577a75b1b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405294"
---
# <a name="syntax-of-the-print-schema"></a><span data-ttu-id="3caef-103">Sintassi dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="3caef-103">Syntax of the Print Schema</span></span>

<span data-ttu-id="3caef-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="3caef-104">This topic is not current.</span></span> <span data-ttu-id="3caef-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3caef-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3caef-106">Lo schema di stampa è espresso nella sintassi XML.</span><span class="sxs-lookup"><span data-stu-id="3caef-106">The Print Schema is expressed in XML syntax.</span></span> <span data-ttu-id="3caef-107">È quindi previsto che i lettori conoscano la sintassi XML e termini come elemento, tag di elemento, contenuto degli elementi, attributo e spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3caef-107">Readers are therefore expected to be familiar with XML syntax and terms such as element, element tag, element content, attribute, and namespace.</span></span> <span data-ttu-id="3caef-108">Print Schema Framework è costituito da un numero ridotto di tipi di elementi. ogni tipo di elemento ha uno scopo specifico nelle tecnologie create sullo schema di stampa.</span><span class="sxs-lookup"><span data-stu-id="3caef-108">The Print Schema Framework is composed of a small number of element types; each element type serves a specific purpose in the technologies built on the Print Schema.</span></span>

<span data-ttu-id="3caef-109">I tipi di elemento vengono distinti in base al tag dell'elemento XML.</span><span class="sxs-lookup"><span data-stu-id="3caef-109">Element types are distinguished by their XML element tag.</span></span> <span data-ttu-id="3caef-110">Print Schema Framework definisce la struttura complessiva e l'organizzazione delle tecnologie dipendenti, indicando per ogni tipo di elemento quali tipi di elemento sono consentiti come elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="3caef-110">The Print Schema Framework defines the overall structure and organization of the dependent technologies, by denoting for each element type which element types are allowed as child elements.</span></span>

<span data-ttu-id="3caef-111">Molti tipi di elementi sono differenziati da altri dello stesso tipo in base all'attributo name, che svolge un ruolo significativo nello schema.</span><span class="sxs-lookup"><span data-stu-id="3caef-111">Many element types are differentiated from others of the same type by the name attribute, which plays a significant role in the schema.</span></span> <span data-ttu-id="3caef-112">L'attributo name serve per identificare le istanze di ogni tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="3caef-112">The name attribute serves to identify instances of each element type.</span></span> <span data-ttu-id="3caef-113">Le parole chiave dello schema di stampa definiscono un set di valori per l'attributo name per molti dei tipi di elemento.</span><span class="sxs-lookup"><span data-stu-id="3caef-113">The Print Schema Keywords defines a set of values for the name attribute for many of the element types.</span></span> <span data-ttu-id="3caef-114">Nella maggior parte dei casi, i provider possono assegnare i propri valori all'attributo name.</span><span class="sxs-lookup"><span data-stu-id="3caef-114">In most cases, providers can assign their own values to the name attribute.</span></span> <span data-ttu-id="3caef-115">È necessario assicurarsi che i valori siano QName XML qualificati con uno spazio dei nomi univoco per il provider.</span><span class="sxs-lookup"><span data-stu-id="3caef-115">They need only ensure the values are XML QNames qualified with a namespace that is unique to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3caef-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3caef-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3caef-117">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="3caef-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



