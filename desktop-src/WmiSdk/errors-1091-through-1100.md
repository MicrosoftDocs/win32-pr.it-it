---
description: Descrive gli errori del provider SNMP WMI da 1091 a 1100.
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: Errori da 1091 a 1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf582a3df41fbc7c329f5a993555a2d76145ded0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319298"
---
# <a name="errors-1091-through-1100"></a><span data-ttu-id="13a13-103">Errori da 1091 a 1100</span><span class="sxs-lookup"><span data-stu-id="13a13-103">Errors 1091 through 1100</span></span>

<span data-ttu-id="13a13-104">Descrive gli errori del provider SNMP WMI da 1091 a 1100.</span><span class="sxs-lookup"><span data-stu-id="13a13-104">Describes WMI SNMP provider errors 1091 through 1100.</span></span>

[<span data-ttu-id="13a13-105">Avviso 1091</span><span class="sxs-lookup"><span data-stu-id="13a13-105">Warning 1091</span></span>](#warning-1091)

[<span data-ttu-id="13a13-106">Errore irreversibile 1092</span><span class="sxs-lookup"><span data-stu-id="13a13-106">Fatal Error 1092</span></span>](#fatal-error-1092)

[<span data-ttu-id="13a13-107">Errore irreversibile 1093</span><span class="sxs-lookup"><span data-stu-id="13a13-107">Fatal Error 1093</span></span>](#fatal-error-1093)

[<span data-ttu-id="13a13-108">Errore irreversibile 1094</span><span class="sxs-lookup"><span data-stu-id="13a13-108">Fatal Error 1094</span></span>](#fatal-error-1094)

[<span data-ttu-id="13a13-109">Errore irreversibile 1095</span><span class="sxs-lookup"><span data-stu-id="13a13-109">Fatal Error 1095</span></span>](#fatal-error-1095)

[<span data-ttu-id="13a13-110">Errore irreversibile 1097</span><span class="sxs-lookup"><span data-stu-id="13a13-110">Fatal Error 1097</span></span>](#fatal-error-1097)

[<span data-ttu-id="13a13-111">Errore irreversibile 1098</span><span class="sxs-lookup"><span data-stu-id="13a13-111">Fatal Error 1098</span></span>](#fatal-error-1098)

[<span data-ttu-id="13a13-112">Errore irreversibile 1099</span><span class="sxs-lookup"><span data-stu-id="13a13-112">Fatal Error 1099</span></span>](#fatal-error-1099)

## <a name="warning-1091"></a><span data-ttu-id="13a13-113">Avviso 1091</span><span class="sxs-lookup"><span data-stu-id="13a13-113">Warning 1091</span></span>

<dl> <dt>

<span data-ttu-id="13a13-114"><span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, avviso>: " <fileName> : \# la clausola <della riga implicita> non è consentita per gli oggetti a dimensione fissa"**</span><span class="sxs-lookup"><span data-stu-id="13a13-114"><span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, Warning>: "<fileName>:<line\#> IMPLIED clause is not allowed for fixed size objects"**</span></span>
</dt> <dd>

<span data-ttu-id="13a13-115">Avviso di semantica del modulo specifico per la chiamata di macro di **tipo oggetto** SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="13a13-115">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic warning.</span></span> <span data-ttu-id="13a13-116">La parola chiave implicita può essere presente solo per un oggetto con sintassi a lunghezza variabile, ad esempio un identificatore di oggetto o una stringa di OTTETti a lunghezza variabile, nella clausola INDEX.</span><span class="sxs-lookup"><span data-stu-id="13a13-116">The IMPLIED keyword can only be present for an object having a variable-length syntax, such as an OBJECT IDENTIFIER or variable-length OCTET STRING, in the INDEX clause.</span></span>

</dd> </dl>

## <a name="fatal-error-1092"></a><span data-ttu-id="13a13-117">Errore irreversibile 1092</span><span class="sxs-lookup"><span data-stu-id="13a13-117">Fatal Error 1092</span></span>

<dl> <dt>

<span data-ttu-id="13a13-118"><span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092,> irreversibile: " <fileName> : <linea \#> clausola implicita non consentita per oggetti potenzialmente di lunghezza zero"**</span><span class="sxs-lookup"><span data-stu-id="13a13-118"><span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, Fatal>: "<fileName>:<line\#> IMPLIED clause not allowed for potentially zero-length objects"**</span></span>
</dt> <dd>

<span data-ttu-id="13a13-119">Errore di semantica del modulo specifico del **tipo di oggetto** SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="13a13-119">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="13a13-120">Impossibile utilizzare la clausola implicita su un oggetto a lunghezza variabile se tale oggetto può avere una lunghezza pari a zero.</span><span class="sxs-lookup"><span data-stu-id="13a13-120">The IMPLIED clause cannot be used on a variable-length object if that object can have a zero length.</span></span>

</dd> </dl>

## <a name="fatal-error-1093"></a><span data-ttu-id="13a13-121">Errore irreversibile 1093</span><span class="sxs-lookup"><span data-stu-id="13a13-121">Fatal Error 1093</span></span>

<dl> <dt>

<span data-ttu-id="13a13-122"><span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093.> irreversibile: " <fileName><linea \#>: solo il tipo" Integer "può essere enumerato in base alla SMI SMI"**</span><span class="sxs-lookup"><span data-stu-id="13a13-122"><span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093. Fatal>: "<fileName><line\#>: Only the type "INTEGER" can be enumerated according to the V1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="13a13-123">Assegnazione del tipo, errore semantico del modulo specifico di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="13a13-123">Type assignment, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="13a13-124">Un'enumerazione MIB SNMPv1 può usare solo il tipo INTEGER.</span><span class="sxs-lookup"><span data-stu-id="13a13-124">An SNMPv1 MIB enumeration can use only the type INTEGER.</span></span>

</dd> </dl>

## <a name="fatal-error-1094"></a><span data-ttu-id="13a13-125">Errore irreversibile 1094</span><span class="sxs-lookup"><span data-stu-id="13a13-125">Fatal Error 1094</span></span>

<dl> <dt>

<span data-ttu-id="13a13-126"><span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094.> irreversibile: " <fileName><linea \#>: il tipo usato nell'enumerazione non viene risolto in uno dei tipi consentiti"**</span><span class="sxs-lookup"><span data-stu-id="13a13-126"><span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094. Fatal>: "<fileName><line\#>: The type used in the enumeration does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="13a13-127">Assegnazione del tipo, errore semantico del modulo specifico di SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="13a13-127">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="13a13-128">Il tipo utilizzato in un'enumerazione deve essere di tipo INTEGER o equivalente oppure un'altra enumerazione.</span><span class="sxs-lookup"><span data-stu-id="13a13-128">The type used in an enumeration must be INTEGER or an equivalent type, or another enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1095"></a><span data-ttu-id="13a13-129">Errore irreversibile 1095</span><span class="sxs-lookup"><span data-stu-id="13a13-129">Fatal Error 1095</span></span>

<dl> <dt>

<span data-ttu-id="13a13-130"><span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095.> irreversibile: " <fileName><line \#>: il membro di enumerazione non è un membro dell'enumerazione padre"**</span><span class="sxs-lookup"><span data-stu-id="13a13-130"><span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095. Fatal>: "<fileName><line\#>: Enumeration member is not a member of the parent enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="13a13-131">Assegnazione del tipo, errore semantico del modulo specifico di SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="13a13-131">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="13a13-132">Se viene utilizzata un'altra enumerazione, il set di elementi deve essere un subset del set di elementi dell'enumerazione padre.</span><span class="sxs-lookup"><span data-stu-id="13a13-132">If another enumeration is used, its set of items must be a subset of the parent enumeration's set of items.</span></span>

</dd> </dl>

## <a name="fatal-error-1097"></a><span data-ttu-id="13a13-133">Errore irreversibile 1097</span><span class="sxs-lookup"><span data-stu-id="13a13-133">Fatal Error 1097</span></span>

<dl> <dt>

<span data-ttu-id="13a13-134"><span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097,> irreversibile: " <fileName><riga \#>: <name> l'identificatore non viene risolto in un valore integer"**</span><span class="sxs-lookup"><span data-stu-id="13a13-134"><span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097, Fatal>: "<fileName><line\#>: identifier <name> does not resolve to an integer value"**</span></span>
</dt> <dd>

<span data-ttu-id="13a13-135">Assegnazione del tipo, errore semantico del modulo specifico di SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="13a13-135">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="13a13-136">I valori nel tipo BITS devono essere valori integer.</span><span class="sxs-lookup"><span data-stu-id="13a13-136">The values in the BITS type must be integer values.</span></span>

</dd> </dl>

## <a name="fatal-error-1098"></a><span data-ttu-id="13a13-137">Errore irreversibile 1098</span><span class="sxs-lookup"><span data-stu-id="13a13-137">Fatal Error 1098</span></span>

<dl> <dt>

<span data-ttu-id="13a13-138"><span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098,> irreversibile: " <fileName><riga \#>: valore duplicato <value> nel costrutto bits"**</span><span class="sxs-lookup"><span data-stu-id="13a13-138"><span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098, Fatal>: "<fileName><line\#>: Duplicate value <value> in BITS construct"**</span></span>
</dt> <dd>

<span data-ttu-id="13a13-139">Assegnazione del tipo, errore semantico del modulo specifico di SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="13a13-139">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="13a13-140">Non devono essere presenti nomi e valori duplicati in un costrutto BITS.</span><span class="sxs-lookup"><span data-stu-id="13a13-140">There must be no duplicate names and values in a BITS construct.</span></span> <span data-ttu-id="13a13-141">Il <riga \#> parametro è la posizione della ricorrenza del nome/valore.</span><span class="sxs-lookup"><span data-stu-id="13a13-141">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1099"></a><span data-ttu-id="13a13-142">Errore irreversibile 1099</span><span class="sxs-lookup"><span data-stu-id="13a13-142">Fatal Error 1099</span></span>

<dl> <dt>

<span data-ttu-id="13a13-143"><span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099,> irreversibile: " <fileName><riga \#>: nome duplicato <identifier> nel costrutto bits"**</span><span class="sxs-lookup"><span data-stu-id="13a13-143"><span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in BITS construct"**</span></span>
</dt> <dd>

<span data-ttu-id="13a13-144">Assegnazione del tipo, errore semantico del modulo specifico di SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="13a13-144">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="13a13-145">Non devono essere presenti nomi e valori duplicati in un costrutto BITS.</span><span class="sxs-lookup"><span data-stu-id="13a13-145">There must be no duplicate names and values in a BITS construct.</span></span> <span data-ttu-id="13a13-146">Il <riga \#> parametro è la posizione della ricorrenza del nome/valore.</span><span class="sxs-lookup"><span data-stu-id="13a13-146">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

 

 



