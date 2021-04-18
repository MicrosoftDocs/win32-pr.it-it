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
# <a name="errors-1061-through-1070"></a><span data-ttu-id="0e390-103">Errori da 1061 a 1070</span><span class="sxs-lookup"><span data-stu-id="0e390-103">Errors 1061 through 1070</span></span>

<span data-ttu-id="0e390-104">Descrive gli errori del provider SNMP WMI da 1061 a 1070.</span><span class="sxs-lookup"><span data-stu-id="0e390-104">Describes WMI SNMP provider errors 1061 through 1070.</span></span>

[<span data-ttu-id="0e390-105">Errore irreversibile 1063</span><span class="sxs-lookup"><span data-stu-id="0e390-105">Fatal Error 1063</span></span>](#fatal-error-1063)

[<span data-ttu-id="0e390-106">Errore irreversibile 1064</span><span class="sxs-lookup"><span data-stu-id="0e390-106">Fatal Error 1064</span></span>](#fatal-error-1064)

[<span data-ttu-id="0e390-107">Errore irreversibile 1070</span><span class="sxs-lookup"><span data-stu-id="0e390-107">Fatal Error 1070</span></span>](#fatal-error-1070)

## <a name="fatal-error-1063"></a><span data-ttu-id="0e390-108">Errore irreversibile 1063</span><span class="sxs-lookup"><span data-stu-id="0e390-108">Fatal Error 1063</span></span>

<dl> <dt>

<span data-ttu-id="0e390-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063,> irreversibile: " <fileName><riga \#>: il limite superiore della specifica di dimensione è inferiore al limite inferiore"**</span><span class="sxs-lookup"><span data-stu-id="0e390-109"><span id="_1063__Fatal_____fileName__line____Upper_bound_of_SIZE_specification_is_less_than_the_lower_bound_"></span><span id="_1063__fatal_____filename__line____upper_bound_of_size_specification_is_less_than_the_lower_bound_"></span><span id="_1063__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_SIZE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1063, Fatal>: "<fileName><line\#>: Upper bound of SIZE specification is less than the lower bound"**</span></span>
</dt> <dd>

<span data-ttu-id="0e390-110">Errore semantico del modulo nella specifica di dimensione, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="0e390-110">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="0e390-111">Il simbolo usato in una specifica di dimensione deve essere risolto in stringa ottetto o opaco.</span><span class="sxs-lookup"><span data-stu-id="0e390-111">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="0e390-112">Il limite inferiore di una specifica di intervallo o di dimensione non deve essere maggiore del limite superiore.</span><span class="sxs-lookup"><span data-stu-id="0e390-112">The lower bound of a range or SIZE specification must be no greater than the upper bound.</span></span>

</dd> </dl>

## <a name="fatal-error-1064"></a><span data-ttu-id="0e390-113">Errore irreversibile 1064</span><span class="sxs-lookup"><span data-stu-id="0e390-113">Fatal Error 1064</span></span>

<dl> <dt>

<span data-ttu-id="0e390-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064,> irreversibile: " <fileName> : <riga \#>: l'elemento sequenza non <identifier> viene risolto in un tipo di oggetto"**</span><span class="sxs-lookup"><span data-stu-id="0e390-114"><span id="_1064__Fatal_____fileName___line____SEQUENCE_item__identifier__does_not_resolve_to_an_OBJECT-TYPE_"></span><span id="_1064__fatal_____filename___line____sequence_item__identifier__does_not_resolve_to_an_object-type_"></span><span id="_1064__FATAL_____FILENAME___LINE____SEQUENCE_ITEM__IDENTIFIER__DOES_NOT_RESOLVE_TO_AN_OBJECT-TYPE_"></span>**<1064, Fatal>: "<fileName>:<line\#>: SEQUENCE item <identifier> does not resolve to an OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="0e390-115">Errore semantico del modulo di assegnazione del tipo, specifico di SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="0e390-115">Type assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="0e390-116">Tutti i singoli elementi di una dichiarazione di sequenza devono essere risolti in un tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e390-116">All of the individual elements of a SEQUENCE declaration must resolve to an OBJECT-TYPE.</span></span>

</dd> </dl>

## <a name="fatal-error-1070"></a><span data-ttu-id="0e390-117">Errore irreversibile 1070</span><span class="sxs-lookup"><span data-stu-id="0e390-117">Fatal Error 1070</span></span>

<dl> <dt>

<span data-ttu-id="0e390-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070,> irreversibile: " <fileName><riga \#>: modulo MIB <moduleName> , da cui <symbolName> viene importato il simbolo, non è presente nell'input"**</span><span class="sxs-lookup"><span data-stu-id="0e390-118"><span id="_1070__Fatal_____fileName__line____MIB_Module__moduleName___from_which_symbol__symbolName__is_imported__is_not_present_in_input_"></span><span id="_1070__fatal_____filename__line____mib_module__modulename___from_which_symbol__symbolname__is_imported__is_not_present_in_input_"></span><span id="_1070__FATAL_____FILENAME__LINE____MIB_MODULE__MODULENAME___FROM_WHICH_SYMBOL__SYMBOLNAME__IS_IMPORTED__IS_NOT_PRESENT_IN_INPUT_"></span>**<1070, Fatal>: "<fileName><line\#>: MIB Module <moduleName>, from which symbol <symbolName> is imported, is not present in input"**</span></span>
</dt> <dd>

<span data-ttu-id="0e390-119">Errore semantico del modulo nel riferimento incrociato, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="0e390-119">Module semantic error in cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="0e390-120">Se uno dei moduli nella sezione Imports del modulo principale o di un modulo sussidiario non esiste e viene fatto riferimento a uno o più simboli da questo modulo, si verifica questo errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="0e390-120">If one of the modules in the IMPORTS section of the main module or a subsidiary module does not exist and one or more symbols from this module are actually referenced, this fatal error occurs.</span></span>

</dd> </dl>

 

 



