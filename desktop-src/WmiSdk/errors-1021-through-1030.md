---
description: Descrive gli errori del provider SNMP WMI da 1021 a 1033.
ms.assetid: fc638d0f-20f4-46d0-a36a-c3898415f35c
ms.tgt_platform: multiple
title: Errori da 1021 a 1030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8bce9c7c4d70250fa63ad0100cf93c8d5b26984
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310369"
---
# <a name="errors-1021-through-1030"></a>Errori da 1021 a 1030

Descrive gli errori del provider SNMP WMI da 1021 a 1033.

[Errore irreversibile 1021](#fatal-error-1021)

[Errore irreversibile 1022](#fatal-error-1022)

[Errore irreversibile 1023](#fatal-error-1023)

[Errore irreversibile 1024](#fatal-error-1024)

[Errore irreversibile 1025](#fatal-error-1025)

[Errore irreversibile 1026](#fatal-error-1026)

[Avviso 1027](#warning-1027)

[Errore irreversibile 1028](#fatal-error-1028)

[Errore irreversibile 1029](#fatal-error-1029)

[Errore irreversibile 1030](#fatal-error-1030)

## <a name="fatal-error-1021"></a>Errore irreversibile 1021

<dl> <dt>

<span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021,> irreversibile: " <fileName><riga \#>: <identifier> l'identificatore nella clausola Variables di trap-type non viene risolto in un tipo di oggetto scalare"**
</dt> <dd>

Chiamata della macro di **tipo trap** , errore semantico del modulo specifico di SNMPv1. Ogni elemento nell'elenco di variabili utilizzato nella clausola VARIABLES di una chiamata a una macro di **tipo trap** deve risolvere il nome di un'istanza scalare di tipo oggetto.

</dd> </dl>

## <a name="fatal-error-1022"></a>Errore irreversibile 1022

<dl> <dt>

<span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022,> irreversibile: " <fileName><riga \#>: il valore non viene risolto nel tipo <type> "**
</dt> <dd>

Errore semantico del modulo di assegnazione valore, specifico di SNMPv1 e SNMPv2C. Il tipo errato del valore del RHS di un'assegnazione di valore INTEGER, **null**, stringa ottetto o identificatore di oggetto non è corretto.

</dd> </dl>

## <a name="fatal-error-1023"></a>Errore irreversibile 1023

<dl> <dt>

<span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023,> irreversibile: " <fileName><riga \#>: <identifier> l'identificatore non viene risolto nel tipo <identifier> "**
</dt> <dd>

Errore semantico del modulo di assegnazione valore, specifico di SNMPv1 e SNMPv2C. Un simbolo (riferimento al valore) nel RHS di un'assegnazione di valore INTEGER, **null**, stringa ottetto o identificatore di oggetto non viene risolto nel tipo corretto.

</dd> </dl>

## <a name="fatal-error-1024"></a>Errore irreversibile 1024

<dl> <dt>

<span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024,> irreversibile: " <fileName><riga \#>: numero intero negativo nella definizione del valore OID"**
</dt> <dd>

Errore semantico del modulo di assegnazione valore, specifico di SNMPv1 e SNMPv2C. Tutti i valori in un elenco di componenti OID devono essere numeri interi non negativi (preferibilmente positivi).

</dd> </dl>

## <a name="fatal-error-1025"></a>Errore irreversibile 1025

<dl> <dt>

<span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025,> irreversibile: " <identifier> l'identificatore nel valore OID non viene risolto in un numero intero positivo"**
</dt> <dd>

Errore semantico del modulo di assegnazione valore, specifico di SNMPv1 e SNMPv2C. Tutti i valori in un elenco di componenti OID devono essere numeri interi non negativi (preferibilmente positivi).

</dd> </dl>

## <a name="fatal-error-1026"></a>Errore irreversibile 1026

<dl> <dt>

<span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026,> irreversibile: " <fileName><riga \#>: <identifier> l'identificatore nel valore OID non viene risolto in un valore OID né in un numero intero positivo"**
</dt> <dd>

Errore semantico del modulo di assegnazione valore, specifico di SNMPv1 e SNMPv2C. Il primo componente utilizzato in un valore OID deve essere risolto in un valore OID o un numero intero.

</dd> </dl>

## <a name="warning-1027"></a>Avviso 1027

<dl> <dt>

<span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, avviso>: " <fileName><riga \#>: simbolo importato non <identifier> usato"**
</dt> <dd>

Avviso semantico del modulo della sezione Imports, specifico di SNMPv1 e SNMPv2C. Viene emesso un avviso per ogni simbolo importato inutilizzato.

</dd> </dl>

## <a name="fatal-error-1028"></a>Errore irreversibile 1028

<dl> <dt>

<span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028,> irreversibile: "modulo <identifier> non importato nella sezione IMports"**
</dt> <dd>

Errore semantico del modulo della sezione Imports, specifico di SNMPv1 o SNMPv2C. Il nome di un modulo usato per fare riferimento a un simbolo deve essere presente nella clausola Imports oppure corrispondere al nome del modulo corrente.

</dd> </dl>

## <a name="fatal-error-1029"></a>Errore irreversibile 1029

<dl> <dt>

<span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029,> irreversibile: " <fileName><riga \#>: Impossibile importare il modulo corrente <identifier> "**
</dt> <dd>

Errore semantico del modulo della sezione Imports, specifico di SNMPv1 o SNMPv2C. Il nome del modulo corrente è anche costituito da figure nell'elenco Imports.

</dd> </dl>

## <a name="fatal-error-1030"></a>Errore irreversibile 1030

<dl> <dt>

<span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030,> irreversibile: " <fileName><riga \#>: il simbolo non è stato <identifier> importato dal modulo <identifier> "**
</dt> <dd>

Errore semantico del modulo della sezione Imports, specifico di SNMPv1 o SNMPv2C. È stata usata la notazione "Module. symbol", ma il simbolo non è stato importato dal modulo specificato nella sezione Imports.

</dd> </dl>

 

 



