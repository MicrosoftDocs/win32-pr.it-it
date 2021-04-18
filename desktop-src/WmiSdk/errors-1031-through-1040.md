---
description: Descrive gli errori del provider SNMP WMI da 1031 a 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Errori da 1031 a 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34079c2cbdb8e50aef04e8c364ba99abee760fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315728"
---
# <a name="errors-1031-through-1040"></a>Errori da 1031 a 1040

Descrive gli errori del provider SNMP WMI da 1031 a 1040.

[Avviso 1031](#warning-1031)

[Errore irreversibile 1032](#fatal-error-1032)

[Errore irreversibile 1033](#fatal-error-1033)

[Avviso 1034](#warning-1034)

[Avviso 1036](#warning-1036)

[Errore irreversibile 1037](#fatal-error-1037)

[Errore irreversibile 1038](#fatal-error-1038)

[Errore irreversibile 1039](#fatal-error-1039)

[Errore irreversibile 1040](#fatal-error-1040)

## <a name="warning-1031"></a>Avviso 1031

<dl> <dt>

<span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, avviso>: " <fileName> : <riga \#>: <identifier> è necessario importare dal modulo il simbolo standard <identifier> . Presumendo la definizione standard ".**
</dt> <dd>

Avviso semantico del modulo della sezione Imports, specifico di SNMPv1 e SNMPv2C. Se un identificatore SNMP noto al compilatore si trova nella sezione Imports, il modulo da cui viene importato deve essere uno dei moduli standard.

Alcune importazioni di uso comune sono "conoscenze presunte" nella parte del compilatore. Non è necessario che il compilatore richieda l'accesso ad altri moduli di informazioni per risolverli.

Le importazioni SNMPv1 e SNMPv2C predefinite sono descritte nelle tabelle seguenti.

</dd> </dl>

**Importazioni SNMPv1 predefinite**



| Importa classe | Modulo      | Istanze                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| Valore ASN. 1  | RFC1155-SMI | Internet, directory, gestione, sperimentale, privato, aziende |
|              | RFC1213-MIB | MIB-II e IP, interfacce, trasmissione                             |
| Tipo ASN. 1   | RFC1155-SMI | NetworkAddress, IpAddress, Counter, gauge, TimeTicks, Opaque        |
|              | RFC1213-MIB | DisplayString, PhysAddress                                          |
| Macro ASN. 1  | RFC-1212    | TIPO OGGETTO                                                         |
|              | RFC-1215    | TIPO TRAP                                                           |



 

**Importazioni SNMPv2C predefinite**



| Importa classe       | Modulo      | Istanze                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore ASN. 1        | SNMPv2-SMI  | org, DoD, Internet, directory, MGMT, MIB-2, trasmissione, sperimentale, privato, imprese, sicurezza, SNMPv2, snmpDomains, snmpProxys, snmpModules                                                           |
|                    | SNMPv2-TM   | rfc1157Proxy                                                                                                                                                                                                   |
| Identità dell'oggetto    | SNMPv2-SMI  | zeroDotZero                                                                                                                                                                                                    |
|                    | SNMPv2-TM   | snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain                                                                                                                     |
| Tipo ASN. 1         | SNMPv2-SMI  | Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, gauge32                                                                                                                             |
| Macro ASN. 1        | SNMPv2-SMI  | MODULE-IDENTITY, OGGETTO-IDENTITY, TIPO-OGGETTO, TIPO DI NOTIFICA                                                                                                                                               |
|                    | SNMPv2-CONF | OGGETTO-GRUPPO, NOTIFICA-GRUPPO, CONFORMITÀ MODULO, AGENTE-FUNZIONALITÀ                                                                                                                                        |
|                    | SNMPv2-TC   | CONVENZIONE TESTUALE                                                                                                                                                                                             |
| Convenzione testuale | SNMPv2-TC   | DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, TDomain, Taddress |
|                    | SNMPv2-TM   | SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a>Errore irreversibile 1032

<dl> <dt>

<span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032,> irreversibile: " <fileName><riga \#>: valore duplicato <value> nell'enumerazione"**
</dt> <dd>

Errore semantico del modulo in un'enumerazione, specifico di SNMPv1 o SNMPv2C. Non devono essere presenti valori duplicati. Il <riga \#> parametro è la posizione della ricorrenza del nome/valore.

</dd> </dl>

## <a name="fatal-error-1033"></a>Errore irreversibile 1033

<dl> <dt>

<span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033,> irreversibile: " <fileName><riga \#>: nome duplicato <identifier> nell'enumerazione"**
</dt> <dd>

Errore semantico del modulo in un'enumerazione, specifico di SNMPv1 o SNMPv2C. Non devono essere presenti nomi duplicati. Il <riga \#> parametro è la posizione della ricorrenza del nome/valore.

</dd> </dl>

## <a name="warning-1034"></a>Avviso 1034

<dl> <dt>

<span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, avviso>: " <fileName><riga \#>: il valore 0 non è consentito in un'enumerazione"**
</dt> <dd>

Avviso semantico del modulo in un'enumerazione, specifico di SNMPv1 o SNMPv2C. Si consiglia di non utilizzare un valore denominato zero in un'enumerazione.

</dd> </dl>

## <a name="warning-1036"></a>Avviso 1036

<dl> <dt>

<span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, avviso> " <fileName><riga \#>: il valore nell'enumerazione non viene risolto in un numero intero positivo"**
</dt> <dd>

Avviso semantico del modulo in un'enumerazione, specifico di SNMPv1 o SNMPv2C. In un'enumerazione non è consentito un valore negativo.

</dd> </dl>

## <a name="fatal-error-1037"></a>Errore irreversibile 1037

<dl> <dt>

<span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037,> irreversibile: " <fileName><riga \#>: l'identificatore <identifier> non viene risolto in una stringa di ottetti o tipi opachi"**
</dt> <dd>

Errore semantico del modulo nella specifica di dimensione, specifico di SNMPv1 o SNMPv2C. Il simbolo usato in una specifica di dimensione deve essere risolto in stringa ottetto o opaco.

</dd> </dl>

## <a name="fatal-error-1038"></a>Errore irreversibile 1038

<dl> <dt>

<span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038,> irreversibile: " <fileName><riga \#>: l'identificatore non <identifier> risolve un tipo Integer o un tipo di misuratore"**
</dt> <dd>

Errore semantico del modulo nella specifica di intervallo. Questo errore può verificarsi in SNMPv1 o SNMPv2C.

In SNMPv1 il simbolo usato in una specifica di intervallo deve essere risolto in INTEGER o misuratore.

In SNMPv2C il simbolo usato in una specifica di intervallo deve essere risolto in INTEGER, gauge32, Integer32 o Unsigned32.

</dd> </dl>

## <a name="fatal-error-1039"></a>Errore irreversibile 1039

<dl> <dt>

<span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039,> irreversibile: <fileName><riga \#>: valore negativo utilizzato nella specifica di dimensione "**
</dt> <dd>

Errore semantico del modulo nella specifica di dimensione, specifico di SNMPv1 o SNMPv2C. Qualsiasi valore utilizzato per specificare le dimensioni non deve essere negativo.

</dd> </dl>

## <a name="fatal-error-1040"></a>Errore irreversibile 1040

<dl> <dt>

<span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040,> irreversibile: " <fileName><riga \#>: <identifier> l'identificatore nella specifica di dimensione non viene risolto in un valore integrale non negativo"**
</dt> <dd>

Errore semantico del modulo nella specifica di intervallo o di dimensione, specifico di SNMPv1 o SNMPv2C. Qualsiasi simbolo utilizzato per specificare un valore in una specifica di dimensione viene risolto in un valore non negativo.

</dd> </dl>

 

 



