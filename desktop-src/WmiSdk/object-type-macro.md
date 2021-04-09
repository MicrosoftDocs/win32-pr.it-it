---
description: La macro di tipo oggetto contiene clausole obbligatorie e facoltative che descrivono le caratteristiche di base di un oggetto MIB. Il provider SNMP converte un MIB nelle parti corrispondenti della macro del tipo di oggetto.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Macro di tipo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128078"
---
# <a name="object-type-macro"></a><span data-ttu-id="1ce8f-104">Macro di tipo oggetto</span><span class="sxs-lookup"><span data-stu-id="1ce8f-104">OBJECT-TYPE Macro</span></span>

<span data-ttu-id="1ce8f-105">La macro di tipo oggetto contiene clausole obbligatorie e facoltative che descrivono le caratteristiche di base di un oggetto MIB.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-105">The OBJECT-TYPE macro contains mandatory and optional clauses that describe the basic characteristics of a MIB object.</span></span> <span data-ttu-id="1ce8f-106">Il provider SNMP converte un MIB nelle parti corrispondenti della macro del tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-106">The SNMP Provider converts an MIB to the corresponding parts of the OBJECT-TYPE macro.</span></span>

> [!Note]  
> <span data-ttu-id="1ce8f-107">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1ce8f-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="1ce8f-108">Componenti</span><span class="sxs-lookup"><span data-stu-id="1ce8f-108">Components</span></span>

<dl> <dt>

<span data-ttu-id="1ce8f-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>Oggetto MIB</span><span class="sxs-lookup"><span data-stu-id="1ce8f-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB object</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-110">Oggetto che contiene la maggior parte dei dati in questione.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-110">Object that contains most of the data in question.</span></span>

</dd> <dt>

<span data-ttu-id="1ce8f-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descrittore di oggetto</span><span class="sxs-lookup"><span data-stu-id="1ce8f-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-112">Nome univoco o descrittore di oggetto che identifica ogni oggetto MIB.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-112">Unique name or object descriptor identifying each MIB object.</span></span> <span data-ttu-id="1ce8f-113">Ogni descrittore di oggetti MIB viene mappato esattamente a un nome di proprietà CIM.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-113">Each MIB object descriptor maps exactly to a CIM property name.</span></span> <span data-ttu-id="1ce8f-114">Ad esempio, **ifindex** viene convertito in **ifindex**.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-114">For example, **ifIndex** translates to **ifIndex**.</span></span>

</dd> <dt>

