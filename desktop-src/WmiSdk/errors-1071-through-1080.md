---
description: Descrive gli errori del provider WMI SNMP da 1071 a 1080.
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: Errori da 1071 a 1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c92cfd1c79b5bedd070229adcbc4c663d209903428073fc976cd575022e9ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679621"
---
# <a name="errors-1071-through-1080"></a>Errori da 1071 a 1080

Descrive gli errori del provider WMI SNMP da 1071 a 1080.

[Avviso 1071](#warning-1071)

[Avviso 1072](#warning-1072)

[Errore irreversibile 1074](#fatal-error-1074)

[Errore irreversibile 1075](#fatal-error-1075)

[Errore irreversibile 1077](#fatal-error-1077)

[Errore irreversibile 1079](#fatal-error-1079)

[Avviso 1080](#warning-1080)

## <a name="warning-1071"></a>Avviso 1071

<dl> <dt>

<span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, avviso>: "<riga>: Simbolo non <fileName> presente nel modulo importato \# <identifier> <identifier> "**
</dt> <dd>

Avviso semantico del modulo relativo al riferimento incrociato, specifico di SNMPv1 o SNMPv2C. Un simbolo importato da un modulo non viene risolto in alcun elemento in tale modulo. Anche se il modulo è specificato nell'input, viene visualizzato questo avviso.

</dd> </dl>

## <a name="warning-1072"></a>Avviso 1072

<dl> <dt>

<span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, Avviso>: " <fileName> :<riga \#> OBJECT-TYPE <name> è un discendente di OBJECT-TYPE <name> del modulo <name> "**
</dt> <dd>

Avviso semantico del modulo di chiamata di macro **OBJECT-TYPE.** Un oggetto scalare non può avere oggetti discendenti.

Questo avviso può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1074"></a>Errore irreversibile 1074

<dl> <dt>

<span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074,> irreversibile: <fileName> ":<line \#> SEQUENCE (Conceptual row) OBJECT-TYPE <name> does not have a SEQUENCE OF (Conceptual table) OBJECT-TYPE as its parent"**
</dt> <dd>

Errore semantico del modulo di chiamata di macro **OBJECT-TYPE.** Ogni oggetto riga deve avere un oggetto tabella come padre.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1075"></a>Errore irreversibile 1075

<dl> <dt>

<span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075, errore irreversibile>:" <fileName> :<riga>: OBJECT-TYPE non può essere un elemento figlio della tabella OBJECT-TYPE del modulo a meno che non si trova nella sequenza di \# <name> <name> <name> quest'ultimo"**
</dt> <dd>

Errore semantico del modulo di chiamata di macro **OBJECT-TYPE.** Ogni oggetto SEQUENCE deve avere esattamente gli stessi oggetti indicati nella definizione del tipo SEQUENCE come elementi figlio. Analogamente, ogni oggetto SEQUENCE OF deve avere esattamente un elemento figlio.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1077"></a>Errore irreversibile 1077

<dl> <dt>

<span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077, fatal>: " <fileName> :<line \#>: The syntax of table OBJECT-TYPE is not the SEQUENCE OF the syntax of the <name> child OBJECT-TYPE <name> of module <name> "**
</dt> <dd>

Errore semantico del modulo di chiamata di macro **OBJECT-TYPE.** La clausola di sintassi di un oggetto tabella deve essere "SEQUENCE OF" della sintassi dell'oggetto riga.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1079"></a>Errore irreversibile 1079

<dl> <dt>

<span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079, fatal>:"fileName>:<line \#>: OBJECT-TYPE <name> is an extra child of OBJECT-TYPE of module <name> <name> "**
</dt> <dd>

Errore semantico del modulo di chiamata di macro **OBJECT-TYPE.** Ogni oggetto SEQUENCE OF deve avere esattamente un elemento figlio.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="warning-1080"></a>Avviso 1080

<dl> <dt>

<span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, avviso>: "<riga>: Modulo MIB , da cui viene importato il <fileName> \# <moduleName> <symbolName> simbolo, non è presente nell'input"**
</dt> <dd>

Avviso semantico del modulo relativo al riferimento incrociato, specifico di SNMPv1 o SNMPv2C. Se uno dei moduli nella sezione IMPORTS del modulo principale o di un modulo secondario non esiste, ma non viene fatto riferimento ai simboli di questo modulo, viene visualizzato questo avviso.

</dd> </dl>

 

 



