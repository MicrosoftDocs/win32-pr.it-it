---
description: Informazioni sulle definizioni dei parametri in un documento PrintCapabilities. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Definizioni dei parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc8ad2bed3a972202bc0a5bb07cbdd4ef9d8f44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396576"
---
# <a name="parameter-definitions"></a><span data-ttu-id="3dba2-105">Definizioni dei parametri</span><span class="sxs-lookup"><span data-stu-id="3dba2-105">Parameter Definitions</span></span>

<span data-ttu-id="3dba2-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="3dba2-106">This topic is not current.</span></span> <span data-ttu-id="3dba2-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3dba2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3dba2-108">Questa sezione descrive le definizioni dei parametri pubblici che possono essere visualizzate in un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="3dba2-108">This section outlines the public parameter definitions which may appear in either a PrintCapabilities document.</span></span>

<span data-ttu-id="3dba2-109">I parametri vengono usati per descrivere un intervallo di valori accettabile, anziché un'enumerazione discreta di valori.</span><span class="sxs-lookup"><span data-stu-id="3dba2-109">Parameters are used to describe an acceptable range of values, rather than a discrete enumeration of values.</span></span>

## <a name="parameterdef"></a><span data-ttu-id="3dba2-110">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3dba2-110">ParameterDef</span></span>

<span data-ttu-id="3dba2-111">Per un riepilogo del tipo di elemento ParameterDef, vedere la [sezione ParameterDef.](parameterdef.md)</span><span class="sxs-lookup"><span data-stu-id="3dba2-111">For a summary of the ParameterDef element type, please refer to [ParameterDef](parameterdef.md) section.</span></span>

<span data-ttu-id="3dba2-112">Per altre informazioni sull'interazione tra elementi ParameterDef ed elementi ParameterInit, vedere la [sezione Elementi ParameterDef e ParameterInit.](./parameterdef-and-parameterinit-elements.md)</span><span class="sxs-lookup"><span data-stu-id="3dba2-112">For more information on the interaction between ParameterDef elements and ParameterInit elements, refer to [ParameterDef and ParameterInit Elements](./parameterdef-and-parameterinit-elements.md) section.</span></span>

<span data-ttu-id="3dba2-113">Gli elementi ParameterDef definiti nelle parole chiave dello schema di stampa devono essere definiti completamente in un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="3dba2-113">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span>

## <a name="parameterref"></a><span data-ttu-id="3dba2-114">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="3dba2-114">ParameterRef</span></span>

<span data-ttu-id="3dba2-115">Per un riepilogo del tipo di elemento ParameterRef, vedere la [sezione ParameterRef.](parameterref.md)</span><span class="sxs-lookup"><span data-stu-id="3dba2-115">For a summary of the ParameterRef element type, please refer to [ParameterRef](parameterref.md) section.</span></span>

<span data-ttu-id="3dba2-116">Una parola chiave dell'elemento configurabile dall'utente può contenere un riferimento a un parametro.</span><span class="sxs-lookup"><span data-stu-id="3dba2-116">A user configurable element keyword may contain a reference to a Parameter.</span></span> <span data-ttu-id="3dba2-117">Gli elementi ParameterRef vengono specificati come elementi figlio di un elemento ScoredProperty. Per altre informazioni, vedere la [sezione Elementi di riferimento ai](parameter-reference-elements.md) parametri.</span><span class="sxs-lookup"><span data-stu-id="3dba2-117">ParameterRef elements are specified as a child of a ScoredProperty element For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dba2-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3dba2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dba2-119">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="3dba2-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
