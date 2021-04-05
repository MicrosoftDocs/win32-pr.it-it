---
description: Orca.exe è un editor di tabelle di database per la creazione e la modifica di Windows Installer pacchetti e Unione di moduli.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f17874e08fcdbfdbab38c480219579897b9896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049430"
---
# <a name="orcaexe"></a><span data-ttu-id="e2441-103">Orca.exe</span><span class="sxs-lookup"><span data-stu-id="e2441-103">Orca.exe</span></span>

<span data-ttu-id="e2441-104">Orca.exe è un editor di tabelle di database per la creazione e la modifica di Windows Installer pacchetti e Unione di moduli.</span><span class="sxs-lookup"><span data-stu-id="e2441-104">Orca.exe is a database table editor for creating and editing Windows Installer packages and merge modules.</span></span> <span data-ttu-id="e2441-105">Lo strumento fornisce un'interfaccia grafica per la convalida, evidenziando le voci specifiche in cui si verificano errori o avvisi di convalida.</span><span class="sxs-lookup"><span data-stu-id="e2441-105">The tool provides a graphical interface for validation, highlighting the particular entries where validation errors or warnings occur.</span></span>

<span data-ttu-id="e2441-106">Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="e2441-106">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="e2441-107">Viene fornito come file di Orca.msi.</span><span class="sxs-lookup"><span data-stu-id="e2441-107">It is provided as an Orca.msi file.</span></span> <span data-ttu-id="e2441-108">Dopo aver installato i componenti Windows SDK per gli sviluppatori di Windows Installer, fare doppio clic su Orca.msi per installare il file Orca.exe.</span><span class="sxs-lookup"><span data-stu-id="e2441-108">After installing the Windows SDK Components for Windows Installer Developers, double click Orca.msi to install the Orca.exe file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2441-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2441-109">Syntax</span></span>

