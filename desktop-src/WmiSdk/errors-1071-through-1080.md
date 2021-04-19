---
description: Descrive gli errori del provider SNMP WMI da 1071 a 1080.
ms.assetid: c9161c96-6839-4b32-b1bd-b40af18ab314
ms.tgt_platform: multiple
title: Errori da 1071 a 1080
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277aa7dd69d674ebc16bc0a2b4d104c349e593a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319299"
---
# <a name="errors-1071-through-1080"></a>Errori da 1071 a 1080

Descrive gli errori del provider SNMP WMI da 1071 a 1080.

[Avviso 1071](#warning-1071)

[Avviso 1072](#warning-1072)

[Errore irreversibile 1074](#fatal-error-1074)

[Errore irreversibile 1075](#fatal-error-1075)

[Errore irreversibile 1077](#fatal-error-1077)

[Errore irreversibile 1079](#fatal-error-1079)

[Avviso 1080](#warning-1080)

## <a name="warning-1071"></a>Avviso 1071

<dl> <dt>

<span id="_1071__Warning_____fileName__line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__warning_____filename__line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1071__WARNING_____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1071, avviso>: " <fileName><riga \#>: simbolo <identifier> non presente nel modulo importato <identifier> "**
</dt> <dd>

Avviso semantico del modulo relativo al riferimento incrociato, specifico di SNMPv1 o SNMPv2C. Un simbolo importato da un modulo non viene risolto in alcun elemento del modulo. Anche se tale modulo è specificato nell'input, viene visualizzato questo avviso.

</dd> </dl>

## <a name="warning-1072"></a>Avviso 1072

<dl> <dt>

<span id="_1072__Warning_____fileName___line___OBJECT-TYPE__name__is_a_descendant_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1072__warning_____filename___line___object-type__name__is_a_descendant_of_object-type__name__of_module__name__"></span><span id="_1072__WARNING_____FILENAME___LINE___OBJECT-TYPE__NAME__IS_A_DESCENDANT_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span><**1072, avviso>: " <fileName> : <linea \#> oggetto-tipo <name> è un discendente di tipo oggetto <name> di modulo <name> "**
</dt> <dd>

Avviso semantico del modulo di chiamata macro del **tipo di oggetto** . Un oggetto scalare non può contenere oggetti discendenti.

Questo avviso può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1074"></a>Errore irreversibile 1074

<dl> <dt>

<span id="_1074__Fatal_____fileName___line___SEQUENCE__Conceptual_row__OBJECT-TYPE__name__does_not_have_a_SEQUENCE_OF__Conceptual_table__OBJECT-TYPE_as_its_parent_"></span><span id="_1074__fatal_____filename___line___sequence__conceptual_row__object-type__name__does_not_have_a_sequence_of__conceptual_table__object-type_as_its_parent_"></span><span id="_1074__FATAL_____FILENAME___LINE___SEQUENCE__CONCEPTUAL_ROW__OBJECT-TYPE__NAME__DOES_NOT_HAVE_A_SEQUENCE_OF__CONCEPTUAL_TABLE__OBJECT-TYPE_AS_ITS_PARENT_"></span>**<1074,> irreversibile: " <fileName> : <riga \#> sequenza (riga concettuale) il tipo <name> di oggetto non dispone di una sequenza di tipo di oggetto (tabella concettuale) come padre"**
</dt> <dd>

Errore semantico del modulo di chiamata macro del **tipo di oggetto** . Ogni oggetto riga deve avere un oggetto Table come padre.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1075"></a>Errore irreversibile 1075

<dl> <dt>

<span id="_1075__Fatal____fileName___line____OBJECT-TYPE__name__cannot_be_a_child_of_table_OBJECT-TYPE__name__of_module__name__unless_it_is_in_the_SEQUENCE_of_the_latter_"></span><span id="_1075__fatal____filename___line____object-type__name__cannot_be_a_child_of_table_object-type__name__of_module__name__unless_it_is_in_the_sequence_of_the_latter_"></span><span id="_1075__FATAL____FILENAME___LINE____OBJECT-TYPE__NAME__CANNOT_BE_A_CHILD_OF_TABLE_OBJECT-TYPE__NAME__OF_MODULE__NAME__UNLESS_IT_IS_IN_THE_SEQUENCE_OF_THE_LATTER_"></span>**<1075,> irreversibile: " <fileName> : <riga \#>: <name> il tipo di oggetto non può essere un elemento figlio di un tipo di oggetto tabella, a <name> meno che non si <name> trovi nella sequenza del secondo"**
</dt> <dd>

Errore semantico del modulo di chiamata macro del **tipo di oggetto** . Ogni oggetto sequenza deve avere esattamente gli stessi oggetti indicati nella definizione del tipo di sequenza come elementi figlio. Analogamente, ogni sequenza di oggetto deve avere esattamente un elemento figlio.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1077"></a>Errore irreversibile 1077

<dl> <dt>

<span id="_1077__Fatal_____fileName___line____The_syntax_of_table_OBJECT-TYPE__name__is_not_the_SEQUENCE_OF_the_syntax_of_the_child_OBJECT-TYPE__name__of_module__name__"></span><span id="_1077__fatal_____filename___line____the_syntax_of_table_object-type__name__is_not_the_sequence_of_the_syntax_of_the_child_object-type__name__of_module__name__"></span><span id="_1077__FATAL_____FILENAME___LINE____THE_SYNTAX_OF_TABLE_OBJECT-TYPE__NAME__IS_NOT_THE_SEQUENCE_OF_THE_SYNTAX_OF_THE_CHILD_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1077,> irreversibile: " <fileName> : <riga \#>: la sintassi dell'oggetto Table-Type <name> non è la sequenza della sintassi del tipo di oggetto figlio <name> del modulo <name> "**
</dt> <dd>

Errore semantico del modulo di chiamata macro del **tipo di oggetto** . La clausola della sintassi di un oggetto Table deve essere "SEQUENCE OF" della sintassi dell'oggetto riga.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1079"></a>Errore irreversibile 1079

<dl> <dt>

<span id="_1079__Fatal___fileName___line____OBJECT-TYPE__name__is_an_extra_child_of_OBJECT-TYPE__name__of_module__name__"></span><span id="_1079__fatal___filename___line____object-type__name__is_an_extra_child_of_object-type__name__of_module__name__"></span><span id="_1079__FATAL___FILENAME___LINE____OBJECT-TYPE__NAME__IS_AN_EXTRA_CHILD_OF_OBJECT-TYPE__NAME__OF_MODULE__NAME__"></span>**<1079,> irreversibile: "fileName>: <line \#>: Object-Type <name> è un elemento figlio aggiuntivo di Object-Type <name> di module <name> "**
</dt> <dd>

Errore semantico del modulo di chiamata macro del **tipo di oggetto** . Ogni sequenza di oggetti deve avere esattamente un elemento figlio.

Questo errore può verificarsi in SNMPv1 o SNMPv2C.

</dd> </dl>

## <a name="warning-1080"></a>Avviso 1080

<dl> <dt>

<span id="_1080__Warning_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1080__warning_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1080__WARNING_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1080, avviso>: " <fileName><riga \#>: modulo MIB <moduleName> , da cui <symbolName> viene importato il simbolo, non è presente nell'input"**
</dt> <dd>

Avviso semantico del modulo relativo al riferimento incrociato, specifico di SNMPv1 o SNMPv2C. Se uno dei moduli nella sezione Imports del modulo principale o di un modulo sussidiario non esiste, ma non viene fatto riferimento a simboli da questo modulo, viene visualizzato questo avviso.

</dd> </dl>

 

 



