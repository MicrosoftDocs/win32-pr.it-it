---
description: Rappresentano gli attributi come costrutti di funzionalità/opzione o come parametri. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Rappresentazione di attributi come costrutti di funzionalità/opzioni o come parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c93f4de56709ed310a7f0aa259b1dbfd3377ed42
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120056"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a><span data-ttu-id="46450-105">Rappresentazione di attributi come costrutti di funzionalità/opzioni o come parametri</span><span class="sxs-lookup"><span data-stu-id="46450-105">Representing Attributes as Feature/Option Constructs or as Parameters</span></span>

<span data-ttu-id="46450-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="46450-106">This topic is not current.</span></span> <span data-ttu-id="46450-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="46450-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="46450-108">L'autore di un documento PrintCapabilities definisce gli attributi del dispositivo che costituiscono la configurazione.</span><span class="sxs-lookup"><span data-stu-id="46450-108">The author of a PrintCapabilities document defines device attributes that make up the configuration.</span></span> <span data-ttu-id="46450-109">Nel documento PrintCapabilities l'autore può scegliere di rappresentare un attributo del dispositivo come costrutto Feature/Option o come costrutto di parametro.</span><span class="sxs-lookup"><span data-stu-id="46450-109">In the PrintCapabilities document, the author can choose to represent a device attribute either as a Feature/Option construct or as a parameter construct.</span></span>

<span data-ttu-id="46450-110">Se un attributo del dispositivo ha un numero relativamente ridotto di possibili stati che non rientrano in alcun tipo di modello ovvio, un costrutto di funzionalità/opzione è in genere la scelta migliore.</span><span class="sxs-lookup"><span data-stu-id="46450-110">If a device attribute has a relatively small number of possible states that do not fall into any sort of obvious pattern, a Feature/Option construct is usually the better choice.</span></span> <span data-ttu-id="46450-111">Ad esempio, se i valori consentiti per l'attributo di dispositivo PageMediaSize sono i valori Letter, Legal, A4ISO, Tabloid e Envelope10, un costrutto Feature/Option è la scelta migliore per la rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="46450-111">For example, if the allowed values for the PageMediaSize device attribute are the values Letter, Legal, A4ISO, Tabloid, and Envelope10, a Feature/Option construct would be the better choice for representation.</span></span> <span data-ttu-id="46450-112">A causa della difficoltà e dell'ambiguità associate all'espressione dei valori consentiti senza enumerazione esplicita, il costrutto di parametro non è appropriato per l'attributo PageMediaSize.</span><span class="sxs-lookup"><span data-stu-id="46450-112">Because of the difficulty and ambiguity associated with expressing the allowable values without explicit enumeration, the parameter construct is not appropriate for the PageMediaSize attribute.</span></span>

<span data-ttu-id="46450-113">Se un attributo del dispositivo può essere rappresentato da un intervallo di numeri interi, la rappresentazione dei parametri è in genere la scelta migliore, soprattutto per gli intervalli che includono molti valori.</span><span class="sxs-lookup"><span data-stu-id="46450-113">If a device attribute can be represented by a range of integers, parameter representation is usually the better choice, especially for ranges that include many values.</span></span> <span data-ttu-id="46450-114">Ad esempio, se l'attributo di dispositivo CopyCount per un particolare modello di stampante può variare da 1 a 99.999, questo attributo deve essere categorizzato come parametro, definendo un'istanza ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="46450-114">For example, if the CopyCount device attribute for a particular model of printer can range from 1 through 99,999, then this attribute should be categorized as a parameter, by defining a ParameterDef instance.</span></span> <span data-ttu-id="46450-115">Assegnare valori alle istanze delle proprietà standard MinValue e MaxValue dell'elemento ParameterDef per definire l'intervallo di valori per l'attributo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="46450-115">Assign values to the MinValue and MaxValue standard Property instances of the ParameterDef element to define the range of values for the JobCopyCount attribute.</span></span> <span data-ttu-id="46450-116">A causa del numero elevato di valori che devono essere elencati in modo esplicito come elementi Option, la rappresentazione di funzionalità/opzioni non è appropriata per l'attributo del dispositivo JobCopyCount.</span><span class="sxs-lookup"><span data-stu-id="46450-116">Because of the large number of values that must be explicitly listed as Option elements, Feature/Option representation is not appropriate for the JobCopyCount device attribute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46450-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46450-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46450-118">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="46450-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



