---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Definizioni dei parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5a71bfc5a5111a826b5d221ff1436ecf921dd2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234571"
---
# <a name="parameter-definitions"></a><span data-ttu-id="9c8f7-104">Definizioni dei parametri</span><span class="sxs-lookup"><span data-stu-id="9c8f7-104">Parameter Definitions</span></span>

<span data-ttu-id="9c8f7-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="9c8f7-105">This topic is not current.</span></span> <span data-ttu-id="9c8f7-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9c8f7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9c8f7-107">In questa sezione vengono descritte le definizioni dei parametri pubblici che possono essere visualizzate in un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="9c8f7-107">This section outlines the public parameter definitions which may appear in either a PrintCapabilities document.</span></span>

<span data-ttu-id="9c8f7-108">I parametri vengono usati per descrivere un intervallo di valori accettabile, anziché un'enumerazione discreta di valori.</span><span class="sxs-lookup"><span data-stu-id="9c8f7-108">Parameters are used to describe an acceptable range of values, rather than a discrete enumeration of values.</span></span>

## <a name="parameterdef"></a><span data-ttu-id="9c8f7-109">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="9c8f7-109">ParameterDef</span></span>

<span data-ttu-id="9c8f7-110">Per un riepilogo del tipo di elemento ParameterDef, vedere la sezione [ParameterDef](parameterdef.md) .</span><span class="sxs-lookup"><span data-stu-id="9c8f7-110">For a summary of the ParameterDef element type, please refer to [ParameterDef](parameterdef.md) section.</span></span>

<span data-ttu-id="9c8f7-111">Per altre informazioni sull'interazione tra gli elementi ParameterDef e gli elementi ParameterInit, vedere la sezione [elementi ParameterDef e ParameterInit](./parameterdef-and-parameterinit-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="9c8f7-111">For more information on the interaction between ParameterDef elements and ParameterInit elements, refer to [ParameterDef and ParameterInit Elements](./parameterdef-and-parameterinit-elements.md) section.</span></span>

<span data-ttu-id="9c8f7-112">Gli elementi ParameterDef definiti nelle parole chiave Print Schema devono essere definiti completamente in un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="9c8f7-112">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span>

## <a name="parameterref"></a><span data-ttu-id="9c8f7-113">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="9c8f7-113">ParameterRef</span></span>

<span data-ttu-id="9c8f7-114">Per un riepilogo del tipo di elemento ParameterRef, vedere la sezione [ParameterRef](parameterref.md) .</span><span class="sxs-lookup"><span data-stu-id="9c8f7-114">For a summary of the ParameterRef element type, please refer to [ParameterRef](parameterref.md) section.</span></span>

<span data-ttu-id="9c8f7-115">Una parola chiave dell'elemento configurabile dall'utente può contenere un riferimento a un parametro.</span><span class="sxs-lookup"><span data-stu-id="9c8f7-115">A user configurable element keyword may contain a reference to a Parameter.</span></span> <span data-ttu-id="9c8f7-116">Gli elementi ParameterRef vengono specificati come elementi figlio di un elemento ScoredProperty per altre informazioni. vedere la sezione [elementi di riferimento ai parametri](parameter-reference-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="9c8f7-116">ParameterRef elements are specified as a child of a ScoredProperty element For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c8f7-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c8f7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c8f7-118">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="9c8f7-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
