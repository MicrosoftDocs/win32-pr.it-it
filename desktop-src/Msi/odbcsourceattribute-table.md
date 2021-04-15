---
description: La tabella ODBCSourceAttribute contiene informazioni sugli attributi delle origini dati.
ms.assetid: 8ee50fd7-507e-484f-9a16-de5449470562
title: Tabella ODBCSourceAttribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52dd9636ac19eae0fb3a9e41d1a1c8389753e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525771"
---
# <a name="odbcsourceattribute-table"></a><span data-ttu-id="f5924-103">Tabella ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="f5924-103">ODBCSourceAttribute Table</span></span>

<span data-ttu-id="f5924-104">La tabella ODBCSourceAttribute contiene informazioni sugli attributi delle origini dati.</span><span class="sxs-lookup"><span data-stu-id="f5924-104">The ODBCSourceAttribute table contains information about the attributes of data sources.</span></span>

<span data-ttu-id="f5924-105">La tabella ODBCSourceAttribute include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5924-105">The ODBCSourceAttribute table has the following columns.</span></span>



| <span data-ttu-id="f5924-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="f5924-106">Column</span></span>       | <span data-ttu-id="f5924-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5924-107">Type</span></span>                         | <span data-ttu-id="f5924-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="f5924-108">Key</span></span> | <span data-ttu-id="f5924-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="f5924-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="f5924-110">DataSource\_</span><span class="sxs-lookup"><span data-stu-id="f5924-110">DataSource\_</span></span> | [<span data-ttu-id="f5924-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="f5924-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="f5924-112">S</span><span class="sxs-lookup"><span data-stu-id="f5924-112">Y</span></span>   | <span data-ttu-id="f5924-113">N</span><span class="sxs-lookup"><span data-stu-id="f5924-113">N</span></span>        |
| <span data-ttu-id="f5924-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="f5924-114">Attribute</span></span>    | [<span data-ttu-id="f5924-115">Text</span><span class="sxs-lookup"><span data-stu-id="f5924-115">Text</span></span>](text.md)             | <span data-ttu-id="f5924-116">S</span><span class="sxs-lookup"><span data-stu-id="f5924-116">Y</span></span>   | <span data-ttu-id="f5924-117">N</span><span class="sxs-lookup"><span data-stu-id="f5924-117">N</span></span>        |
| <span data-ttu-id="f5924-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f5924-118">Value</span></span>        | [<span data-ttu-id="f5924-119">Formattato</span><span class="sxs-lookup"><span data-stu-id="f5924-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="f5924-120">N</span><span class="sxs-lookup"><span data-stu-id="f5924-120">N</span></span>   | <span data-ttu-id="f5924-121">S</span><span class="sxs-lookup"><span data-stu-id="f5924-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f5924-122">Colonne</span><span class="sxs-lookup"><span data-stu-id="f5924-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f5924-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_</span><span class="sxs-lookup"><span data-stu-id="f5924-123"><span id="DataSource_"></span><span id="datasource_"></span><span id="DATASOURCE_"></span>DataSource\_</span></span>
</dt> <dd>

<span data-ttu-id="f5924-124">Nome del token interno per l'origine dati.</span><span class="sxs-lookup"><span data-stu-id="f5924-124">Internal token name for data source.</span></span> <span data-ttu-id="f5924-125">Chiave primaria per la tabella.</span><span class="sxs-lookup"><span data-stu-id="f5924-125">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="f5924-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attributo</span><span class="sxs-lookup"><span data-stu-id="f5924-126"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="f5924-127">Nome dell'attributo dell'origine dati.</span><span class="sxs-lookup"><span data-stu-id="f5924-127">Name of data source attribute.</span></span> <span data-ttu-id="f5924-128">Chiave primaria per la tabella.</span><span class="sxs-lookup"><span data-stu-id="f5924-128">A primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="f5924-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="f5924-129"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="f5924-130">Valore stringa localizzabile per l'attributo.</span><span class="sxs-lookup"><span data-stu-id="f5924-130">The localizable string value for the attribute.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5924-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5924-131">Remarks</span></span>

<span data-ttu-id="f5924-132">Le azioni [InstallODBC](installodbc-action.md) e [RemoveODBC](removeodbc-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="f5924-132">The [InstallODBC](installodbc-action.md) and [RemoveODBC](removeodbc-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="f5924-133">Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f5924-133">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="f5924-134">Convalida</span><span class="sxs-lookup"><span data-stu-id="f5924-134">Validation</span></span>

<dl>

[<span data-ttu-id="f5924-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="f5924-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f5924-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="f5924-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f5924-137">ICE32</span><span class="sxs-lookup"><span data-stu-id="f5924-137">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f5924-138">ICE46</span><span class="sxs-lookup"><span data-stu-id="f5924-138">ICE46</span></span>](ice46.md)  
</dl>

 

 



