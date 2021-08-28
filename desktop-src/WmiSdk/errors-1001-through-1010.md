---
description: Descrive gli errori del provider WMI SNMP da 1001 a 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Errori da 1001 a 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc5c754936d8900a16b89be1f1137984ee6e7d40
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886371"
---
# <a name="errors-1001-through-1010"></a>Errori da 1001 a 1010

Descrive gli errori del provider WMI SNMP da 1001 a 1010.

[Errore irreversibile 1001](#fatal-error-1001)

[Errore irreversibile 1002](#fatal-error-1002)

[Errore irreversibile 1003](#fatal-error-1003)

[Avviso 1004](#warning-1004)

[Avviso 1005](#warning-1005)

[Errore irreversibile 1006](#fatal-error-1006)

[Errore irreversibile 1008](#fatal-error-1008)

## <a name="fatal-error-1001"></a>Errore irreversibile 1001

<dl> <dt>

<span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, errore irreversibile>: " fileName :<line>: la clausola SYNTAX di OBJECT-TYPE non viene risolta nei tipi &lt; &gt; \# consentiti"
</dt> <dd>

Errore semantico del modulo di chiamata di macro OBJECT-TYPE. La clausola SYNTAX della macro OBJECT-TYPE deve essere risolta in un tipo o sottotipo, formato usando la specifica SIZE o range consentita dall'SMI SNMPv1 o SNMPv2C. In caso contrario, viene segnalato l'errore irreversibile 1001.

Questo errore può verificarsi durante la compilazione di un MIB SNMPv1 o SNMPv2C.

I tipi consentiti dall'SMI SNMPv1 sono:

-   INTEGER
-   NULL
-   OCTET STRING
-   IDENTIFICATORE DI OGGETTO
-   NetworkAddress
-   IpAddress
-   Contatore
-   Misuratore
-   TimeTicks
-   Opaco
-   DisplayString
-   PhysAddress

I tipi consentiti da SMI SNMPv2C sono:

-   INTEGER
-   OCTET STRING
-   IDENTIFICATORE DI OGGETTO
-   BITS
-   Numero intero32
-   IpAddress
-   Counter32
-   TimeTicks
-   Opaco
-   Counter64
-   Unsigned32
-   DisplayString
-   PhysAddress
-   MacAddress
-   Valore di verità
-   TestAndIncr
-   Tipo autonomo
-   InstancePointer
-   VariablePointer
-   RowPointer
-   RowStatus
-   TimeStamp
-   TimeInterval
-   DateAndTime
-   StorageType
-   Tdomain
-   Taddress

</dd> </dl>

## <a name="fatal-error-1002"></a>Errore irreversibile 1002

<dl> <dt>

<span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Errore irreversibile>: " &lt; fileName &gt; :<riga \#>: Clausola ACCESS non &lt; valida &gt; "
</dt> <dd>

Errore semantico del modulo di chiamata di macro OBJECT-TYPE. Per SNMPv1, la clausola ACCESS della macro OBJECT-TYPE deve essere "sola lettura", "sola scrittura", "lettura/scrittura" o "non accessibile".

Per SNMPv2C, la clausola MAX-ACCESS deve essere "read-only", "read-create", "read/write" o "not-accessible".

</dd> </dl>

## <a name="fatal-error-1003"></a>Errore irreversibile 1003

<dl> <dt>

<span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Errore irreversibile>: " &lt; fileName &gt; :<riga \#>: Clausola STATUS &lt; non valida &gt; "
</dt> <dd>

Errore semantico del modulo di chiamata di macro OBJECT-TYPE. Per SNMPv1, la clausola STATUS di una chiamata di macro OBJECT-TYPE deve essere "obbligatoria", "facoltativa", "obsoleta" o "deprecata".

Per SNMPv2C, la clausola STATUS di una chiamata di macro OBJECT-TYPE deve essere "corrente", "deprecata" o "obsoleta".

</dd> </dl>

## <a name="warning-1004"></a>Avviso 1004

<dl> <dt>

<span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, warning>: " &lt; fileName &gt; :<line>: OBJECT-TYPE identifier , la cui sintassi viene risolta in uno dei tipi Counter non termina con la \# &lt; lettera &gt; 's' "
</dt> <dd>

Avviso semantico del modulo di chiamata di macro OBJECT-TYPE. L'identificatore per un oggetto di SYNTAX Counter (SNMPv1) o Counter32 e Counter64 (SNMPv2C) deve essere plurale.

Questo avviso può verificarsi durante la compilazione di un MIB SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="warning-1005"></a>Avviso 1005

<dl> <dt>

<span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, avviso>: " &lt; fileName &gt; :<riga \#>: OBJECT-TYPE con SINTASSI "SEQUENCE OF", deve avere una clausola ACCESS "non accessibile"
</dt> <dd>

Avviso semantico del modulo di chiamata di macro OBJECT-TYPE. Una tabella o una riga concettuale (rispettivamente i tipi di oggetto SEQUENCE OF o SEQUENCE) deve essere "non accessibile".

Questo avviso può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1006"></a>Errore irreversibile 1006

<dl> <dt>

<span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, errore irreversibile>: " &lt; fileName :<riga> identificatore OBJECT-TYPE , che è di SYNTAX SEQUENCE, non ha una clausola INDEX o &gt; \# &lt; &gt; AUGMENTS"
</dt> <dd>

Errore semantico del modulo di chiamata di macro OBJECT-TYPE. Per SNMPv1, la clausola INDEX deve essere presente per una definizione OBJECT-TYPE la cui sintassi viene risolta in un tipo SEQUENCE.

Per SNMPv2C, la clausola INDEX o AUGMENTS deve essere presente per una dichiarazione di riga concettuale.

</dd> </dl>

## <a name="fatal-error-1008"></a>Errore irreversibile 1008

<dl> <dt>

<span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, errore irreversibile>: " &lt; fileName &gt; :<line \#>: OBJECT-TYPE &lt; identifier , which is of SYNTAX &gt; "SEQUENCE" has not been referenced"
</dt> <dd>

Errore semantico del modulo di chiamata di macro OBJECT-TYPE. Un OBJECT-TYPE con la clausola SYNTAX come tipo SEQUENCE deve figurare nella clausola SYNTAX esattamente una chiamata OBJECT-TYPE che sta per una dichiarazione di tabella, ad esempio un oggetto con la clausola SYNTAX come tipo SEQUENCE OF. Il <riga \#> parametro fa riferimento al secondo punto di riferimento.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

 

 



