---
description: Descrive gli errori del provider SNMP WMI da 1061 a 1070.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Errori da 1061 a 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a4bf0773ade1f62eb11f0c496aea340410c4a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310365"
---
# <a name="errors-1061-through-1070"></a>Errori da 1061 a 1070

Descrive gli errori del provider SNMP WMI da 1061 a 1070.

[Errore irreversibile 1063](#fatal-error-1063)

[Errore irreversibile 1064](#fatal-error-1064)

[Errore irreversibile 1070](#fatal-error-1070)

## <a name="fatal-error-1063"></a>Errore irreversibile 1063

<dl> <dt>

<span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063,> irreversibile: " <fileName><riga \#>: il limite superiore della specifica di dimensione è inferiore al limite inferiore"**
</dt> <dd>

Errore semantico del modulo nella specifica di dimensione, specifico di SNMPv1 o SNMPv2C. Il simbolo usato in una specifica di dimensione deve essere risolto in stringa ottetto o opaco. Il limite inferiore di una specifica di intervallo o di dimensione non deve essere maggiore del limite superiore.

</dd> </dl>

## <a name="fatal-error-1064"></a>Errore irreversibile 1064

<dl> <dt>

<span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064,> irreversibile: " <fileName> : <riga \#>: l'elemento sequenza non <identifier> viene risolto in un tipo di oggetto"**
</dt> <dd>

Errore semantico del modulo di assegnazione del tipo, specifico di SNMPv1 e SNMPv2C. Tutti i singoli elementi di una dichiarazione di sequenza devono essere risolti in un tipo di oggetto.

</dd> </dl>

## <a name="fatal-error-1070"></a>Errore irreversibile 1070

<dl> <dt>

<span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070,> irreversibile: " <fileName><riga \#>: modulo MIB <moduleName> , da cui <symbolName> viene importato il simbolo, non è presente nell'input"**
</dt> <dd>

Errore semantico del modulo nel riferimento incrociato, specifico di SNMPv1 o SNMPv2C. Se uno dei moduli nella sezione Imports del modulo principale o di un modulo sussidiario non esiste e viene fatto riferimento a uno o più simboli da questo modulo, si verifica questo errore irreversibile.

</dd> </dl>

 

 



