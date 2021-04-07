---
description: Descrive gli errori del provider SNMP WMI da 1011 a 1020.
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: Errori da 1011 a 1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a73f90ce0fc161604d87672fb5b33f9708aa945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058017"
---
# <a name="errors-1011-through-1020"></a><span data-ttu-id="98901-103">Errori da 1011 a 1020</span><span class="sxs-lookup"><span data-stu-id="98901-103">Errors 1011 through 1020</span></span>

<span data-ttu-id="98901-104">Descrive gli errori del provider SNMP WMI da 1011 a 1020.</span><span class="sxs-lookup"><span data-stu-id="98901-104">Describes WMI SNMP provider errors 1011 through 1020.</span></span>

[<span data-ttu-id="98901-105">Errore irreversibile 1011</span><span class="sxs-lookup"><span data-stu-id="98901-105">Fatal Error 1011</span></span>](#fatal-error-1011)

[<span data-ttu-id="98901-106">Errore irreversibile 1012</span><span class="sxs-lookup"><span data-stu-id="98901-106">Fatal Error 1012</span></span>](#fatal-error-1012)

[<span data-ttu-id="98901-107">Errore irreversibile 1013</span><span class="sxs-lookup"><span data-stu-id="98901-107">Fatal Error 1013</span></span>](#fatal-error-1013)

[<span data-ttu-id="98901-108">Avviso 1014</span><span class="sxs-lookup"><span data-stu-id="98901-108">Warning 1014</span></span>](#warning-1014)

[<span data-ttu-id="98901-109">Errore irreversibile 1015</span><span class="sxs-lookup"><span data-stu-id="98901-109">Fatal Error 1015</span></span>](#fatal-error-1015)

[<span data-ttu-id="98901-110">Errore irreversibile 1016</span><span class="sxs-lookup"><span data-stu-id="98901-110">Fatal Error 1016</span></span>](#fatal-error-1016)

[<span data-ttu-id="98901-111">Errore irreversibile 1018</span><span class="sxs-lookup"><span data-stu-id="98901-111">Fatal Error 1018</span></span>](#fatal-error-1018)

[<span data-ttu-id="98901-112">Errore irreversibile 1020</span><span class="sxs-lookup"><span data-stu-id="98901-112">Fatal Error 1020</span></span>](#fatal-error-1020)

## <a name="fatal-error-1011"></a><span data-ttu-id="98901-113">Errore irreversibile 1011</span><span class="sxs-lookup"><span data-stu-id="98901-113">Fatal Error 1011</span></span>

<dl> <dt>

<span data-ttu-id="98901-114"><span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011,> irreversibile: " <fileName> : <riga \#> la sintassi del membro <identifier> della sequenza, <identifier> , differisce dalla clausola della sintassi del tipo di oggetto"**</span><span class="sxs-lookup"><span data-stu-id="98901-114"><span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011, Fatal>: "<fileName>:<line\#> the SYNTAX of member <identifier> of SEQUENCE, <identifier>, differs from the SYNTAX clause of the OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="98901-115">Errore semantico del modulo di chiamata macro del **tipo di oggetto** .</span><span class="sxs-lookup"><span data-stu-id="98901-115">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="98901-116">Un elemento di una sequenza deve essere uguale al tipo nella clausola SYNTAX della definizione del tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="98901-116">An element of a SEQUENCE must be same as the type in the SYNTAX clause of the OBJECT-TYPE definition.</span></span> <span data-ttu-id="98901-117">Il <riga \#> parametro è la riga della clausola della sintassi della definizione del tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="98901-117">The <line\#> parameter is the line of the SYNTAX clause of the OBJECT-TYPE definition.</span></span>

<span data-ttu-id="98901-118">Questo errore può verificarsi in SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="98901-118">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1012"></a><span data-ttu-id="98901-119">Errore irreversibile 1012</span><span class="sxs-lookup"><span data-stu-id="98901-119">Fatal Error 1012</span></span>

<dl> <dt>

<span data-ttu-id="98901-120"><span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012,> irreversibile: " <fileName> : <riga \#> una clausola index o augmentes è obbligatoria solo per i tipi di oggetto sequenza"**</span><span class="sxs-lookup"><span data-stu-id="98901-120"><span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012, Fatal>: "<fileName>:<line\#> An INDEX or AUGMENTS clause is required only for SEQUENCE OBJECT-TYPES"**</span></span>
</dt> <dd>

<span data-ttu-id="98901-121">Errore semantico del modulo di chiamata macro del **tipo di oggetto** .</span><span class="sxs-lookup"><span data-stu-id="98901-121">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="98901-122">Una clausola INDEX deve essere presente solo in una definizione di tipo di oggetto la cui sintassi viene risolta in un tipo di sequenza.</span><span class="sxs-lookup"><span data-stu-id="98901-122">An INDEX clause must only be present in an OBJECT-TYPE definition whose SYNTAX resolves to a SEQUENCE type.</span></span>

<span data-ttu-id="98901-123">Questo errore può verificarsi durante la compilazione di un MIB SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="98901-123">This error can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

</dd> </dl>

## <a name="fatal-error-1013"></a><span data-ttu-id="98901-124">Errore irreversibile 1013</span><span class="sxs-lookup"><span data-stu-id="98901-124">Fatal Error 1013</span></span>

<dl> <dt>

<span data-ttu-id="98901-125"><span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013,> irreversibile: " <fileName><riga \#>: <identifier> deve essere risolto in un tipo di sequenza"**</span><span class="sxs-lookup"><span data-stu-id="98901-125"><span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013, Fatal>: "<fileName><line\#>: <identifier> should resolve to a SEQUENCE type"**</span></span>
</dt> <dd>

<span data-ttu-id="98901-126">Errore semantico del modulo di chiamata macro del **tipo di oggetto** .</span><span class="sxs-lookup"><span data-stu-id="98901-126">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="98901-127">Un tipo usato nel costrutto "SEQUENCE OF" deve essere risolto in un tipo di sequenza.</span><span class="sxs-lookup"><span data-stu-id="98901-127">A type used in the "SEQUENCE OF" construct must resolve to a SEQUENCE type.</span></span>

<span data-ttu-id="98901-128">Questo errore può verificarsi in SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="98901-128">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="warning-1014"></a><span data-ttu-id="98901-129">Avviso 1014</span><span class="sxs-lookup"><span data-stu-id="98901-129">Warning 1014</span></span>

<dl> <dt>

<span data-ttu-id="98901-130"><span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, avviso>: " <fileName> : <riga \#>: identificatore secondario del valore 0 non consigliato in OID"**</span><span class="sxs-lookup"><span data-stu-id="98901-130"><span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, Warning>: "<fileName>:<line\#>: Sub-identifier of value 0 not recommended in OIDs"**</span></span>
</dt> <dd>

<span data-ttu-id="98901-131">Avviso semantico del modulo di chiamata macro del **tipo di oggetto** .</span><span class="sxs-lookup"><span data-stu-id="98901-131">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="98901-132">È consigliabile che nessun oggetto in un MIB standard Internet usi un identificatore secondario pari a zero nell'identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="98901-132">It is recommended that no object in an Internet Standard MIB use a sub-identifier of zero in its OBJECT IDENTIFIER.</span></span>

<span data-ttu-id="98901-133">Questo avviso può verificarsi in SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="98901-133">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1015"></a><span data-ttu-id="98901-134">Errore irreversibile 1015</span><span class="sxs-lookup"><span data-stu-id="98901-134">Fatal Error 1015</span></span>

<dl> <dt>

<span data-ttu-id="98901-135"><span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015,> irreversibile: " <fileName> : <riga \#>: OBJECT-TYPEs <identifier> dal modulo <identifier> e <identifier> dal modulo <identifier> vengono assegnati gli stessi valori OID"**</span><span class="sxs-lookup"><span data-stu-id="98901-135"><span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015, Fatal>: "<fileName>:<line\#>: OBJECT-TYPEs <identifier> from module <identifier> and <identifier> from module <identifier> are assigned the same OID values"**</span></span>
</dt> <dd>

<span data-ttu-id="98901-136">Errore semantico del modulo di chiamata macro del **tipo di oggetto** .</span><span class="sxs-lookup"><span data-stu-id="98901-136">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="98901-137">Due richiami di **tipo di oggetto** (nello stesso o in moduli diversi) non devono essere assegnati allo stesso valore dell'identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="98901-137">Two **OBJECT-TYPE** invocations (in the same or different modules) must not be assigned the same Object Identifier value.</span></span>

<span data-ttu-id="98901-138">Questo errore può verificarsi in SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="98901-138">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1016"></a><span data-ttu-id="98901-139">Errore irreversibile 1016</span><span class="sxs-lookup"><span data-stu-id="98901-139">Fatal Error 1016</span></span>

<dl> <dt>

<span data-ttu-id="98901-140"><span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016,> irreversibile: " <fileName> : <riga \#>: il valore nella clausola DEFVAL non corrisponde al tipo nella clausola Syntax"**</span><span class="sxs-lookup"><span data-stu-id="98901-140"><span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016, Fatal>: "<fileName>:<line\#>: Value in the DEFVAL clause does not match the type in the SYNTAX clause"**</span></span>
</dt> <dd>

<span data-ttu-id="98901-141">Errore semantico del modulo di chiamata macro del **tipo di oggetto** .</span><span class="sxs-lookup"><span data-stu-id="98901-141">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="98901-142">Un valore in una clausola DEFVAL deve essere un valore del tipo indicato nella clausola SYNTAX.</span><span class="sxs-lookup"><span data-stu-id="98901-142">A value in a DEFVAL clause must be a value of the type mentioned in the SYNTAX clause.</span></span>

<span data-ttu-id="98901-143">Questo errore può verificarsi in SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="98901-143">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1018"></a><span data-ttu-id="98901-144">Errore irreversibile 1018</span><span class="sxs-lookup"><span data-stu-id="98901-144">Fatal Error 1018</span></span>

<dl> <dt>

<span data-ttu-id="98901-145"><span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018,> irreversibile: " <fileName><riga \#>: <symbol> nella clausola Enterprise di trap-type non viene risolto in un valore OID"**</span><span class="sxs-lookup"><span data-stu-id="98901-145"><span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018, Fatal>: "<fileName><line\#>: <symbol> in ENTERPRISE clause of TRAP-TYPE does not resolve to an OID value"**</span></span>
</dt> <dd>

<span data-ttu-id="98901-146">Chiamata della macro di **tipo trap** , errore semantico del modulo specifico di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="98901-146">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="98901-147">Il simbolo usato nella clausola ENTERPRISE di una chiamata della macro di **tipo trap** deve risolversi in un valore dell'identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="98901-147">The symbol used in the ENTERPRISE clause of a **TRAP-TYPE** macro invocation must resolve to an Object Identifier value.</span></span>

</dd> </dl>

## <a name="fatal-error-1020"></a><span data-ttu-id="98901-148">Errore irreversibile 1020</span><span class="sxs-lookup"><span data-stu-id="98901-148">Fatal Error 1020</span></span>

<dl> <dt>

<span data-ttu-id="98901-149"><span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020,> irreversibile: " <fileName><riga \#>: il valore assegnato a trap-type non <identifier> viene risolto in un numero intero positivo"**</span><span class="sxs-lookup"><span data-stu-id="98901-149"><span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020, Fatal>: "<fileName><line\#>: Value assigned to TRAP-TYPE <identifier> does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="98901-150">Chiamata della macro di **tipo trap** , errore semantico del modulo specifico di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="98901-150">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="98901-151">Un simbolo utilizzato per specificare il valore trap non viene risolto in un numero intero positivo.</span><span class="sxs-lookup"><span data-stu-id="98901-151">A symbol used in specifying the trap value does not resolve to a positive integer.</span></span>

</dd> </dl>

 

 



