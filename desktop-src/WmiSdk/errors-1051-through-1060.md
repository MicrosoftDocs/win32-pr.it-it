---
description: Descrive gli errori del provider SNMP WMI da 1051 a 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Errori da 1051 a 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170eddf3126a40f929aa36899259b731fa244941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315726"
---
# <a name="errors-1051-through-1060"></a><span data-ttu-id="9547c-103">Errori da 1051 a 1060</span><span class="sxs-lookup"><span data-stu-id="9547c-103">Errors 1051 through 1060</span></span>

<span data-ttu-id="9547c-104">Descrive gli errori del provider SNMP WMI da 1051 a 1060.</span><span class="sxs-lookup"><span data-stu-id="9547c-104">Describes WMI SNMP provider errors 1051 through 1060.</span></span>

[<span data-ttu-id="9547c-105">Errore irreversibile 1051</span><span class="sxs-lookup"><span data-stu-id="9547c-105">Fatal Error 1051</span></span>](#fatal-error-1051)

[<span data-ttu-id="9547c-106">Errore irreversibile 1054</span><span class="sxs-lookup"><span data-stu-id="9547c-106">Fatal Error 1054</span></span>](#fatal-error-1054)

[<span data-ttu-id="9547c-107">Errore irreversibile 1055</span><span class="sxs-lookup"><span data-stu-id="9547c-107">Fatal Error 1055</span></span>](#fatal-error-1055)

## <a name="fatal-error-1051"></a><span data-ttu-id="9547c-108">Errore irreversibile 1051</span><span class="sxs-lookup"><span data-stu-id="9547c-108">Fatal Error 1051</span></span>

<dl> <dt>

<span data-ttu-id="9547c-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051,> irreversibile: " <fileName> : <riga \#>: riferimento ambiguo al simbolo <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="9547c-109"><span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Fatal>: "<fileName>:<line\#>: Ambiguous reference to symbol <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="9547c-110">Errore semantico del modulo della sezione Imports, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9547c-110">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="9547c-111">Ogni descrittore di oggetto che corrisponde a un oggetto in un MIB standard Internet deve essere univoco.</span><span class="sxs-lookup"><span data-stu-id="9547c-111">Each object descriptor corresponding to an object in an Internet Standard MIB must be unique.</span></span> <span data-ttu-id="9547c-112">Poiché MIB aziendali possono avere descrittori di oggetto comuni, i descrittori importati da due moduli devono essere usati senza ambiguità nel modulo MIB usando la notazione "Module. Descriptor".</span><span class="sxs-lookup"><span data-stu-id="9547c-112">Since enterprise MIBs can have common object descriptors, such descriptors imported from two modules must be used unambiguously in the MIB module by using the notation "module.descriptor."</span></span>

</dd> </dl>

## <a name="fatal-error-1054"></a><span data-ttu-id="9547c-113">Errore irreversibile 1054</span><span class="sxs-lookup"><span data-stu-id="9547c-113">Fatal Error 1054</span></span>

<dl> <dt>

<span data-ttu-id="9547c-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054,> irreversibile: " <fileName> : <riga \#>: <identifier> nella clausola index non viene risolto in uno dei tipi consentiti"**</span><span class="sxs-lookup"><span data-stu-id="9547c-114"><span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, Fatal>: "<fileName>:<line\#>: <identifier> in INDEX clause does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="9547c-115">Errore semantico del modulo di chiamata macro del **tipo di oggetto** .</span><span class="sxs-lookup"><span data-stu-id="9547c-115">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="9547c-116">Il tipo di un oggetto nella clausola INDEX, o qualsiasi tipo specificato nella clausola INDEX, deve essere risolto in un tipo scalare, ovvero in una sequenza non sequenziale o non in sequenza di tipo.</span><span class="sxs-lookup"><span data-stu-id="9547c-116">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span> <span data-ttu-id="9547c-117">Qualsiasi tipo specificato nella clausola INDEX deve essere risolto anche in uno di questi.</span><span class="sxs-lookup"><span data-stu-id="9547c-117">Any type specified in the INDEX clause must also resolve to one of these.</span></span>

<span data-ttu-id="9547c-118">Questo errore può verificarsi in SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9547c-118">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1055"></a><span data-ttu-id="9547c-119">Errore irreversibile 1055</span><span class="sxs-lookup"><span data-stu-id="9547c-119">Fatal Error 1055</span></span>

<dl> <dt>

<span data-ttu-id="9547c-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055,> irreversibile: " <fileName> : <riga \#>: sintassi del tipo di oggetto index <identifier> , non viene risolto in uno dei tipi consentiti"**</span><span class="sxs-lookup"><span data-stu-id="9547c-120"><span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, Fatal>:"<fileName>:<line\#>: SYNTAX of INDEX OBJECT-TYPE <identifier>, does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="9547c-121">Errore semantico del modulo di chiamata macro del **tipo di oggetto** .</span><span class="sxs-lookup"><span data-stu-id="9547c-121">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="9547c-122">Il tipo di un oggetto nella clausola INDEX, o qualsiasi tipo specificato nella clausola INDEX, deve essere risolto in un tipo scalare, ovvero in una sequenza non sequenziale o non in sequenza di tipo.</span><span class="sxs-lookup"><span data-stu-id="9547c-122">The type of an object in the INDEX clause, or any type specified in the INDEX clause, must resolve to a scalar type, that is, a non-SEQUENCE or non-SEQUENCE OF type.</span></span>

<span data-ttu-id="9547c-123">Questo errore può verificarsi in SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="9547c-123">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



