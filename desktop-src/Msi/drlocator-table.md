---
description: La tabella DrLocator contiene le informazioni necessarie per trovare un file o una directory eseguendo una ricerca nell'albero di directory.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Tabella DrLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308193"
---
# <a name="drlocator-table"></a><span data-ttu-id="01a0e-103">Tabella DrLocator</span><span class="sxs-lookup"><span data-stu-id="01a0e-103">DrLocator Table</span></span>

<span data-ttu-id="01a0e-104">La tabella DrLocator contiene le informazioni necessarie per trovare un file o una directory eseguendo una ricerca nell'albero di directory.</span><span class="sxs-lookup"><span data-stu-id="01a0e-104">The DrLocator table holds the information needed to find a file or directory by searching the directory tree.</span></span>

<span data-ttu-id="01a0e-105">La tabella DrLocator include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="01a0e-105">The DrLocator table has the following columns.</span></span>



| <span data-ttu-id="01a0e-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="01a0e-106">Column</span></span>      | <span data-ttu-id="01a0e-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="01a0e-107">Type</span></span>                         | <span data-ttu-id="01a0e-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="01a0e-108">Key</span></span> | <span data-ttu-id="01a0e-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="01a0e-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="01a0e-110">Firma\_</span><span class="sxs-lookup"><span data-stu-id="01a0e-110">Signature\_</span></span> | [<span data-ttu-id="01a0e-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="01a0e-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="01a0e-112">S</span><span class="sxs-lookup"><span data-stu-id="01a0e-112">Y</span></span>   | <span data-ttu-id="01a0e-113">N</span><span class="sxs-lookup"><span data-stu-id="01a0e-113">N</span></span>        |
| <span data-ttu-id="01a0e-114">Padre</span><span class="sxs-lookup"><span data-stu-id="01a0e-114">Parent</span></span>      | [<span data-ttu-id="01a0e-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="01a0e-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="01a0e-116">S</span><span class="sxs-lookup"><span data-stu-id="01a0e-116">Y</span></span>   | <span data-ttu-id="01a0e-117">S</span><span class="sxs-lookup"><span data-stu-id="01a0e-117">Y</span></span>        |
| <span data-ttu-id="01a0e-118">Percorso</span><span class="sxs-lookup"><span data-stu-id="01a0e-118">Path</span></span>        | [<span data-ttu-id="01a0e-119">AnyPath</span><span class="sxs-lookup"><span data-stu-id="01a0e-119">AnyPath</span></span>](anypath.md)       | <span data-ttu-id="01a0e-120">S</span><span class="sxs-lookup"><span data-stu-id="01a0e-120">Y</span></span>   | <span data-ttu-id="01a0e-121">S</span><span class="sxs-lookup"><span data-stu-id="01a0e-121">Y</span></span>        |
| <span data-ttu-id="01a0e-122">Profondità</span><span class="sxs-lookup"><span data-stu-id="01a0e-122">Depth</span></span>       | [<span data-ttu-id="01a0e-123">Integer</span><span class="sxs-lookup"><span data-stu-id="01a0e-123">Integer</span></span>](integer.md)       | <span data-ttu-id="01a0e-124">N</span><span class="sxs-lookup"><span data-stu-id="01a0e-124">N</span></span>   | <span data-ttu-id="01a0e-125">S</span><span class="sxs-lookup"><span data-stu-id="01a0e-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="01a0e-126">Colonne</span><span class="sxs-lookup"><span data-stu-id="01a0e-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="01a0e-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_</span><span class="sxs-lookup"><span data-stu-id="01a0e-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="01a0e-128">La \_ colonna Signature è una chiave esterna per la prima colonna della [tabella Signature](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="01a0e-128">The Signature\_ column is an external key to the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="01a0e-129">Questo campo può rappresentare una firma del file univoca elencata nella tabella della firma.</span><span class="sxs-lookup"><span data-stu-id="01a0e-129">This field may represent a unique file signature listed in the Signature table.</span></span> <span data-ttu-id="01a0e-130">Se il valore in questa colonna è assente dalla tabella di firma, si presuppone che la ricerca sia per una directory a cui punta la tabella DrLocator.</span><span class="sxs-lookup"><span data-stu-id="01a0e-130">If the value in this column is absent from the Signature table, then the search is assumed to be for a directory pointed to by the DrLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="01a0e-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Padre</span><span class="sxs-lookup"><span data-stu-id="01a0e-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Parent</span></span>
</dt> <dd>

<span data-ttu-id="01a0e-132">Questa colonna è la firma della directory padre del file o della directory nella \_ colonna firma.</span><span class="sxs-lookup"><span data-stu-id="01a0e-132">This column is the signature of the parent directory of the file or directory in the Signature\_ column.</span></span> <span data-ttu-id="01a0e-133">Se questo campo è null e la colonna Path non si espande in un percorso completo, viene eseguita la ricerca in tutte le unità fisse del sistema dell'utente usando il percorso.</span><span class="sxs-lookup"><span data-stu-id="01a0e-133">If this field is null, and the Path column does not expand to a full path, then all the fixed drives of the user's system are searched by using the Path.</span></span>

<span data-ttu-id="01a0e-134">Questo campo è una chiave in una delle tabelle seguenti: [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)o DrLocator.</span><span class="sxs-lookup"><span data-stu-id="01a0e-134">This field is a key into one of the following tables: the [RegLocator](reglocator-table.md), the [IniLocator](inilocator-table.md), the [CompLocator](complocator-table.md), or the DrLocator tables.</span></span>

</dd> <dt>

<span data-ttu-id="01a0e-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Percorso</span><span class="sxs-lookup"><span data-stu-id="01a0e-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="01a0e-136">La colonna percorso contiene il percorso nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="01a0e-136">The Path column contains the path on the user's system.</span></span> <span data-ttu-id="01a0e-137">Si tratta di un percorso completo o di un sottopercorso relativo sotto la directory specificata nella colonna padre.</span><span class="sxs-lookup"><span data-stu-id="01a0e-137">This is a either a full path or a relative subpath below the directory specified in the Parent column.</span></span> <span data-ttu-id="01a0e-138">Vedere le restrizioni sul tipo di dati [AnyPath](anypath.md) .</span><span class="sxs-lookup"><span data-stu-id="01a0e-138">See the restrictions on the [AnyPath](anypath.md) data type.</span></span>

</dd> <dt>

<span data-ttu-id="01a0e-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Profondità</span><span class="sxs-lookup"><span data-stu-id="01a0e-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Depth</span></span>
</dt> <dd>

<span data-ttu-id="01a0e-140">Profondità sotto il percorso in cui il programma di installazione cerca il file o la directory specificata nella \_ colonna Signature.</span><span class="sxs-lookup"><span data-stu-id="01a0e-140">The depth below the path that the installer searches for the file or directory specified in the Signature\_ column.</span></span> <span data-ttu-id="01a0e-141">Il valore utilizzato nel campo Depth è basato su zero.</span><span class="sxs-lookup"><span data-stu-id="01a0e-141">The value used in the Depth field is based on zero.</span></span> <span data-ttu-id="01a0e-142">Se ad esempio il campo percorso è c:/Program Files/bin, la colonna Depth deve essere impostata su 0 o su un valore maggiore per rilevare un file che si trova all'interno del contenitore di cartelle.</span><span class="sxs-lookup"><span data-stu-id="01a0e-142">For example, if the Path field is c:/Program Files/bin, the Depth column must be set to 0 or greater, to detect a file located inside the folder bin.</span></span> <span data-ttu-id="01a0e-143">Se il campo Depth è vuoto, si presuppone che la profondità sia zero.</span><span class="sxs-lookup"><span data-stu-id="01a0e-143">If the Depth field is empty, the depth is assumed to be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01a0e-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="01a0e-144">Remarks</span></span>

<span data-ttu-id="01a0e-145">Questa tabella viene utilizzata con la [tabella AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="01a0e-145">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="01a0e-146">Generalmente, le colonne della tabella non sono localizzate.</span><span class="sxs-lookup"><span data-stu-id="01a0e-146">This table's columns are generally not localized.</span></span> <span data-ttu-id="01a0e-147">Se un autore decide di cercare i prodotti in più lingue, è necessario che nella tabella sia inclusa una voce separata per ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="01a0e-147">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="01a0e-148">Vedere [ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="01a0e-148">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="01a0e-149">Convalida</span><span class="sxs-lookup"><span data-stu-id="01a0e-149">Validation</span></span>

<dl>

[<span data-ttu-id="01a0e-150">ICE03</span><span class="sxs-lookup"><span data-stu-id="01a0e-150">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="01a0e-151">ICE06</span><span class="sxs-lookup"><span data-stu-id="01a0e-151">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="01a0e-152">ICE46</span><span class="sxs-lookup"><span data-stu-id="01a0e-152">ICE46</span></span>](ice46.md)  
</dl>

 

 