<span data-ttu-id="1ce8f-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Clausola SYNTAX](syntax-clause.md)</span><span class="sxs-lookup"><span data-stu-id="1ce8f-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[SYNTAX Clause](syntax-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-116">Definisce i dati e il tipo di un oggetto MIB.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-116">Defines the data and type of an MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="1ce8f-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[Clausola INDEX](index-clause.md)</span><span class="sxs-lookup"><span data-stu-id="1ce8f-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX clause](index-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-118">Definisce una chiave per la selezione di una riga di tabella univoca.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-118">Defines a key for selecting a unique table row.</span></span>

</dd> <dt>

<span data-ttu-id="1ce8f-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>Clausola AUGMENTs</span><span class="sxs-lookup"><span data-stu-id="1ce8f-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>AUGMENTS clause</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-120">Indica che la raccolta di tabelle specificata può essere considerata un'estensione di un'altra raccolta di tabelle e può sostituire la clausola INDEX in SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-120">Indicates that the table collection it specifies can be considered an extension of another table collection, and can replace the INDEX clause in SNMPv2.</span></span> <span data-ttu-id="1ce8f-121">Le raccolte a cui fa riferimento la clausola AUGMENTs possono essere combinate con l'altra raccolta di tabelle per formare una raccolta.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-121">The collections referred to by the AUGMENTS clause can be combined with the other table collection to form one collection.</span></span> <span data-ttu-id="1ce8f-122">La raccolta risultante condivide le proprietà della chiave primaria specificate nell'ultima raccolta di tabelle nella catena.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-122">The resulting collection shares the primary key properties specified in the last table collection in the chain.</span></span>

<span data-ttu-id="1ce8f-123">In questo caso, le regole di mapping precedenti specificate per la clausola INDEX vengono applicate all'ultima raccolta di tabelle nella catena.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-123">In this case, the previous mapping rules specified for the INDEX clause are applied to the last table collection in the chain.</span></span> <span data-ttu-id="1ce8f-124">La raccolta di oggetti viene quindi mappata a una definizione di classe CIM.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-124">The collection of objects then maps to one CIM class definition.</span></span>

</dd> <dt>

<span data-ttu-id="1ce8f-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>Clausola dell'identificatore di oggetto</span><span class="sxs-lookup"><span data-stu-id="1ce8f-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>OBJECT-IDENTIFIER clause</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-126">Contiene un identificatore di oggetto univoco per un oggetto MIB.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-126">Contains a unique object identifier for an MIB object.</span></span> <span data-ttu-id="1ce8f-127">Questo identificatore di oggetto esegue il mapping all' **\_ identificatore di oggetto** qualificatore della proprietà CIM.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-127">This object identifier maps to the CIM property qualifier **object\_identifier**.</span></span>

</dd> <dt>

<span data-ttu-id="1ce8f-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Clausole ACCESS e MAX-ACCESS](access-and-max-access-clauses.md)</span><span class="sxs-lookup"><span data-stu-id="1ce8f-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[ACCESS and MAX-ACCESS Clauses](access-and-max-access-clauses.md)</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-129">Definire i diritti di accesso all'oggetto MIB.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-129">Define the access rights to the MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="1ce8f-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Clausola DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1ce8f-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-131">Fornisce una descrizione di testo dell'oggetto, che esegue il mapping alla **Descrizione** del qualificatore della proprietà CIM.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-131">Provides a text description of the object, which maps to the CIM property qualifier **Description**.</span></span> <span data-ttu-id="1ce8f-132">Questa clausola può essere vuota.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-132">This clause may be empty.</span></span>

<span data-ttu-id="1ce8f-133">Ogni oggetto **Table** e **entry** in una definizione di tabella SNMP contiene anche una clausola Description, che può anche essere vuota.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-133">Each **TABLE** and **ENTRY** object in an SNMP table definition also contains a DESCRIPTION clause, which also may be empty.</span></span> <span data-ttu-id="1ce8f-134">Le clausole della descrizione della tabella e della voce sono concatenate e il risultato viene mappato alla **Descrizione** del qualificatore della classe CIM.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-134">The TABLE and ENTRY DESCRIPTION clauses are concatenated and the result maps to the CIM class qualifier **Description**.</span></span>

</dd> <dt>

<span data-ttu-id="1ce8f-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Clausola STATUS</span><span class="sxs-lookup"><span data-stu-id="1ce8f-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-136">Indica se l'oggetto deve essere supportato.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-136">Indicates whether the object must be supported.</span></span> <span data-ttu-id="1ce8f-137">Quando il valore della clausola STATUS è **obsoleto**, il provider elimina l'oggetto MIB dal mapping.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-137">When the value of the STATUS clause is **obsolete**, the provider discards the MIB object from the mapping.</span></span> <span data-ttu-id="1ce8f-138">In caso contrario, la clausola STATUS viene mappata allo **stato** del qualificatore della proprietà CIM.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-138">Otherwise, the STATUS clause maps to the CIM property qualifier **Status**.</span></span>

<span data-ttu-id="1ce8f-139">Per SNMPv1, il valore preferito dello **stato** è **obbligatorio** o **facoltativo**, ma il qualificatore può contenere un altro valore.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-139">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="1ce8f-140">Per SNMPv2C, il valore preferito dello **stato** è **Current** o **deprecato**, ma il qualificatore può contenere un altro valore.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-140">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> <dt>

<span data-ttu-id="1ce8f-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>Clausola DEFVAL</span><span class="sxs-lookup"><span data-stu-id="1ce8f-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL clause</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-142">Assegna un valore predefinito a una variabile in una riga della tabella logica ed esegue il mapping al qualificatore di proprietà CIM della stringa **DEFVAL**.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-142">Assigns a default value to a variable in a logical table row, and maps to the string CIM property qualifier **Defval**.</span></span>

</dd> <dt>

<span data-ttu-id="1ce8f-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Clausola REFERENCE</span><span class="sxs-lookup"><span data-stu-id="1ce8f-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-144">Fa riferimento a un altro documento che contiene ulteriori informazioni sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-144">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="1ce8f-145">Questa clausola esegue il mapping al **riferimento** al qualificatore di proprietà CIM, che è di tipo String.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-145">This clause maps to the CIM property qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="1ce8f-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>Clausola UNITs</span><span class="sxs-lookup"><span data-stu-id="1ce8f-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>UNITS clause</span></span>
</dt> <dd>

<span data-ttu-id="1ce8f-147">Fornisce una definizione precisa degli elementi rappresentati dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-147">Provides a precise definition of what the object represents.</span></span> <span data-ttu-id="1ce8f-148">Questa clausola esegue il mapping alle **unità** del qualificatore di proprietà CIM, che è di tipo String.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-148">This clause maps to the CIM property qualifier **Units**, which is of type string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ce8f-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ce8f-149">Remarks</span></span>

<span data-ttu-id="1ce8f-150">La macro di tipo oggetto descrive le caratteristiche di base di un singolo oggetto MIB.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-150">The OBJECT-TYPE macro describes the basic characteristics of an individual MIB object.</span></span> <span data-ttu-id="1ce8f-151">Un set di macro di tipo oggetto può essere considerato un gruppo di oggetti correlati.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-151">A set of OBJECT-TYPE macros can be considered as a group of related objects.</span></span> <span data-ttu-id="1ce8f-152">In SNMPv2C utilizzare la macro del gruppo di oggetti per raggruppare in modo formale i set di oggetti correlati in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-152">In SNMPv2C, use the OBJECT-GROUP macro to formally group sets of related objects into a collection.</span></span> <span data-ttu-id="1ce8f-153">Tuttavia, non esiste un meccanismo formale per la creazione di raccolte in SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-153">However, there is no formal mechanism for creating collections in SNMPv1.</span></span> <span data-ttu-id="1ce8f-154">Ai fini del provider SNMP, la macro del gruppo di oggetti viene ignorata, ma è possibile inventare relazioni di raggruppamento e creare raccolte di infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="1ce8f-154">For the purposes of the SNMP Provider, the OBJECT-GROUP macro is ignored, but you can invent grouping relationships and fabricate collections.</span></span>

 

 



