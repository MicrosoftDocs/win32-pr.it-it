---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Rappresentazione di attributi come costrutti di funzionalità o di opzioni o come parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c24843a175337f40a84dcdacc41e1a2ab1e15e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104058482"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="2561b-104">Rappresentazione di attributi come costrutti di funzionalità o di opzioni o come parametri</span><span class="sxs-lookup"><span data-stu-id="2561b-104">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="2561b-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="2561b-105">This topic is not current.</span></span> <span data-ttu-id="2561b-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2561b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2561b-107">L'autore di un documento PrintCapabilities definisce gli attributi del dispositivo che costituiscono la configurazione.</span><span class="sxs-lookup"><span data-stu-id="2561b-107">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="2561b-108">Nel documento PrintCapabilities l'autore può scegliere di rappresentare un attributo di dispositivo come costrutto di funzionalità/opzione o come costrutto di parametro.</span><span class="sxs-lookup"><span data-stu-id="2561b-108">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="2561b-109">Se un attributo del dispositivo ha un numero relativamente ridotto di stati possibili che non rientrano in una sorta di modello ovvio, un costrutto di funzionalità/opzione è in genere la scelta migliore.</span><span class="sxs-lookup"><span data-stu-id="2561b-109">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="2561b-110">Se, ad esempio, i valori consentiti per l'attributo del dispositivo PageMediaSize sono i valori lettera, Legal, A4ISO, tabloid e Envelope10, un costrutto di funzionalità/opzione sarebbe la scelta migliore per la rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="2561b-110">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="2561b-111">A causa della difficoltà e dell'ambiguità associate all'espressione dei valori consentiti senza enumerazione esplicita, il costrutto di parametro non è appropriato per l'attributo PageMediaSize.</span><span class="sxs-lookup"><span data-stu-id="2561b-111">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="2561b-112">Se un attributo del dispositivo può essere rappresentato da un intervallo di numeri interi, la rappresentazione del parametro rappresenta in genere la scelta migliore, specialmente per gli intervalli che includono molti valori.</span><span class="sxs-lookup"><span data-stu-id="2561b-112">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="2561b-113">Se, ad esempio, l'attributo del dispositivo CopyCount per un determinato modello di stampante può variare da 1 a 99.999, questo attributo deve essere categorizzato come parametro, definendo un'istanza di ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="2561b-113">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="2561b-114">Assegnare i valori alle istanze di proprietà standard MinValue e MaxValue dell'elemento ParameterDef per definire l'intervallo di valori per l'attributo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="2561b-114">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="2561b-115">A causa dell'elevato numero di valori che devono essere elencati in modo esplicito come elementi option, la rappresentazione di funzionalità/opzioni non è appropriata per l'attributo del dispositivo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="2561b-115">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2561b-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2561b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2561b-117">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="2561b-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



