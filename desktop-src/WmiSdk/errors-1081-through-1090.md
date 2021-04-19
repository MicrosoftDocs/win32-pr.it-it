---
description: Descrive gli errori del provider SNMP WMI da 1081 a 1090.
ms.assetid: aa953c53-a61f-48e4-9234-acc450b9bdf1
ms.tgt_platform: multiple
title: Errori da 1081 a 1090
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a80399ef61bce644813447559a76bf9710873be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310363"
---
# <a name="errors-1081-through-1090"></a><span data-ttu-id="ad493-103">Errori da 1081 a 1090</span><span class="sxs-lookup"><span data-stu-id="ad493-103">Errors 1081 through 1090</span></span>

<span data-ttu-id="ad493-104">Descrive gli errori del provider SNMP WMI da 1081 a 1090.</span><span class="sxs-lookup"><span data-stu-id="ad493-104">Describes WMI SNMP provider errors 1081 through 1090.</span></span>

[<span data-ttu-id="ad493-105">Errore irreversibile 1081</span><span class="sxs-lookup"><span data-stu-id="ad493-105">Fatal Error 1081</span></span>](#fatal-error-1081)

[<span data-ttu-id="ad493-106">Errore irreversibile 1082</span><span class="sxs-lookup"><span data-stu-id="ad493-106">Fatal Error 1082</span></span>](#fatal-error-1082)

[<span data-ttu-id="ad493-107">Errore irreversibile 1084</span><span class="sxs-lookup"><span data-stu-id="ad493-107">Fatal Error 1084</span></span>](#fatal-error-1084)

[<span data-ttu-id="ad493-108">Avviso 1085</span><span class="sxs-lookup"><span data-stu-id="ad493-108">Warning 1085</span></span>](#warning-1085)

[<span data-ttu-id="ad493-109">Avviso 1086</span><span class="sxs-lookup"><span data-stu-id="ad493-109">Warning 1086</span></span>](#warning-1086)

[<span data-ttu-id="ad493-110">Errore irreversibile 1087</span><span class="sxs-lookup"><span data-stu-id="ad493-110">Fatal Error 1087</span></span>](#fatal-error-1087)

[<span data-ttu-id="ad493-111">Errore irreversibile 1089</span><span class="sxs-lookup"><span data-stu-id="ad493-111">Fatal Error 1089</span></span>](#fatal-error-1089)

[<span data-ttu-id="ad493-112">Errore irreversibile 1090</span><span class="sxs-lookup"><span data-stu-id="ad493-112">Fatal Error 1090</span></span>](#fatal-error-1090)

## <a name="fatal-error-1081"></a><span data-ttu-id="ad493-113">Errore irreversibile 1081</span><span class="sxs-lookup"><span data-stu-id="ad493-113">Fatal Error 1081</span></span>

<dl> <dt>

<span data-ttu-id="ad493-114"><span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081,> irreversibile: " <fileName> riga \#>: simbolo <identifier> non presente nel modulo importato <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="ad493-114"><span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081, Fatal>: "<fileName>line\#>: Symbol <identifier> not present in imported module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="ad493-115">Errore semantico del modulo nel riferimento incrociato, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ad493-115">Module semantic error in cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="ad493-116">Un simbolo importato da un modulo non viene risolto in alcun elemento del modulo.</span><span class="sxs-lookup"><span data-stu-id="ad493-116">A symbol imported from a module does not resolve to anything in that module.</span></span> <span data-ttu-id="ad493-117">Questo errore si verifica se si fa effettivamente riferimento a tale simbolo nel MIB.</span><span class="sxs-lookup"><span data-stu-id="ad493-117">If that symbol is actually referenced in the MIB, this error occurs.</span></span>

</dd> </dl>

## <a name="fatal-error-1082"></a><span data-ttu-id="ad493-118">Errore irreversibile 1082</span><span class="sxs-lookup"><span data-stu-id="ad493-118">Fatal Error 1082</span></span>

<dl> <dt>

<span data-ttu-id="ad493-119"><span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082,> irreversibile: " <fileName> : <riga \#>: clausola di stato non valida <clause> "**</span><span class="sxs-lookup"><span data-stu-id="ad493-119"><span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082, Fatal>: "<fileName>:<line\#>: Invalid STATUS clause <clause>"**</span></span>
</dt> <dd>

<span data-ttu-id="ad493-120">Chiamata macro **oggetto-identità** , errore semantico del modulo specifico di SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ad493-120">**OBJECT-IDENTITY** macro invocation, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="ad493-121">La clausola STATUS della chiamata dell'identità di un **oggetto** deve essere "Current", "deprecated" o "obsolete".</span><span class="sxs-lookup"><span data-stu-id="ad493-121">The STATUS clause of an **OBJECT-IDENTITY** invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="fatal-error-1084"></a><span data-ttu-id="ad493-122">Errore irreversibile 1084</span><span class="sxs-lookup"><span data-stu-id="ad493-122">Fatal Error 1084</span></span>

<dl> <dt>

<span data-ttu-id="ad493-123"><span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084,> irreversibile: "fileName><line \#>: module-Identity required after the IMports section for all SNMPv2 modules"**</span><span class="sxs-lookup"><span data-stu-id="ad493-123"><span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084, Fatal>: "fileName><line\#>: MODULE-IDENTITY required after the IMPORTS section for all SNMPv2 modules"**</span></span>
</dt> <dd>

<span data-ttu-id="ad493-124">Chiamata macro **modulo-identità** , errore semantico del modulo specifico di SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ad493-124">**MODULE-IDENTITY** macro invocation, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="ad493-125">Deve essere presente una sola chiamata di **identità del modulo** in un SNMPv2c MIB, immediatamente dopo la sezione Imports.</span><span class="sxs-lookup"><span data-stu-id="ad493-125">There must be one and only one **MODULE-IDENTITY** invocation in an SNMPv2C MIB, immediately after the IMPORTS section.</span></span>

</dd> </dl>

## <a name="warning-1085"></a><span data-ttu-id="ad493-126">Avviso 1085</span><span class="sxs-lookup"><span data-stu-id="ad493-126">Warning 1085</span></span>

<dl> <dt>

<span data-ttu-id="ad493-127"><span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, avviso>: " <fileName><riga \#>: non sono stati trovati gruppi nel modulo <name> . Non è stato possibile fabbricare l'identità del modulo. Il tentativo di caricare il modulo in archivio SMIR avrà esito negativo "**</span><span class="sxs-lookup"><span data-stu-id="ad493-127"><span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, Warning>: "<fileName><line\#>: No groups found in module <name>. Could not fabricate MODULE-IDENTITY. Attempt to load the module into the SMIR will fail"**</span></span>
</dt> <dd>

<span data-ttu-id="ad493-128">Avviso specifico del modulo SNMPv1 semantico.</span><span class="sxs-lookup"><span data-stu-id="ad493-128">Module semantic SNMPv1-specific warning.</span></span> <span data-ttu-id="ad493-129">Questo errore viene generato se non vengono trovati gruppi di oggetti in un modulo.</span><span class="sxs-lookup"><span data-stu-id="ad493-129">This error is generated if no object groups are found in a module.</span></span>

</dd> </dl>

## <a name="warning-1086"></a><span data-ttu-id="ad493-130">Avviso 1086</span><span class="sxs-lookup"><span data-stu-id="ad493-130">Warning 1086</span></span>

<dl> <dt>

<span data-ttu-id="ad493-131"><span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, avviso>: " <fileName><riga \#>: non sono stati trovati gruppi nel modulo <name> "**</span><span class="sxs-lookup"><span data-stu-id="ad493-131"><span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, Warning>: "<fileName><line\#>: No groups found in module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="ad493-132">Avviso specifico del modulo SNMPv1 semantico.</span><span class="sxs-lookup"><span data-stu-id="ad493-132">Module semantic SNMPv1-specific warning.</span></span> <span data-ttu-id="ad493-133">Questo errore viene generato se non vengono trovati gruppi di oggetti in un modulo.</span><span class="sxs-lookup"><span data-stu-id="ad493-133">This error is generated if no object groups are found in a module.</span></span>

</dd> </dl>

## <a name="fatal-error-1087"></a><span data-ttu-id="ad493-134">Errore irreversibile 1087</span><span class="sxs-lookup"><span data-stu-id="ad493-134">Fatal Error 1087</span></span>

<dl> <dt>

<span data-ttu-id="ad493-135"><span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087.> irreversibile: " <fileName><linea \#>: clausola di stato non valida <clause> per una macro della convenzione testuale"**</span><span class="sxs-lookup"><span data-stu-id="ad493-135"><span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087. Fatal>: "<fileName><line\#>: Invalid STATUS clause <clause> for a TEXTUAL-CONVENTION macro"**</span></span>
</dt> <dd>

<span data-ttu-id="ad493-136">Assegnazione del tipo, errore semantico del modulo specifico di SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ad493-136">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="ad493-137">La clausola status di una chiamata della macro della **convenzione testuale** deve essere "Current", "deprecated" o "obsolete".</span><span class="sxs-lookup"><span data-stu-id="ad493-137">The status clause of a **TEXTUAL-CONVENTION** macro invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="fatal-error-1089"></a><span data-ttu-id="ad493-138">Errore irreversibile 1089</span><span class="sxs-lookup"><span data-stu-id="ad493-138">Fatal Error 1089</span></span>

<dl> <dt>

<span data-ttu-id="ad493-139"><span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089,> irreversibile: " <fileName> : <linea \#>: il simbolo <identifier> nella clausola augments non viene risolto in un oggetto di riga, tipo"**</span><span class="sxs-lookup"><span data-stu-id="ad493-139"><span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, Fatal>: "<fileName>:<line\#>: Symbol <identifier> in AUGMENTS clause does not resolve to a row OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="ad493-140">Errore di semantica del modulo specifico del **tipo di oggetto** SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ad493-140">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="ad493-141">Se è presente una clausola AUGMENTs, l'identificatore nella clausola AUGMENTs deve essere risolto in un tipo di oggetto Table.</span><span class="sxs-lookup"><span data-stu-id="ad493-141">If an AUGMENTS clause is present, then the identifier in the AUGMENTS clause must resolve to a table OBJECT-TYPE.</span></span>

</dd> </dl>

## <a name="fatal-error-1090"></a><span data-ttu-id="ad493-142">Errore irreversibile 1090</span><span class="sxs-lookup"><span data-stu-id="ad493-142">Fatal Error 1090</span></span>

<dl> <dt>

<span data-ttu-id="ad493-143"><span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090,> irreversibile: " <fileName> : <\# la clausola implicita> è utile solo per l'ultimo oggetto index"**</span><span class="sxs-lookup"><span data-stu-id="ad493-143"><span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090, Fatal>: "<fileName>:<line\#> IMPLIED clause is useful only for the last INDEX object"**</span></span>
</dt> <dd>

<span data-ttu-id="ad493-144">Errore di semantica del modulo specifico del **tipo di oggetto** SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="ad493-144">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="ad493-145">La clausola implicita può essere associata solo all'ultimo oggetto nella clausola INDEX.</span><span class="sxs-lookup"><span data-stu-id="ad493-145">The IMPLIED clause can be associated only with the last object in the INDEX clause.</span></span>

</dd> </dl>

 

 



