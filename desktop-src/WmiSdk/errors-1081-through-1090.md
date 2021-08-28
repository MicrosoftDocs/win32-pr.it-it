---
description: Descrive gli errori del provider SNMP WMI da 1081 a 1090.
ms.assetid: aa953c53-a61f-48e4-9234-acc450b9bdf1
ms.tgt_platform: multiple
title: Errori da 1081 a 1090
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c1ce7b1a8c575067fe2231108e0d314af2f8dc8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879708"
---
# <a name="errors-1081-through-1090"></a>Errori da 1081 a 1090

Descrive gli errori del provider SNMP WMI da 1081 a 1090.

[Errore irreversibile 1081](#fatal-error-1081)

[Errore irreversibile 1082](#fatal-error-1082)

[Errore irreversibile 1084](#fatal-error-1084)

[Avviso 1085](#warning-1085)

[Avviso 1086](#warning-1086)

[Errore irreversibile 1087](#fatal-error-1087)

[Errore irreversibile 1089](#fatal-error-1089)

[Errore irreversibile 1090](#fatal-error-1090)

## <a name="fatal-error-1081"></a>Errore irreversibile 1081

<dl> <dt>

<span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081, Fatal>: " &lt; fileName &gt; line>: Identificatore di simbolo non presente \# &lt; &gt; nell'identificatore del modulo &lt; importato &gt; "**
</dt> <dd>

Errore semantico del modulo nel riferimento incrociato, specifico di SNMPv1 o SNMPv2C. Un simbolo importato da un modulo non viene risolto in alcun elemento in tale modulo. Se si fa effettivamente riferimento a tale simbolo nel MIB, si verifica questo errore.

</dd> </dl>

## <a name="fatal-error-1082"></a>Errore irreversibile 1082

<dl> <dt>

<span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082, Fatal>: " &lt; fileName &gt; :<line \#>: Clausola STATUS &lt; non valida &gt; "**
</dt> <dd>

Chiamata alla macro **OBJECT-IDENTITY,** errore semantico del modulo specifico di SNMPv2C. La clausola STATUS di una chiamata **OBJECT-IDENTITY** deve essere "current", "deprecata" o "obsoleta".

</dd> </dl>

## <a name="fatal-error-1084"></a>Errore irreversibile 1084

<dl> <dt>

<span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084, Fatal>: "fileName><line>: MODULE-IDENTITY obbligatorio dopo la sezione IMPORTS per tutti i moduli \# SNMPv2"**
</dt> <dd>

Chiamata di macro **MODULE-IDENTITY,** errore semantico del modulo specifico di SNMPv2C. Deve essere presente una sola chiamata **MODULE-IDENTITY** in un MIB SNMPv2C, immediatamente dopo la sezione IMPORTS.

</dd> </dl>

## <a name="warning-1085"></a>Avviso 1085

<dl> <dt>

<span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, Avviso>: " fileName<&lt; riga>: Nessun gruppo &gt; trovato nel nome del modulo \# &lt; &gt; . Impossibile creare MODULE-IDENTITY. Il tentativo di caricare il modulo in SMIR avrà esito negativo"**
</dt> <dd>

Avviso semantico del modulo specifico di SNMPv1. Questo errore viene generato se non vengono trovati gruppi di oggetti in un modulo.

</dd> </dl>

## <a name="warning-1086"></a>Avviso 1086

<dl> <dt>

<span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, Avviso>: " &lt; fileName &gt;<riga \#>: Nessun &lt; gruppo trovato nel nome del modulo &gt; "**
</dt> <dd>

Avviso semantico del modulo specifico di SNMPv1. Questo errore viene generato se non vengono trovati gruppi di oggetti in un modulo.

</dd> </dl>

## <a name="fatal-error-1087"></a>Errore irreversibile 1087

<dl> <dt>

<span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087. Errore>: &lt; "fileName &gt;<riga \#>: clausola STATUS non valida per una macro &lt; &gt; TEXTUAL-CONVENTION"**
</dt> <dd>

Assegnazione di tipo, errore semantico del modulo specifico di SNMPv2C. La clausola status di una chiamata di macro **TEXTUAL-CONVENTION** deve essere "current", "deprecato" o "obsoleto".

</dd> </dl>

## <a name="fatal-error-1089"></a>Errore irreversibile 1089

<dl> <dt>

<span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, Errore irreversibile>: " fileName :<line>: L'identificatore di simbolo nella clausola AUGMENTS non viene risolto in &lt; &gt; una riga \# &lt; &gt; OBJECT-TYPE"**
</dt> <dd>

Errore semantico del modulo specifico della chiamata di macro **OBJECT-TYPE** SNMPv2C. Se è presente una clausola AUGMENTS, l'identificatore nella clausola AUGMENTS deve essere risolto in una tabella OBJECT-TYPE.

</dd> </dl>

## <a name="fatal-error-1090"></a>Errore irreversibile 1090

<dl> <dt>

<span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090, Fatal>: " &lt; fileName :<line> IMPLIED clause is useful only for the last INDEX object" (Errore irreversibile>: " fileName :<riga> clausola IMPLIED è utile solo per &gt; \# l'ultimo oggetto INDEX"**
</dt> <dd>

Errore semantico del modulo specifico della chiamata di macro **OBJECT-TYPE** SNMPv2C. La clausola IMPLIED può essere associata solo all'ultimo oggetto nella clausola INDEX.

</dd> </dl>

 

 



