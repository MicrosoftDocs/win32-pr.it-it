---
description: Descrive gli errori del provider WMI SNMP da 1061 a 1070.
ms.assetid: 1bbd6153-7241-4673-ae17-1caa92b2e6a6
ms.tgt_platform: multiple
title: Errori da 1061 a 1070
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c0072f30c8daf584c1aaf2acf783b15d2d9498a3c1479264a1db361c3e3ce43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117924572"
---
# <a name="errors-1061-through-1070"></a>Errori da 1061 a 1070

Descrive gli errori del provider WMI SNMP da 1061 a 1070.

[Errore irreversibile 1063](#fatal-error-1063)

[Errore irreversibile 1064](#fatal-error-1064)

[Errore irreversibile 1070](#fatal-error-1070)

## <a name="fatal-error-1063"></a>Errore irreversibile 1063

<dl> <dt>

<span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, errore irreversibile>: "<riga>: Limite superiore della specifica SIZE è minore del <fileName> \# limite inferiore"**
</dt> <dd>

Errore semantico del modulo nella specifica SIZE, specifico di SNMPv1 o SNMPv2C. Il simbolo usato in una specifica SIZE deve essere risolto in OCTET STRING o Opaque. Il limite inferiore di un intervallo o di una specifica SIZE non deve essere maggiore del limite superiore.

</dd> </dl>

## <a name="fatal-error-1064"></a>Errore irreversibile 1064

<dl> <dt>

<span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, errore irreversibile>: ":<riga>: L'elemento SEQUENCE non viene risolto <fileName> \# in un <identifier> OBJECT-TYPE"**
</dt> <dd>

Errore semantico del modulo di assegnazione del tipo, specifico di SNMPv1 o SNMPv2C. Tutti i singoli elementi di una dichiarazione SEQUENCE devono essere risolti in OBJECT-TYPE.

</dd> </dl>

## <a name="fatal-error-1070"></a>Errore irreversibile 1070

<dl> <dt>

<span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, errore irreversibile>: "<riga>: Modulo MIB , da cui viene importato il simbolo, non è <fileName> \# presente <moduleName> <symbolName> nell'input"**
</dt> <dd>

Errore semantico del modulo nel riferimento incrociato, specifico di SNMPv1 o SNMPv2C. Se uno dei moduli nella sezione IMPORTS del modulo principale o di un modulo secondario non esiste e si fa effettivamente riferimento a uno o più simboli di questo modulo, si verifica questo errore irreversibile.

</dd> </dl>

 

 



