---
description: La tabella AppSearch contiene le proprietà necessarie per cercare un file con una particolare firma del file. La tabella AppSearch può essere utilizzata anche per impostare una proprietà sul valore esistente di una voce del registro di sistema o di un file ini.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: Tabella AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227211"
---
# <a name="appsearch-table"></a><span data-ttu-id="2d95c-104">Tabella AppSearch</span><span class="sxs-lookup"><span data-stu-id="2d95c-104">AppSearch Table</span></span>

<span data-ttu-id="2d95c-105">La tabella AppSearch contiene le proprietà necessarie per cercare un file con una particolare firma del file.</span><span class="sxs-lookup"><span data-stu-id="2d95c-105">The AppSearch table contains properties needed to search for a file having a particular file signature.</span></span> <span data-ttu-id="2d95c-106">La tabella AppSearch può essere utilizzata anche per impostare una proprietà sul valore esistente di una voce del registro di sistema o di un file ini.</span><span class="sxs-lookup"><span data-stu-id="2d95c-106">The AppSearch table can also be used to set a property to the existing value of a registry or .ini file entry.</span></span>

<span data-ttu-id="2d95c-107">La tabella AppSearch include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="2d95c-107">The AppSearch table has the following columns.</span></span>



| <span data-ttu-id="2d95c-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="2d95c-108">Column</span></span>      | <span data-ttu-id="2d95c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d95c-109">Type</span></span>                         | <span data-ttu-id="2d95c-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="2d95c-110">Key</span></span> | <span data-ttu-id="2d95c-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="2d95c-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="2d95c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d95c-112">Property</span></span>    | [<span data-ttu-id="2d95c-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="2d95c-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="2d95c-114">S</span><span class="sxs-lookup"><span data-stu-id="2d95c-114">Y</span></span>   | <span data-ttu-id="2d95c-115">N</span><span class="sxs-lookup"><span data-stu-id="2d95c-115">N</span></span>        |
| <span data-ttu-id="2d95c-116">Firma\_</span><span class="sxs-lookup"><span data-stu-id="2d95c-116">Signature\_</span></span> | [<span data-ttu-id="2d95c-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="2d95c-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="2d95c-118">S</span><span class="sxs-lookup"><span data-stu-id="2d95c-118">Y</span></span>   | <span data-ttu-id="2d95c-119">N</span><span class="sxs-lookup"><span data-stu-id="2d95c-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2d95c-120">Colonne</span><span class="sxs-lookup"><span data-stu-id="2d95c-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2d95c-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d95c-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="2d95c-122">Eseguendo l'azione [AppSearch](appsearch-action.md) , questa proprietà viene impostata sul percorso del file indicato dalla colonna Signature \_ .</span><span class="sxs-lookup"><span data-stu-id="2d95c-122">Running the [AppSearch](appsearch-action.md) action sets this property to the location of the file indicated by the Signature\_ column.</span></span> <span data-ttu-id="2d95c-123">Questa proprietà viene impostata se la firma del file esiste nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2d95c-123">This property is set if the file signature exists on the user's computer.</span></span> <span data-ttu-id="2d95c-124">Le proprietà usate in questa colonna devono essere proprietà [pubbliche](public-properties.md) e avere un identificatore che non contiene lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="2d95c-124">The properties used in this column must be [public](public-properties.md) properties and have an identifier that contains no lowercase letters.</span></span>

<span data-ttu-id="2d95c-125">La proprietà elencata nel campo della proprietà può essere inizializzata nella tabella delle [Proprietà](property-table.md) o da una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="2d95c-125">The property listed in the Property field may be initialized in the [Property](property-table.md) table or from a command line.</span></span> <span data-ttu-id="2d95c-126">Se l'azione [AppSearch](appsearch-action.md) individua la firma, il programma di installazione esegue l'override del valore della proprietà inizializzata con il valore trovato.</span><span class="sxs-lookup"><span data-stu-id="2d95c-126">If the [AppSearch](appsearch-action.md) action locates the signature, the installer overrides the initialized property value with the found value.</span></span> <span data-ttu-id="2d95c-127">Se la firma non viene trovata, viene usato il valore iniziale della proprietà.</span><span class="sxs-lookup"><span data-stu-id="2d95c-127">If the signature is not found, then the initial property value is used.</span></span> <span data-ttu-id="2d95c-128">Se la proprietà non è mai stata inizializzata, la proprietà verrà impostata solo se la firma viene trovata.</span><span class="sxs-lookup"><span data-stu-id="2d95c-128">If the property was never initialized, then the property will only be set if the signature is found.</span></span> <span data-ttu-id="2d95c-129">In caso contrario, la proprietà non è definita.</span><span class="sxs-lookup"><span data-stu-id="2d95c-129">Otherwise, the property is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="2d95c-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_</span><span class="sxs-lookup"><span data-stu-id="2d95c-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="2d95c-131">La colonna della firma \_ contiene un identificatore univoco denominato firma ed è anche una chiave esterna nelle tabelle [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)e [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2d95c-131">The Signature\_ column contains a unique identifier called a signature and is also an external key into the [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span> <span data-ttu-id="2d95c-132">Quando si cerca un file, anche il valore in questa colonna deve essere una chiave esterna nella tabella della [firma](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2d95c-132">When searching for a file, the value in this column must also be a foreign key into the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="2d95c-133">Se il valore di questa colonna non è elencato nella tabella della firma, il programma di installazione determina che la ricerca è relativa a una directory.</span><span class="sxs-lookup"><span data-stu-id="2d95c-133">If the value in this column is not listed in the Signature table, the installer determines that the search is for a directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d95c-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d95c-134">Remarks</span></span>

<span data-ttu-id="2d95c-135">L'azione [AppSearch](appsearch-action.md) nelle [*tabelle Sequence*](s-gly.md) elabora le informazioni contenute in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="2d95c-135">The [AppSearch](appsearch-action.md) action in [*sequence tables*](s-gly.md) processes the information in this table.</span></span> <span data-ttu-id="2d95c-136">Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2d95c-136">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="2d95c-137">L'azione [AppSearch](appsearch-action.md) Cerca le firme usando prima la tabella [CompLocator](complocator-table.md) , il secondo della tabella [RegLocator](reglocator-table.md) , la terza tabella [IniLocator](inilocator-table.md) e infine la tabella [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2d95c-137">The [AppSearch](appsearch-action.md) action searches for signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table second, the [IniLocator](inilocator-table.md) table third, and finally the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="2d95c-138">Le firme dei file sono elencate nella tabella della [firma](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2d95c-138">File signatures are listed in the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="2d95c-139">Una firma che non è presente nella tabella delle firme indica una directory e l'azione imposta la proprietà sul percorso di directory per la firma.</span><span class="sxs-lookup"><span data-stu-id="2d95c-139">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="2d95c-140">Vedere [ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="2d95c-140">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="2d95c-141">Convalida</span><span class="sxs-lookup"><span data-stu-id="2d95c-141">Validation</span></span>

<dl>

[<span data-ttu-id="2d95c-142">ICE03</span><span class="sxs-lookup"><span data-stu-id="2d95c-142">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2d95c-143">ICE06</span><span class="sxs-lookup"><span data-stu-id="2d95c-143">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2d95c-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="2d95c-144">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="2d95c-145">ICE52</span><span class="sxs-lookup"><span data-stu-id="2d95c-145">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="2d95c-146">ICE88</span><span class="sxs-lookup"><span data-stu-id="2d95c-146">ICE88</span></span>](ice88.md)  
</dl>

 

 



