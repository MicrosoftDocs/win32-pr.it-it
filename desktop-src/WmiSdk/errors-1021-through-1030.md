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
# <a name="errors-1021-through-1030"></a><span data-ttu-id="d9b27-103">Errori da 1021 a 1030</span><span class="sxs-lookup"><span data-stu-id="d9b27-103">Errors 1021 through 1030</span></span>

<span data-ttu-id="d9b27-104">Descrive gli errori del provider SNMP WMI da 1021 a 1033.</span><span class="sxs-lookup"><span data-stu-id="d9b27-104">Describes WMI SNMP provider errors 1021 through 1033.</span></span>

[<span data-ttu-id="d9b27-105">Errore irreversibile 1021</span><span class="sxs-lookup"><span data-stu-id="d9b27-105">Fatal Error 1021</span></span>](#fatal-error-1021)

[<span data-ttu-id="d9b27-106">Errore irreversibile 1022</span><span class="sxs-lookup"><span data-stu-id="d9b27-106">Fatal Error 1022</span></span>](#fatal-error-1022)

[<span data-ttu-id="d9b27-107">Errore irreversibile 1023</span><span class="sxs-lookup"><span data-stu-id="d9b27-107">Fatal Error 1023</span></span>](#fatal-error-1023)

[<span data-ttu-id="d9b27-108">Errore irreversibile 1024</span><span class="sxs-lookup"><span data-stu-id="d9b27-108">Fatal Error 1024</span></span>](#fatal-error-1024)

[<span data-ttu-id="d9b27-109">Errore irreversibile 1025</span><span class="sxs-lookup"><span data-stu-id="d9b27-109">Fatal Error 1025</span></span>](#fatal-error-1025)

[<span data-ttu-id="d9b27-110">Errore irreversibile 1026</span><span class="sxs-lookup"><span data-stu-id="d9b27-110">Fatal Error 1026</span></span>](#fatal-error-1026)

[<span data-ttu-id="d9b27-111">Avviso 1027</span><span class="sxs-lookup"><span data-stu-id="d9b27-111">Warning 1027</span></span>](#warning-1027)

[<span data-ttu-id="d9b27-112">Errore irreversibile 1028</span><span class="sxs-lookup"><span data-stu-id="d9b27-112">Fatal Error 1028</span></span>](#fatal-error-1028)

[<span data-ttu-id="d9b27-113">Errore irreversibile 1029</span><span class="sxs-lookup"><span data-stu-id="d9b27-113">Fatal Error 1029</span></span>](#fatal-error-1029)

[<span data-ttu-id="d9b27-114">Errore irreversibile 1030</span><span class="sxs-lookup"><span data-stu-id="d9b27-114">Fatal Error 1030</span></span>](#fatal-error-1030)

## <a name="fatal-error-1021"></a><span data-ttu-id="d9b27-115">Errore irreversibile 1021</span><span class="sxs-lookup"><span data-stu-id="d9b27-115">Fatal Error 1021</span></span>

<dl> <dt>

<span data-ttu-id="d9b27-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021,> irreversibile: " <fileName><riga \#>: <identifier> l'identificatore nella clausola Variables di trap-type non viene risolto in un tipo di oggetto scalare"**</span><span class="sxs-lookup"><span data-stu-id="d9b27-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, Fatal>: "<fileName><line\#>: Identifier <identifier> in the VARIABLES clause of TRAP-TYPE does not resolve to a scalar OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="d9b27-117">Chiamata della macro di **tipo trap** , errore semantico del modulo specifico di SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="d9b27-117">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="d9b27-118">Ogni elemento nell'elenco di variabili utilizzato nella clausola VARIABLES di una chiamata a una macro di **tipo trap** deve risolvere il nome di un'istanza scalare di tipo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d9b27-118">Each item in the list of variables used in the VARIABLES clause of a **TRAP-TYPE** macro invocation must resolve to the name of a scalar OBJECT-TYPE instance.</span></span>

</dd> </dl>

## <a name="fatal-error-1022"></a><span data-ttu-id="d9b27-119">Errore irreversibile 1022</span><span class="sxs-lookup"><span data-stu-id="d9b27-119">Fatal Error 1022</span></span>

<dl> <dt>

<span data-ttu-id="d9b27-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022,> irreversibile: " <fileName><riga \#>: il valore non viene risolto nel tipo <type> "**</span><span class="sxs-lookup"><span data-stu-id="d9b27-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, Fatal>: "<fileName><line\#>: Value does not resolve to type <type>"**</span></span>
</dt> <dd>

<span data-ttu-id="d9b27-121">Errore semantico del modulo di assegnazione valore, specifico di SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d9b27-121">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d9b27-122">Il tipo errato del valore del RHS di un'assegnazione di valore INTEGER, **null**, stringa ottetto o identificatore di oggetto non è corretto.</span><span class="sxs-lookup"><span data-stu-id="d9b27-122">The value on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment is of the wrong type.</span></span>

</dd> </dl>

## <a name="fatal-error-1023"></a><span data-ttu-id="d9b27-123">Errore irreversibile 1023</span><span class="sxs-lookup"><span data-stu-id="d9b27-123">Fatal Error 1023</span></span>

<dl> <dt>

<span data-ttu-id="d9b27-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023,> irreversibile: " <fileName><riga \#>: <identifier> l'identificatore non viene risolto nel tipo <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="d9b27-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to the type <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="d9b27-125">Errore semantico del modulo di assegnazione valore, specifico di SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d9b27-125">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d9b27-126">Un simbolo (riferimento al valore) nel RHS di un'assegnazione di valore INTEGER, **null**, stringa ottetto o identificatore di oggetto non viene risolto nel tipo corretto.</span><span class="sxs-lookup"><span data-stu-id="d9b27-126">A symbol (value reference) on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment does not resolve to the right type.</span></span>

</dd> </dl>

## <a name="fatal-error-1024"></a><span data-ttu-id="d9b27-127">Errore irreversibile 1024</span><span class="sxs-lookup"><span data-stu-id="d9b27-127">Fatal Error 1024</span></span>

<dl> <dt>

<span data-ttu-id="d9b27-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024,> irreversibile: " <fileName><riga \#>: numero intero negativo nella definizione del valore OID"**</span><span class="sxs-lookup"><span data-stu-id="d9b27-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, Fatal>: "<fileName><line\#>: Negative integer in OID value definition"**</span></span>
</dt> <dd>

<span data-ttu-id="d9b27-129">Errore semantico del modulo di assegnazione valore, specifico di SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d9b27-129">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d9b27-130">Tutti i valori in un elenco di componenti OID devono essere numeri interi non negativi (preferibilmente positivi).</span><span class="sxs-lookup"><span data-stu-id="d9b27-130">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1025"></a><span data-ttu-id="d9b27-131">Errore irreversibile 1025</span><span class="sxs-lookup"><span data-stu-id="d9b27-131">Fatal Error 1025</span></span>

<dl> <dt>

<span data-ttu-id="d9b27-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025,> irreversibile: " <identifier> l'identificatore nel valore OID non viene risolto in un numero intero positivo"**</span><span class="sxs-lookup"><span data-stu-id="d9b27-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, Fatal>: "Identifier <identifier> in OID value does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="d9b27-133">Errore semantico del modulo di assegnazione valore, specifico di SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d9b27-133">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d9b27-134">Tutti i valori in un elenco di componenti OID devono essere numeri interi non negativi (preferibilmente positivi).</span><span class="sxs-lookup"><span data-stu-id="d9b27-134">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1026"></a><span data-ttu-id="d9b27-135">Errore irreversibile 1026</span><span class="sxs-lookup"><span data-stu-id="d9b27-135">Fatal Error 1026</span></span>

<dl> <dt>

<span data-ttu-id="d9b27-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026,> irreversibile: " <fileName><riga \#>: <identifier> l'identificatore nel valore OID non viene risolto in un valore OID né in un numero intero positivo"**</span><span class="sxs-lookup"><span data-stu-id="d9b27-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, Fatal>: "<fileName><line\#>: Identifier <identifier> in OID value neither resolves to an OID value nor a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="d9b27-137">Errore semantico del modulo di assegnazione valore, specifico di SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d9b27-137">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d9b27-138">Il primo componente utilizzato in un valore OID deve essere risolto in un valore OID o un numero intero.</span><span class="sxs-lookup"><span data-stu-id="d9b27-138">The first component used in an OID value must resolve to an OID value or an INTEGER.</span></span>

</dd> </dl>

## <a name="warning-1027"></a><span data-ttu-id="d9b27-139">Avviso 1027</span><span class="sxs-lookup"><span data-stu-id="d9b27-139">Warning 1027</span></span>

<dl> <dt>

<span data-ttu-id="d9b27-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, avviso>: " <fileName><riga \#>: simbolo importato non <identifier> usato"**</span><span class="sxs-lookup"><span data-stu-id="d9b27-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, Warning>: "<fileName><line\#>: Imported symbol <identifier> unused"**</span></span>
</dt> <dd>

<span data-ttu-id="d9b27-141">Avviso semantico del modulo della sezione Imports, specifico di SNMPv1 e SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d9b27-141">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d9b27-142">Viene emesso un avviso per ogni simbolo importato inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="d9b27-142">A warning is issued for every unused imported symbol.</span></span>

</dd> </dl>

## <a name="fatal-error-1028"></a><span data-ttu-id="d9b27-143">Errore irreversibile 1028</span><span class="sxs-lookup"><span data-stu-id="d9b27-143">Fatal Error 1028</span></span>

<dl> <dt>

<span data-ttu-id="d9b27-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028,> irreversibile: "modulo <identifier> non importato nella sezione IMports"**</span><span class="sxs-lookup"><span data-stu-id="d9b27-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, Fatal>: "Module <identifier> not imported in the IMPORTS section"**</span></span>
</dt> <dd>

<span data-ttu-id="d9b27-145">Errore semantico del modulo della sezione Imports, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d9b27-145">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d9b27-146">Il nome di un modulo usato per fare riferimento a un simbolo deve essere presente nella clausola Imports oppure corrispondere al nome del modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="d9b27-146">A module name used in referencing a symbol must either be present in the IMPORTS clause, or be the name of the current module.</span></span>

</dd> </dl>

## <a name="fatal-error-1029"></a><span data-ttu-id="d9b27-147">Errore irreversibile 1029</span><span class="sxs-lookup"><span data-stu-id="d9b27-147">Fatal Error 1029</span></span>

<dl> <dt>

<span data-ttu-id="d9b27-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029,> irreversibile: " <fileName><riga \#>: Impossibile importare il modulo corrente <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="d9b27-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, Fatal>: "<fileName><line\#>: Current module <identifier> cannot be imported"**</span></span>
</dt> <dd>

<span data-ttu-id="d9b27-149">Errore semantico del modulo della sezione Imports, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d9b27-149">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d9b27-150">Il nome del modulo corrente è anche costituito da figure nell'elenco Imports.</span><span class="sxs-lookup"><span data-stu-id="d9b27-150">The name of the current module also figures in the IMPORTS list.</span></span>

</dd> </dl>

## <a name="fatal-error-1030"></a><span data-ttu-id="d9b27-151">Errore irreversibile 1030</span><span class="sxs-lookup"><span data-stu-id="d9b27-151">Fatal Error 1030</span></span>

<dl> <dt>

<span data-ttu-id="d9b27-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030,> irreversibile: " <fileName><riga \#>: il simbolo non è stato <identifier> importato dal modulo <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="d9b27-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, Fatal>:"<fileName><line\#>: Symbol <identifier> not imported from Module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="d9b27-153">Errore semantico del modulo della sezione Imports, specifico di SNMPv1 o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d9b27-153">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d9b27-154">È stata usata la notazione "Module. symbol", ma il simbolo non è stato importato dal modulo specificato nella sezione Imports.</span><span class="sxs-lookup"><span data-stu-id="d9b27-154">You have used the "Module.Symbol" notation, but the symbol has not been imported from the specified module in the IMPORTS section.</span></span>

</dd> </dl>

 

 



