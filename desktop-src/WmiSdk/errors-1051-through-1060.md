---
description: Descrive gli errori del provider SNMP WMI da 1051 a 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Errori da 1051 a 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 170eddf3126a40f929aa36899259b731fa244941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315726"
---
# <a name="errors-1051-through-1060"></a>Errori da 1051 a 1060

Descrive gli errori del provider SNMP WMI da 1051 a 1060.

[Errore irreversibile 1051](#fatal-error-1051)

[Errore irreversibile 1054](#fatal-error-1054)

[Errore irreversibile 1055](#fatal-error-1055)

## <a name="fatal-error-1051"></a>Errore irreversibile 1051

<dl> <dt>

<span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051,> irreversibile: " <fileName> : <riga \#>: riferimento ambiguo al simbolo <identifier> "**
</dt> <dd>

Errore semantico del modulo della sezione Imports, specifico di SNMPv1 o SNMPv2C. Ogni descrittore di oggetto che corrisponde a un oggetto in un MIB standard Internet deve essere univoco. Poiché MIB aziendali possono avere descrittori di oggetto comuni, i descrittori importati da due moduli devono essere usati senza ambiguità nel modulo MIB usando la notazione "Module. Descriptor".

</dd> </dl>

## <a name="fatal-error-1054"></a>Errore irreversibile 1054

<dl> <dt>

<span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054,> irreversibile: " <fileName> : <riga \#>: <identifier> nella clausola index non viene risolto in uno dei tipi consentiti"**
</dt> <dd>

Errore semantico del modulo di chiamata macro del **tipo di oggetto** . Il tipo di un oggetto nella clausola INDEX, o qualsiasi tipo specificato nella clausola INDEX, deve essere risolto in un tipo scalare, ovvero in una sequenza non sequenziale o non in sequenza di tipo. Qualsiasi tipo specificato nella clausola INDEX deve essere risolto anche in uno di questi.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1055"></a>Errore irreversibile 1055

<dl> <dt>

<span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055,> irreversibile: " <fileName> : <riga \#>: sintassi del tipo di oggetto index <identifier> , non viene risolto in uno dei tipi consentiti"**
</dt> <dd>

Errore semantico del modulo di chiamata macro del **tipo di oggetto** . Il tipo di un oggetto nella clausola INDEX, o qualsiasi tipo specificato nella clausola INDEX, deve essere risolto in un tipo scalare, ovvero in una sequenza non sequenziale o non in sequenza di tipo.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

 

 



