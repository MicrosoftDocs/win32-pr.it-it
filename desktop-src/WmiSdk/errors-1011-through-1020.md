---
description: Descrive gli errori del provider WMI SNMP da 1011 a 1020.
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: Errori da 1011 a 1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49642dd17180b32a683ec7937553dbe60c60584e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886963"
---
# <a name="errors-1011-through-1020"></a>Errori da 1011 a 1020

Descrive gli errori del provider WMI SNMP da 1011 a 1020.

[Errore irreversibile 1011](#fatal-error-1011)

[Errore irreversibile 1012](#fatal-error-1012)

[Errore irreversibile 1013](#fatal-error-1013)

[Avviso 1014](#warning-1014)

[Errore irreversibile 1015](#fatal-error-1015)

[Errore irreversibile 1016](#fatal-error-1016)

[Errore irreversibile 1018](#fatal-error-1018)

[Errore irreversibile 1020](#fatal-error-1020)

## <a name="fatal-error-1011"></a>Errore irreversibile 1011

<dl> <dt>

<span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011, fatal>: " &lt; fileName &gt; :<line \#> the SYNTAX of member &lt; identifier of &gt; SEQUENCE, identifier , &lt; &gt; differs from the SYNTAX clause of the OBJECT-TYPE"**
</dt> <dd>

Errore semantico del modulo di chiamata di macro **OBJECT-TYPE.** Un elemento di sequence deve essere uguale al tipo nella clausola SYNTAX della definizione OBJECT-TYPE. Il <riga \#> parametro è la riga della clausola SYNTAX della definizione OBJECT-TYPE.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1012"></a>Errore irreversibile 1012

<dl> <dt>

<span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012, errore irreversibile>: " fileName :<line> Una clausola INDEX o AUGMENTS è necessaria solo &lt; &gt; per SEQUENCE \# OBJECT-TYPES"**
</dt> <dd>

Errore semantico del modulo di chiamata di macro **OBJECT-TYPE.** Una clausola INDEX deve essere presente solo in una definizione OBJECT-TYPE la cui sintassi viene risolta in un tipo SEQUENCE.

Questo errore può verificarsi durante la compilazione di un MIB SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1013"></a>Errore irreversibile 1013

<dl> <dt>

<span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013, errore irreversibile>: " fileName<&lt; &gt; riga \#>: identificatore deve &lt; &gt; risolversi in un tipo SEQUENCE"**
</dt> <dd>

Errore semantico del modulo di chiamata di macro **OBJECT-TYPE.** Un tipo usato nel costrutto "SEQUENCE OF" deve essere risolto in un tipo SEQUENCE.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="warning-1014"></a>Avviso 1014

<dl> <dt>

<span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, avviso>: " fileName :<riga>: Identificatore secondario del valore 0 non consigliato &lt; &gt; negli \# OID"**
</dt> <dd>

Avviso semantico del modulo di chiamata di macro **OBJECT-TYPE.** È consigliabile che nessun oggetto in un MIB Standard Internet usi un identificatore secondario pari a zero nel relativo IDENTIFICATORE DI OGGETTO.

Questo avviso può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1015"></a>Errore irreversibile 1015

<dl> <dt>

<span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015, fatal>: " &lt; fileName &gt; :<line \#>: OBJECT-TYPEs identifier from &lt; &gt; module identifier and identifier from module identifier are &lt; assigned the same &gt; &lt; &gt; &lt; &gt; OID values"**
</dt> <dd>

Errore semantico del modulo di chiamata di macro **OBJECT-TYPE.** A **due chiamate OBJECT-TYPE** (nello stesso modulo o in moduli diversi) non deve essere assegnato lo stesso valore dell'identificatore di oggetto.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1016"></a>Errore irreversibile 1016

<dl> <dt>

<span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016, errore irreversibile>: " &lt; fileName :<riga>: Il valore nella clausola DEFVAL non corrisponde al tipo nella clausola &gt; \# SYNTAX"**
</dt> <dd>

Errore semantico del modulo di chiamata di macro **OBJECT-TYPE.** Un valore in una clausola DEFVAL deve essere un valore del tipo indicato nella clausola SYNTAX.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1018"></a>Errore irreversibile 1018

<dl> <dt>

<span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018, errore irreversibile>: " fileName<riga>: il simbolo nella clausola ENTERPRISE di TRAP-TYPE non viene risolto in un &lt; &gt; valore \# &lt; &gt; OID"**
</dt> <dd>

Chiamata di macro **TRAP-TYPE,** errore semantico del modulo specifico di SNMPv1. Il simbolo utilizzato nella clausola ENTERPRISE di una chiamata di macro **TRAP-TYPE** deve essere risolto in un valore di identificatore di oggetto.

</dd> </dl>

## <a name="fatal-error-1020"></a>Errore irreversibile 1020

<dl> <dt>

<span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020, errore irreversibile>: " fileName<riga>: Il valore assegnato &lt; &gt; all'identificatore \# TRAP-TYPE non viene risolto in un numero intero &lt; &gt; positivo"**
</dt> <dd>

Chiamata di macro **TRAP-TYPE,** errore semantico del modulo specifico di SNMPv1. Un simbolo utilizzato per specificare il valore trap non viene risolto in un numero intero positivo.

</dd> </dl>

 

 