<span data-ttu-id="e2441-110">\**Orca\*\*\*\[<options>\]\[<source file>\]*</span><span class="sxs-lookup"><span data-stu-id="e2441-110">**orca** *\[<options>\]\[<source file>\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="e2441-111">Opzioni da riga di comando</span><span class="sxs-lookup"><span data-stu-id="e2441-111">Command Line Options</span></span>

<span data-ttu-id="e2441-112">Orca.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e2441-112">Orca.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="e2441-113">Al posto di un trattino, può essere utilizzato anche un delimitatore di barra.</span><span class="sxs-lookup"><span data-stu-id="e2441-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="e2441-114">Opzione</span><span class="sxs-lookup"><span data-stu-id="e2441-114">Option</span></span> | <span data-ttu-id="e2441-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2441-115">Description</span></span>                                                 |
|--------|-------------------------------------------------------------|
| <span data-ttu-id="e2441-116">-Q</span><span class="sxs-lookup"><span data-stu-id="e2441-116">-q</span></span>     | <span data-ttu-id="e2441-117">Modalità non interattiva</span><span class="sxs-lookup"><span data-stu-id="e2441-117">Quiet mode</span></span>                                                  |
| <span data-ttu-id="e2441-118">-S</span><span class="sxs-lookup"><span data-stu-id="e2441-118">-s</span></span>     | <span data-ttu-id="e2441-119"><*Database Schema>* database \[ "Orca. dat"-predefinito\]</span><span class="sxs-lookup"><span data-stu-id="e2441-119"><*database*> Schema database \["orca.dat" - default\]</span></span> |
| <span data-ttu-id="e2441-120">-?</span><span class="sxs-lookup"><span data-stu-id="e2441-120">-?</span></span>     | <span data-ttu-id="e2441-121">Finestra di dialogo della Guida</span><span class="sxs-lookup"><span data-stu-id="e2441-121">Help dialog</span></span>                                                 |



 

<span data-ttu-id="e2441-122">Orca.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole con i moduli merge.</span><span class="sxs-lookup"><span data-stu-id="e2441-122">Orca.exe uses the following case-insensitive command line options with merge modules.</span></span> <span data-ttu-id="e2441-123">Al posto di un trattino, può essere utilizzato anche un delimitatore di barra.</span><span class="sxs-lookup"><span data-stu-id="e2441-123">A slash delimiter may also be used in place of a dash.</span></span> <span data-ttu-id="e2441-124">Quando si esegue un'operazione di merge, il valore-f,-m e <*sourcefile*> sono tutti obbligatori.</span><span class="sxs-lookup"><span data-stu-id="e2441-124">When performing a merge the -f, -m and <*sourcefile*> are all required.</span></span>



| <span data-ttu-id="e2441-125">Opzione</span><span class="sxs-lookup"><span data-stu-id="e2441-125">Option</span></span>     | <span data-ttu-id="e2441-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2441-126">Description</span></span>                                                                |
|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="e2441-127">-c</span><span class="sxs-lookup"><span data-stu-id="e2441-127">-c</span></span>         | <span data-ttu-id="e2441-128">Eseguire il commit del merge nel database se non si verificano errori.</span><span class="sxs-lookup"><span data-stu-id="e2441-128">Commit merge to database if no errors.</span></span>                                     |
| <span data-ttu-id="e2441-129">-!</span><span class="sxs-lookup"><span data-stu-id="e2441-129">-!</span></span>         | <span data-ttu-id="e2441-130">Eseguire il commit del merge in un database anche in caso di errori.</span><span class="sxs-lookup"><span data-stu-id="e2441-130">Commit merge to a database even if there are errors.</span></span>                       |
| <span data-ttu-id="e2441-131">-M</span><span class="sxs-lookup"><span data-stu-id="e2441-131">-m</span></span>         | <span data-ttu-id="e2441-132"><*modulo> Unione* del modulo da unire nel database.</span><span class="sxs-lookup"><span data-stu-id="e2441-132"><*module*> Merge Module to merge into database.</span></span>                      |
| <span data-ttu-id="e2441-133">-f</span><span class="sxs-lookup"><span data-stu-id="e2441-133">-f</span></span>         | <span data-ttu-id="e2441-134">Funzionalità \[ : \] funzionalità di Funzionalità2 per la connessione al modulo merge.</span><span class="sxs-lookup"><span data-stu-id="e2441-134">Feature\[:Feature2\] Feature(s) to connect to Merge Module.</span></span>                |
| <span data-ttu-id="e2441-135">-r</span><span class="sxs-lookup"><span data-stu-id="e2441-135">-r</span></span>         | <span data-ttu-id="e2441-136"><*ID directory*> voce di directory per il reindirizzamento radice del modulo.</span><span class="sxs-lookup"><span data-stu-id="e2441-136"><*directory id*> Directory entry for the module root redirection.</span></span>    |
| <span data-ttu-id="e2441-137">-X</span><span class="sxs-lookup"><span data-stu-id="e2441-137">-x</span></span>         | <span data-ttu-id="e2441-138"><*directory*> estrarre i file in un'immagine nella directory.</span><span class="sxs-lookup"><span data-stu-id="e2441-138"><*directory*> Extract files to an image under the directory.</span></span>         |
| <span data-ttu-id="e2441-139">-g</span><span class="sxs-lookup"><span data-stu-id="e2441-139">-g</span></span>         | <span data-ttu-id="e2441-140"><*lingua> lingua* utilizzata per aprire un modulo.</span><span class="sxs-lookup"><span data-stu-id="e2441-140"><*language*> Language used to open a module.</span></span>                         |
| <span data-ttu-id="e2441-141">-l</span><span class="sxs-lookup"><span data-stu-id="e2441-141">-l</span></span>         | <span data-ttu-id="e2441-142"><file di *log*> file da utilizzare come log, aggiungere se esiste già.</span><span class="sxs-lookup"><span data-stu-id="e2441-142"><*log file*> File to use as a log, append if it already exists.</span></span>      |
| <span data-ttu-id="e2441-143">-i</span><span class="sxs-lookup"><span data-stu-id="e2441-143">-i</span></span>         | <span data-ttu-id="e2441-144"><*directory*> estrarre i file nell'immagine di origine sotto la directory.</span><span class="sxs-lookup"><span data-stu-id="e2441-144"><*directory*> Extract files to the source image under the directory.</span></span> |
| <span data-ttu-id="e2441-145">-CAB</span><span class="sxs-lookup"><span data-stu-id="e2441-145">-cab</span></span>       | <span data-ttu-id="e2441-146"><*filename*> estrarre il file CAB msm nel file.</span><span class="sxs-lookup"><span data-stu-id="e2441-146"><*filename*> Extract the MSM cabinet to file.</span></span>                        |
| <span data-ttu-id="e2441-147">-LFN</span><span class="sxs-lookup"><span data-stu-id="e2441-147">-lfn</span></span>       | <span data-ttu-id="e2441-148">Usare nomi di file lunghi durante l'estrazione.</span><span class="sxs-lookup"><span data-stu-id="e2441-148">Use Long File Names during the extraction.</span></span>                                 |
| <span data-ttu-id="e2441-149">-Configura</span><span class="sxs-lookup"><span data-stu-id="e2441-149">-configure</span></span> | <span data-ttu-id="e2441-150"><*filename*> configurare il modulo usando i dati di un file.</span><span class="sxs-lookup"><span data-stu-id="e2441-150"><*filename*> Configure the module using data from a file.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="e2441-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2441-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2441-152">Strumenti di sviluppo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="e2441-152">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="e2441-153">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="e2441-153">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



