---
description: Descrive gli errori del provider SNMP WMI da 1001 a 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Errori da 1001 a 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa10b83c660d617bdbf37b6f119e824bbba60616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313191"
---
# <a name="errors-1001-through-1010"></a>Errori da 1001 a 1010

Descrive gli errori del provider SNMP WMI da 1001 a 1010.

[Errore irreversibile 1001](#fatal-error-1001)

[Errore irreversibile 1002](#fatal-error-1002)

[Errore irreversibile 1003](#fatal-error-1003)

[Avviso 1004](#warning-1004)

[Avviso 1005](#warning-1005)

[Errore irreversibile 1006](#fatal-error-1006)

[Errore irreversibile 1008](#fatal-error-1008)

## <a name="fatal-error-1001"></a>Errore irreversibile 1001

<dl> <dt>

<span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001,> irreversibile: " <fileName> : <riga \#>: la clausola della sintassi di tipo oggetto non viene risolta nei tipi consentiti"
</dt> <dd>

Errore semantico del modulo di chiamata macro del tipo di oggetto. La clausola SYNTAX della macro del tipo di oggetto deve essere risolta in un tipo o sottotipo, formato utilizzando la specifica di dimensione o intervallo consentita da SNMPv1 o SNMPv2C SMI. In caso contrario, viene restituito l'errore irreversibile 1001.

Questo errore può verificarsi durante la compilazione di un MIB SNMPv1 o SNMPv2C.

I tipi consentiti da SNMPv1 SMI sono:

-   INTEGER
-   NULL
-   STRINGA OTTETTO
-   IDENTIFICATORE OGGETTO
-   NetworkAddress
-   IpAddress
-   Contatore
-   Misuratore
-   TimeTicks
-   Opaco
-   DisplayString
-   PhysAddress

I tipi consentiti da SNMPv2C SMI sono:

-   INTEGER
-   STRINGA OTTETTO
-   IDENTIFICATORE OGGETTO
-   BITS
-   Integer32
-   IpAddress
-   Counter32
-   TimeTicks
-   Opaco
-   Counter64
-   Unsigned32
-   DisplayString
-   PhysAddress
-   MacAddress
-   TruthValue
-   TestAndIncr
-   AutonomousType
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

<span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002,> irreversibile: " <fileName> : <riga \#>: clausola di accesso non valida <clause> "
</dt> <dd>

Errore semantico del modulo di chiamata macro del tipo di oggetto. Per SNMPv1, la clausola ACCESS della macro del tipo di oggetto deve essere di sola lettura, "" sola scrittura "," lettura/scrittura "o" non accessibile ".

Per SNMPv2C, la clausola MAX-ACCESS deve essere di sola lettura, "Read-create", "Read/Write" o "non accessibile".

</dd> </dl>

## <a name="fatal-error-1003"></a>Errore irreversibile 1003

<dl> <dt>

<span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003,> irreversibile: " <fileName> : <riga \#>: clausola di stato non valida <clause> "
</dt> <dd>

Errore semantico del modulo di chiamata macro del tipo di oggetto. Per SNMPv1, la clausola STATUS di una chiamata di macro di tipo oggetto deve essere "obbligatoria", "facoltativo", "obsoleto" o "deprecato".

Per SNMPv2C, la clausola STATUS di una chiamata di macro di tipo oggetto deve essere "Current", "deprecated" o "obsolete".

</dd> </dl>

## <a name="warning-1004"></a>Avviso 1004

<dl> <dt>

<span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: " <fileName> : <line \#>: Object-Type <identifier> , la cui sintassi viene risolta in uno dei tipi di contatore non termina con '" della lettera
</dt> <dd>

Avviso semantico del modulo di chiamata macro del tipo di oggetto. L'identificatore per un oggetto della sintassi del contatore (SNMPv1) o Counter32 e Counter64 (SNMPv2C) deve essere plurale.

Questo avviso può verificarsi durante la compilazione di un MIB SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="warning-1005"></a>Avviso 1005

<dl> <dt>

<span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, avviso>: " <fileName> : <riga \#>: tipo oggetto con sintassi" Sequence of ", deve avere una clausola di accesso" non accessibile "
</dt> <dd>

Avviso semantico del modulo di chiamata macro del tipo di oggetto. Una tabella o una riga concettuale (rispettivamente, sequenza o tipi di oggetto sequenza) deve essere "non accessibile".

Questo avviso può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1006"></a>Errore irreversibile 1006

<dl> <dt>

<span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006,> irreversibile: " <fileName> : <riga \#> tipo di oggetto <identifier> , che è di sequenza di sintassi, non ha una clausola index o augments"
</dt> <dd>

Errore semantico del modulo di chiamata macro del tipo di oggetto. Per SNMPv1, la clausola INDEX deve essere presente per una definizione di tipo oggetto la cui sintassi viene risolta in un tipo di sequenza.

Per SNMPv2C, è necessario che la clausola INDEX o AUGMENTes sia presente per una dichiarazione di riga concettuale.

</dd> </dl>

## <a name="fatal-error-1008"></a>Errore irreversibile 1008

<dl> <dt>

<span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008,> irreversibile: " <fileName> : <riga \#>: il tipo <identifier> di oggetto, che è della sintassi" Sequence ", non è stato fatto riferimento"
</dt> <dd>

Errore semantico del modulo di chiamata macro del tipo di oggetto. Un tipo di oggetto con la clausola SYNTAX come tipo di sequenza deve figurare nella clausola della sintassi di una chiamata di tipo oggetto che sta per una dichiarazione di tabella, ovvero un oggetto con la clausola SYNTAX come sequenza di tipo. Il parametro <line \#> si riferisce al secondo punto di riferimento.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

 

 



