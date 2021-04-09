---
description: La tabella ODBCAttribute contiene informazioni sugli attributi di driver e convertitori Open Database Connectivity (ODBC).
ms.assetid: 82fd83d4-22dd-4641-807b-d2b263918e4c
title: Tabella ODBCAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e76a52dd63bdc8eb969324f7891e7359be7caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130286"
---
# <a name="odbcattribute-table"></a><span data-ttu-id="b1bfa-103">Tabella ODBCAttribute</span><span class="sxs-lookup"><span data-stu-id="b1bfa-103">ODBCAttribute Table</span></span>

<span data-ttu-id="b1bfa-104">La tabella ODBCAttribute contiene informazioni sugli attributi di driver e convertitori Open Database Connectivity (ODBC).</span><span class="sxs-lookup"><span data-stu-id="b1bfa-104">The ODBCAttribute table contains information about the attributes of Open Database Connectivity (ODBC) drivers and translators.</span></span>

<span data-ttu-id="b1bfa-105">La tabella ODBCAttribute include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="b1bfa-105">The ODBCAttribute table has the following columns.</span></span>



| <span data-ttu-id="b1bfa-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="b1bfa-106">Column</span></span>    | <span data-ttu-id="b1bfa-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b1bfa-107">Type</span></span>                         | <span data-ttu-id="b1bfa-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="b1bfa-108">Key</span></span> | <span data-ttu-id="b1bfa-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="b1bfa-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="b1bfa-110">Driver\_</span><span class="sxs-lookup"><span data-stu-id="b1bfa-110">Driver\_</span></span>  | [<span data-ttu-id="b1bfa-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="b1bfa-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="b1bfa-112">S</span><span class="sxs-lookup"><span data-stu-id="b1bfa-112">Y</span></span>   | <span data-ttu-id="b1bfa-113">N</span><span class="sxs-lookup"><span data-stu-id="b1bfa-113">N</span></span>        |
| <span data-ttu-id="b1bfa-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="b1bfa-114">Attribute</span></span> | [<span data-ttu-id="b1bfa-115">Text</span><span class="sxs-lookup"><span data-stu-id="b1bfa-115">Text</span></span>](text.md)             | <span data-ttu-id="b1bfa-116">S</span><span class="sxs-lookup"><span data-stu-id="b1bfa-116">Y</span></span>   | <span data-ttu-id="b1bfa-117">N</span><span class="sxs-lookup"><span data-stu-id="b1bfa-117">N</span></span>        |
| <span data-ttu-id="b1bfa-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b1bfa-118">Value</span></span>     | [<span data-ttu-id="b1bfa-119">Formattato</span><span class="sxs-lookup"><span data-stu-id="b1bfa-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="b1bfa-120">N</span><span class="sxs-lookup"><span data-stu-id="b1bfa-120">N</span></span>   | <span data-ttu-id="b1bfa-121">S</span><span class="sxs-lookup"><span data-stu-id="b1bfa-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b1bfa-122">Colonne</span><span class="sxs-lookup"><span data-stu-id="b1bfa-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b1bfa-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Driver\_</span><span class="sxs-lookup"><span data-stu-id="b1bfa-123"><span id="Driver_"></span><span id="driver_"></span><span id="DRIVER_"></span>Driver\_</span></span>
</dt> <dd>

<span data-ttu-id="b1bfa-124">Nome del token interno per un driver.</span><span class="sxs-lookup"><span data-stu-id="b1bfa-124">Internal token name for a driver.</span></span> <span data-ttu-id="b1bfa-125">Chiave primaria per la tabella.</span><span class="sxs-lookup"><span data-stu-id="b1bfa-125">A primary key for the table.</span></span> <span data-ttu-id="b1bfa-126">Chiave esterna nella [tabella ODBCDriver](odbcdriver-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1bfa-126">A foreign key into the [ODBCDriver table](odbcdriver-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1bfa-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attributo</span><span class="sxs-lookup"><span data-stu-id="b1bfa-127"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="b1bfa-128">Nome dell'attributo del driver.</span><span class="sxs-lookup"><span data-stu-id="b1bfa-128">Name of the driver attribute.</span></span> <span data-ttu-id="b1bfa-129">Chiave primaria per la tabella.</span><span class="sxs-lookup"><span data-stu-id="b1bfa-129">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="b1bfa-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="b1bfa-130"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="b1bfa-131">Valore stringa localizzabile per l'attributo.</span><span class="sxs-lookup"><span data-stu-id="b1bfa-131">Localizable string value for attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1bfa-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1bfa-132">Remarks</span></span>

<span data-ttu-id="b1bfa-133">Le azioni [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="b1bfa-133">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="b1bfa-134">Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1bfa-134">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="b1bfa-135">Convalida</span><span class="sxs-lookup"><span data-stu-id="b1bfa-135">Validation</span></span>

<dl>

[<span data-ttu-id="b1bfa-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="b1bfa-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b1bfa-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="b1bfa-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b1bfa-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="b1bfa-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b1bfa-139">ICE46</span><span class="sxs-lookup"><span data-stu-id="b1bfa-139">ICE46</span></span>](ice46.md)  
</dl>

 

 



