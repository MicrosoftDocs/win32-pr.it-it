---
description: Durante un'installazione di Windows Installer, il programma di installazione può cercare una directory e un file in tale directory.
ms.assetid: ddf624f9-6f85-4ef6-8dfc-8635a25915d0
title: Ricerca di una directory e di un file nella directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4821a53ef0c3f063e943f1f5821b043791dd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313790"
---
# <a name="searching-for-a-directory-and-a-file-in-the-directory"></a><span data-ttu-id="8c249-103">Ricerca di una directory e di un file nella directory</span><span class="sxs-lookup"><span data-stu-id="8c249-103">Searching for a Directory and a File in the Directory</span></span>

<span data-ttu-id="8c249-104">**Per cercare una directory e quindi un file nella directory**</span><span class="sxs-lookup"><span data-stu-id="8c249-104">**To search for a directory and then a file in that directory**</span></span>

1.  <span data-ttu-id="8c249-105">Eseguire prima la ricerca della directory.</span><span class="sxs-lookup"><span data-stu-id="8c249-105">First search for the directory.</span></span>

    <span data-ttu-id="8c249-106">AppDir deve essere definito come la firma valida della directory.</span><span class="sxs-lookup"><span data-stu-id="8c249-106">AppDir must be defined as the valid signature of the directory.</span></span> <span data-ttu-id="8c249-107">Se AppDir non è definito come una firma valida, AppSearch non dispone di una posizione per trovare il file, ad esempio, se la ricerca è per c: \\ MyDir \\MyApp.exe, appdir deve essere definito come c: \\ mydir.</span><span class="sxs-lookup"><span data-stu-id="8c249-107">If AppDir is not defined as a valid signature, AppSearch does not have a place to find the file, for example, if the search is for c:\\MyDir\\MyApp.exe, AppDir should be defined as c:\\MyDir.</span></span> <span data-ttu-id="8c249-108">AppDir può essere definito includendo un record nella [tabella DrLocator](drlocator-table.md)o con un altro metodo.</span><span class="sxs-lookup"><span data-stu-id="8c249-108">AppDir might be defined by including a record in the [DrLocator Table](drlocator-table.md), or by some other method.</span></span> <span data-ttu-id="8c249-109">Nessun record è incluso nella [tabella delle firme](signature-table.md) per la ricerca nella directory.</span><span class="sxs-lookup"><span data-stu-id="8c249-109">No record is included in the [Signature Table](signature-table.md) for the directory search.</span></span> <span data-ttu-id="8c249-110">Per la ricerca di file, elencare la firma e il nome del file nella tabella della firma.</span><span class="sxs-lookup"><span data-stu-id="8c249-110">For the file search, list the file signature and name in the Signature Table.</span></span> <span data-ttu-id="8c249-111">I campi rimanenti di questo record possono essere null per cercare qualsiasi versione di MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="8c249-111">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="8c249-112">[Tabella delle firme](signature-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="8c249-112">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="8c249-113">Firma</span><span class="sxs-lookup"><span data-stu-id="8c249-113">Signature</span></span>          | <span data-ttu-id="8c249-114">File Name</span><span class="sxs-lookup"><span data-stu-id="8c249-114">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="8c249-115">AppFile</span><span class="sxs-lookup"><span data-stu-id="8c249-115">AppFile</span></span><br/> | <span data-ttu-id="8c249-116">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="8c249-116">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="8c249-117">Usare la [tabella AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c249-117">Use the [AppSearch Table](appsearch-table.md).</span></span>

    <span data-ttu-id="8c249-118">Immettere la proprietà che verrà impostata dal programma di installazione se è installata la directory con la firma AppDir.</span><span class="sxs-lookup"><span data-stu-id="8c249-118">Enter the property that the Installer is to set if the directory with the signature AppDir is installed.</span></span> <span data-ttu-id="8c249-119">Se il programma di installazione rileva che questa directory è installata, imposta MYDIR sul percorso della directory.</span><span class="sxs-lookup"><span data-stu-id="8c249-119">If the Installer finds this directory is installed, it sets MYDIR to the directory path.</span></span> <span data-ttu-id="8c249-120">Immettere la proprietà che verrà impostata dal programma di installazione se MyApp.exe è installato.</span><span class="sxs-lookup"><span data-stu-id="8c249-120">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="8c249-121">[Tabella AppSearch](appsearch-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="8c249-121">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="8c249-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c249-122">Property</span></span>         | <span data-ttu-id="8c249-123">Firma</span><span class="sxs-lookup"><span data-stu-id="8c249-123">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="8c249-124">MYDIR</span><span class="sxs-lookup"><span data-stu-id="8c249-124">MYDIR</span></span><br/> | <span data-ttu-id="8c249-125">AppDir</span><span class="sxs-lookup"><span data-stu-id="8c249-125">AppDir</span></span><br/>  |
    | <span data-ttu-id="8c249-126">MYAPP</span><span class="sxs-lookup"><span data-stu-id="8c249-126">MYAPP</span></span><br/> | <span data-ttu-id="8c249-127">AppFile</span><span class="sxs-lookup"><span data-stu-id="8c249-127">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="8c249-128">Usare la [tabella DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c249-128">Use the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="8c249-129">Immettere nella colonna padre la firma, AppDir, definita come percorso della directory.</span><span class="sxs-lookup"><span data-stu-id="8c249-129">Enter in the Parent column the signature, AppDir, that is defined as the path of the directory.</span></span> <span data-ttu-id="8c249-130">Specificare nella colonna profondità il numero di livelli di sottodirectory in cui eseguire la ricerca in questa directory.</span><span class="sxs-lookup"><span data-stu-id="8c249-130">Specify in the Depth column the number of subdirectory levels to search in this directory.</span></span> <span data-ttu-id="8c249-131">AppDir deve essere definito come firma di directory.</span><span class="sxs-lookup"><span data-stu-id="8c249-131">AppDir must be defined as the directory signature.</span></span> <span data-ttu-id="8c249-132">AppDir può essere definito includendo un record, come illustrato qui o da un altro metodo.</span><span class="sxs-lookup"><span data-stu-id="8c249-132">AppDir may be defined by including a record as shown here or by another method.</span></span>

    [<span data-ttu-id="8c249-133">Tabella DrLocator</span><span class="sxs-lookup"><span data-stu-id="8c249-133">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="8c249-134">Firma</span><span class="sxs-lookup"><span data-stu-id="8c249-134">Signature</span></span> | <span data-ttu-id="8c249-135">Padre</span><span class="sxs-lookup"><span data-stu-id="8c249-135">Parent</span></span> | <span data-ttu-id="8c249-136">Percorso</span><span class="sxs-lookup"><span data-stu-id="8c249-136">Path</span></span>      | <span data-ttu-id="8c249-137">Profondità</span><span class="sxs-lookup"><span data-stu-id="8c249-137">Depth</span></span> |
    |-----------|--------|-----------|-------|
    | <span data-ttu-id="8c249-138">AppDir</span><span class="sxs-lookup"><span data-stu-id="8c249-138">AppDir</span></span>    |        | <span data-ttu-id="8c249-139">C: \\ mydir</span><span class="sxs-lookup"><span data-stu-id="8c249-139">C:\\MyDir</span></span> | <span data-ttu-id="8c249-140">0</span><span class="sxs-lookup"><span data-stu-id="8c249-140">0</span></span>     |
    | <span data-ttu-id="8c249-141">AppFile</span><span class="sxs-lookup"><span data-stu-id="8c249-141">AppFile</span></span>   | <span data-ttu-id="8c249-142">AppDir</span><span class="sxs-lookup"><span data-stu-id="8c249-142">AppDir</span></span> |           | <span data-ttu-id="8c249-143">0</span><span class="sxs-lookup"><span data-stu-id="8c249-143">0</span></span>     |

    

     

4.  <span data-ttu-id="8c249-144">Includere l'azione AppSearch nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="8c249-144">Include the AppSearch action in the action sequence.</span></span>

    <span data-ttu-id="8c249-145">Se viene trovato MyApp.exe da installare in AppDir, il programma di installazione imposta la proprietà MYAPP sul percorso del file.</span><span class="sxs-lookup"><span data-stu-id="8c249-145">If MyApp.exe is found to be installed in AppDir, the Installer sets the property MYAPP to the location of file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c249-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c249-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c249-147">Ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti</span><span class="sxs-lookup"><span data-stu-id="8c249-147">Searching for Existing Applications, Files, Registry Entries or .ini File Entries</span></span>](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
</dt> </dl>

 

 




