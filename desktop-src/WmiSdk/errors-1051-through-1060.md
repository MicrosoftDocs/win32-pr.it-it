---
description: Descrive gli errori del provider WMI SNMP da 1051 a 1060.
ms.assetid: 789cc5b6-e3ef-4f66-8dec-6970d6df1fe9
ms.tgt_platform: multiple
title: Errori da 1051 a 1060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3405a799d71b33fa1dabd7c84964b8d1726d2e27
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882589"
---
# <a name="errors-1051-through-1060"></a>Errori da 1051 a 1060

Descrive gli errori del provider WMI SNMP da 1051 a 1060.

[Errore irreversibile 1051](#fatal-error-1051)

[Errore irreversibile 1054](#fatal-error-1054)

[Errore irreversibile 1055](#fatal-error-1055)

## <a name="fatal-error-1051"></a>Errore irreversibile 1051

<dl> <dt>

<span id="_1051__Fatal_____fileName___line____Ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__fatal_____filename___line____ambiguous_reference_to_symbol__identifier__"></span><span id="_1051__FATAL_____FILENAME___LINE____AMBIGUOUS_REFERENCE_TO_SYMBOL__IDENTIFIER__"></span>**<1051, Errore irreversibile>: " &lt; fileName &gt; :<riga \#>: riferimento ambiguo &lt; all'identificatore di simbolo &gt; "**
</dt> <dd>

Errore semantico del modulo della sezione IMPORTS, specifico di SNMPv1 o SNMPv2C. Ogni descrittore di oggetto corrispondente a un oggetto in un MIB Standard Internet deve essere univoco. Poiché i MIB aziendali possono avere descrittori di oggetti comuni, tali descrittori importati da due moduli devono essere usati senza ambiguità nel modulo MIB usando la notazione "module.descriptor".

</dd> </dl>

## <a name="fatal-error-1054"></a>Errore irreversibile 1054

<dl> <dt>

<span id="_1054__Fatal_____fileName___line_____identifier__in_INDEX_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__fatal_____filename___line_____identifier__in_index_clause_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1054__FATAL_____FILENAME___LINE_____IDENTIFIER__IN_INDEX_CLAUSE_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1054, errore irreversibile>: " &lt; fileName :<riga>: l'identificatore nella clausola INDEX non viene risolto in uno dei tipi &gt; \# &lt; &gt; consentiti"**
</dt> <dd>

Errore semantico del modulo di chiamata di macro **OBJECT-TYPE.** Il tipo di un oggetto nella clausola INDEX o di qualsiasi tipo specificato nella clausola INDEX deve essere risolto in un tipo scalare, ad esempio un tipo non SEQUENCE o non SEQUENCE OF. Qualsiasi tipo specificato nella clausola INDEX deve essere risolto anche in uno di questi.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1055"></a>Errore irreversibile 1055

<dl> <dt>

<span id="_1055__Fatal____fileName___line____SYNTAX_of_INDEX_OBJECT-TYPE__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__fatal____filename___line____syntax_of_index_object-type__identifier___does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1055__FATAL____FILENAME___LINE____SYNTAX_OF_INDEX_OBJECT-TYPE__IDENTIFIER___DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1055, fatal>:" &lt; fileName &gt; :<line \#>: SYNTAX of INDEX OBJECT-TYPE &lt; identifier &gt; , does not resolve to one of the allowed types"**
</dt> <dd>

Errore semantico del modulo di chiamata di macro **OBJECT-TYPE.** Il tipo di un oggetto nella clausola INDEX o di qualsiasi tipo specificato nella clausola INDEX deve essere risolto in un tipo scalare, ad esempio un tipo non SEQUENCE o non SEQUENCE OF.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

 

 



