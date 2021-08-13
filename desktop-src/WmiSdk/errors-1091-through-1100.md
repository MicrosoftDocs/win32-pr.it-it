---
description: Descrive gli errori del provider SNMP WMI da 1091 a 1100.
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: Errori da 1091 a 1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cedd1fc12fa5f547e041201f5411a262ddb3a3958ef58e8bed3bfcf8270d7058
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244321"
---
# <a name="errors-1091-through-1100"></a>Errori da 1091 a 1100

Descrive gli errori del provider SNMP WMI da 1091 a 1100.

[Avviso 1091](#warning-1091)

[Errore irreversibile 1092](#fatal-error-1092)

[Errore irreversibile 1093](#fatal-error-1093)

[Errore irreversibile 1094](#fatal-error-1094)

[Errore irreversibile 1095](#fatal-error-1095)

[Errore irreversibile 1097](#fatal-error-1097)

[Errore irreversibile 1098](#fatal-error-1098)

[Errore irreversibile 1099](#fatal-error-1099)

## <a name="warning-1091"></a>Avviso 1091

<dl> <dt>

<span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, avviso>: <fileName> ":<riga> clausola IMPLIED non è consentita per gli oggetti di \# dimensioni fisse"**
</dt> <dd>

Avviso semantico di chiamata di macro **OBJECT-TYPE** SNMPv2C specifico. La parola chiave IMPLIED può essere presente solo per un oggetto con una sintassi a lunghezza variabile, ad esempio OBJECT IDENTIFIER o OCTET STRING a lunghezza variabile, nella clausola INDEX.

</dd> </dl>

## <a name="fatal-error-1092"></a>Errore irreversibile 1092

<dl> <dt>

<span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, Fatal>: <fileName> ":<line \#> IMPLIED clause not allowed for potentially zero-length objects"**
</dt> <dd>

Errore semantico del modulo specifico della chiamata di macro **OBJECT-TYPE** SNMPv2C. La clausola IMPLIED non può essere usata in un oggetto a lunghezza variabile se tale oggetto può avere lunghezza zero.

</dd> </dl>

## <a name="fatal-error-1093"></a>Errore irreversibile 1093

<dl> <dt>

<span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093. Errore>: "<riga>: solo il tipo "INTEGER" può essere enumerato in base <fileName> \# all'SMI V1"**
</dt> <dd>

Assegnazione del tipo, errore semantico del modulo specifico di SNMPv1. Un'enumerazione MIB SNMPv1 può usare solo il tipo INTEGER.

</dd> </dl>

## <a name="fatal-error-1094"></a>Errore irreversibile 1094

<dl> <dt>

<span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094. Errore>: "<riga>: il tipo usato nell'enumerazione non viene risolto <fileName> in uno dei tipi \# consentiti"**
</dt> <dd>

Assegnazione di tipo, errore semantico del modulo specifico di SNMPv2C. Il tipo utilizzato in un'enumerazione deve essere INTEGER o un tipo equivalente o un'altra enumerazione.

</dd> </dl>

## <a name="fatal-error-1095"></a>Errore irreversibile 1095

<dl> <dt>

<span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095. Errore>: "<riga>: il membro di enumerazione <fileName> non è un membro \# dell'enumerazione padre"**
</dt> <dd>

Assegnazione di tipo, errore semantico del modulo specifico di SNMPv2C. Se si usa un'altra enumerazione, il relativo set di elementi deve essere un subset del set di elementi dell'enumerazione padre.

</dd> </dl>

## <a name="fatal-error-1097"></a>Errore irreversibile 1097

<dl> <dt>

<span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097, Fatal>: <fileName> "<line \#>: identifier <name> does not resolve to an integer value"**
</dt> <dd>

Assegnazione di tipo, errore semantico del modulo specifico di SNMPv2C. I valori nel tipo BITS devono essere valori interi.

</dd> </dl>

## <a name="fatal-error-1098"></a>Errore irreversibile 1098

<dl> <dt>

<span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098, Errore irreversibile>: "<<fileName> \# riga>: valore duplicato <value> nel costrutto BITS"**
</dt> <dd>

Assegnazione di tipo, errore semantico del modulo specifico di SNMPv2C. Non devono essere presenti nomi e valori duplicati in un costrutto BITS. Il <riga> è la posizione della ricorrenza \# del nome/valore.

</dd> </dl>

## <a name="fatal-error-1099"></a>Errore irreversibile 1099

<dl> <dt>

<span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099, Errore irreversibile>: "<<fileName> riga \#>: Nome duplicato <identifier> nel costrutto BITS"**
</dt> <dd>

Assegnazione di tipo, errore semantico del modulo specifico di SNMPv2C. Non devono essere presenti nomi e valori duplicati in un costrutto BITS. Il <riga> è la posizione della ricorrenza \# del nome/valore.

</dd> </dl>

 

 



