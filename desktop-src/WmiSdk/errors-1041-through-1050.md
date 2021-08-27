---
description: Descrive gli errori del provider WMI SNMP da 1041 a 1050.
ms.assetid: e7e70fb3-12c6-40b1-91a4-c550e8210c09
ms.tgt_platform: multiple
title: Errori da 1041 a 1050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1a245f8e4da4556dd05a9827255ca2e7f168ab
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879855"
---
# <a name="errors-1041-through-1050"></a>Errori da 1041 a 1050

Descrive gli errori del provider WMI SNMP da 1041 a 1050.

[Errore irreversibile 1041](#fatal-error-1041)

[Errore irreversibile 1042](#fatal-error-1042)

[Avviso 1043](#warning-1043)

[Errore irreversibile 1044](#fatal-error-1044)

[Avviso 1045](#warning-1045)

[Avviso 1046](#warning-1046)

[Avviso 1047](#warning-1047)

[Avviso 1048](#warning-1048)

[Errore irreversibile 1049](#fatal-error-1049)

## <a name="fatal-error-1041"></a>Errore irreversibile 1041

<dl> <dt>

<span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041, errore irreversibile>: " fileName<riga>: l'identificatore nella specifica dell'intervallo non viene risolto in &lt; &gt; un valore \# &lt; &gt; integrale"**
</dt> <dd>

Errore semantico del modulo nella specifica dell'intervallo o della dimensione, specifico di SNMPv1 o SNMPv2C. Il simbolo usato in una specifica SIZE deve essere risolto in OCTET STRING o Opaque. Qualsiasi valore utilizzato per specificare un intervallo deve essere un numero intero.

</dd> </dl>

## <a name="fatal-error-1042"></a>Errore irreversibile 1042

<dl> <dt>

<span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042, errore irreversibile>: " fileName<riga>: Limite superiore della specifica dell'intervallo è minore del limite &lt; &gt; \# inferiore"**
</dt> <dd>

Errore semantico del modulo nella specifica dell'intervallo o della dimensione, specifico di SNMPv1 o SNMPv2C. Il simbolo usato in una specifica SIZE deve essere risolto in OCTET STRING o Opaque. Il limite inferiore di un intervallo o di una specifica SIZE non deve essere maggiore del limite superiore.

</dd> </dl>

## <a name="warning-1043"></a>Avviso 1043

<dl> <dt>

<span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, avviso>: " &lt; fileName &gt; :<riga \#>: OBJECT-TYPE con SINTASSI "SEQUENCE", deve avere una clausola ACCESS "not-accessible"**
</dt> <dd>

Avviso semantico del modulo di chiamata di macro **OBJECT-TYPE.** Una tabella o una riga concettuale (rispettivamente i tipi di oggetto SEQUENCE OF o SEQUENCE) deve essere "non accessibile".

Questo avviso può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1044"></a>Errore irreversibile 1044

<dl> <dt>

<span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044, Errore irreversibile>: " &lt; fileName &gt;<riga \#>: Ridefinizione dell'identificatore &lt; di simbolo &gt; "**
</dt> <dd>

Errore semantico del modulo, specifico di SNMPv1 o SNMPv2C. La ridefinizione di descrittori di oggetti, chiamate di macro e tipi ASN.1 causa un errore.

</dd> </dl>

## <a name="warning-1045"></a>Avviso 1045

<dl> <dt>

<span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, warning>: " &lt; fileName &gt;<lineReference to standard symbolName assumed to be for the definition as &lt; in &gt; &lt; moduleName &gt; . Usare le notazioni "module.symbol", se si vuole fare riferimento alla definizione nel modulo corrente"**
</dt> <dd>

Avviso semantico del modulo, specifico di SNMPv1 o SNMPv2C. Un simbolo noto al compilatore è stato ridefinito e viene fatto riferimento a questo simbolo. Il compilatore presuppone la definizione standard del simbolo. Pertanto, per usare una ridefinizione del simbolo standard, è necessario usare la notazione "Module.Symbol".

</dd> </dl>

## <a name="warning-1046"></a>Avviso 1046

<dl> <dt>

<span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, avviso>: " &lt; fileName &gt;<riga \#>: &lt; simbolo &gt; non definito. Presupponendo una definizione standard"**
</dt> <dd>

Avviso semantico del modulo, specifico di SNMPv1 o SNMPv2C. Un simbolo noto al compilatore non deve essere ridefinito o usato senza essere importato.

</dd> </dl>

## <a name="warning-1047"></a>Avviso 1047

<dl> <dt>

<span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, avviso>: " fileName<riga>: simbolo di definizione del tipo definito ma senza &lt; &gt; \# &lt; &gt; riferimento"**
</dt> <dd>

Avviso semantico del modulo, specifico di SNMPv1 o SNMPv2C. È necessario fare riferimento a tutte le assegnazioni di valore e a tutte le definizioni di tipo.

</dd> </dl>

## <a name="warning-1048"></a>Avviso 1048

<dl> <dt>

<span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, avviso>: " fileName<riga>: simbolo di definizione del valore definito ma a cui non &lt; &gt; viene fatto \# &lt; &gt; riferimento"**
</dt> <dd>

Avviso semantico del modulo, specifico di SNMPv1 o SNMPv2C. È necessario fare riferimento a tutte le assegnazioni di valore e a tutte le definizioni di tipo.

</dd> </dl>

## <a name="fatal-error-1049"></a>Errore irreversibile 1049

<dl> <dt>

<span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, errore irreversibile>: " &lt; fileName :<riga>: clausola DEFVAL non consentita per &gt; \# OBJECT-TYPE con SYNTAX NetworkAddress"**
</dt> <dd>

Errore semantico del modulo specifico di SNMPv1 per la chiamata di macro **OBJECT-TYPE.** La clausola DEFVAL non è consentita per un OBJECT-TYPE la cui clausola SYNTAX viene risolta in NetworkAddress.

</dd> </dl>

 

 



