---
description: Orca.exe è un editor di tabelle di database per la creazione e la modifica di Windows Installer pacchetti e moduli unione.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4647b137650bfba521dba3976ea7a1ae66451ce
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102160"
---
# <a name="orcaexe"></a><span data-ttu-id="f0f94-103">Orca.exe</span><span class="sxs-lookup"><span data-stu-id="f0f94-103">Orca.exe</span></span>

<span data-ttu-id="f0f94-104">Orca.exe è un editor di tabelle di database per la creazione e la modifica di Windows Installer pacchetti e moduli unione.</span><span class="sxs-lookup"><span data-stu-id="f0f94-104">Orca.exe is a database table editor for creating and editing Windows Installer packages and merge modules.</span></span> <span data-ttu-id="f0f94-105">Lo strumento fornisce un'interfaccia grafica per la convalida, evidenziando le voci specifiche in cui si verificano errori o avvisi di convalida.</span><span class="sxs-lookup"><span data-stu-id="f0f94-105">The tool provides a graphical interface for validation, highlighting the particular entries where validation errors or warnings occur.</span></span>

<span data-ttu-id="f0f94-106">Questo strumento è disponibile solo nella pagina [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="f0f94-106">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="f0f94-107">Viene fornito come file Orca.msi.</span><span class="sxs-lookup"><span data-stu-id="f0f94-107">It is provided as an Orca.msi file.</span></span> <span data-ttu-id="f0f94-108">Dopo aver installato i componenti Windows SDK per Windows Installer, fare doppio clic su Orca.msi per installare il file Orca.exe.</span><span class="sxs-lookup"><span data-stu-id="f0f94-108">After installing the Windows SDK Components for Windows Installer Developers, double click Orca.msi to install the Orca.exe file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0f94-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0f94-109">Syntax</span></span>

<span data-ttu-id="f0f94-110">\**orca\*\*\*\[\<options>\]\[\<source file>\]*</span><span class="sxs-lookup"><span data-stu-id="f0f94-110">**orca** *\[\<options>\]\[\<source file>\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="f0f94-111">Opzioni da riga di comando</span><span class="sxs-lookup"><span data-stu-id="f0f94-111">Command Line Options</span></span>

<span data-ttu-id="f0f94-112">Orca.exe usa le opzioni della riga di comando seguenti senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f0f94-112">Orca.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="f0f94-113">È anche possibile usare un delimitatore barra al posto di un trattino.</span><span class="sxs-lookup"><span data-stu-id="f0f94-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="f0f94-114">Opzione</span><span class="sxs-lookup"><span data-stu-id="f0f94-114">Option</span></span> | <span data-ttu-id="f0f94-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0f94-115">Description</span></span>                                                 |
|--------|-------------------------------------------------------------|
| <span data-ttu-id="f0f94-116">-Q</span><span class="sxs-lookup"><span data-stu-id="f0f94-116">-q</span></span>     | <span data-ttu-id="f0f94-117">Modalità non interattiva</span><span class="sxs-lookup"><span data-stu-id="f0f94-117">Quiet mode</span></span>                                                  |
| <span data-ttu-id="f0f94-118">-S</span><span class="sxs-lookup"><span data-stu-id="f0f94-118">-s</span></span>     | <span data-ttu-id="f0f94-119"><*database*> Schema database \[ "orca.dat": impostazione predefinita\]</span><span class="sxs-lookup"><span data-stu-id="f0f94-119"><*database*> Schema database \["orca.dat" - default\]</span></span> |
| <span data-ttu-id="f0f94-120">-?</span><span class="sxs-lookup"><span data-stu-id="f0f94-120">-?</span></span>     | <span data-ttu-id="f0f94-121">Finestra di dialogo Della Guida</span><span class="sxs-lookup"><span data-stu-id="f0f94-121">Help dialog</span></span>                                                 |



 

<span data-ttu-id="f0f94-122">Orca.exe usa le opzioni della riga di comando seguenti senza distinzione tra maiuscole e minuscole con i moduli unione.</span><span class="sxs-lookup"><span data-stu-id="f0f94-122">Orca.exe uses the following case-insensitive command line options with merge modules.</span></span> <span data-ttu-id="f0f94-123">È anche possibile usare un delimitatore barra al posto di un trattino.</span><span class="sxs-lookup"><span data-stu-id="f0f94-123">A slash delimiter may also be used in place of a dash.</span></span> <span data-ttu-id="f0f94-124">Quando si esegue un'unione, sono necessari i <-f, -m *> sourcefile.*</span><span class="sxs-lookup"><span data-stu-id="f0f94-124">When performing a merge the -f, -m and <*sourcefile*> are all required.</span></span>



| <span data-ttu-id="f0f94-125">Opzione</span><span class="sxs-lookup"><span data-stu-id="f0f94-125">Option</span></span>     | <span data-ttu-id="f0f94-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0f94-126">Description</span></span>                                                                |
|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="f0f94-127">-c</span><span class="sxs-lookup"><span data-stu-id="f0f94-127">-c</span></span>         | <span data-ttu-id="f0f94-128">Eseguire il commit del merge nel database se non si verificano errori.</span><span class="sxs-lookup"><span data-stu-id="f0f94-128">Commit merge to database if no errors.</span></span>                                     |
| <span data-ttu-id="f0f94-129">-!</span><span class="sxs-lookup"><span data-stu-id="f0f94-129">-!</span></span>         | <span data-ttu-id="f0f94-130">Eseguire il commit del merge in un database anche se sono presenti errori.</span><span class="sxs-lookup"><span data-stu-id="f0f94-130">Commit merge to a database even if there are errors.</span></span>                       |
| <span data-ttu-id="f0f94-131">-M</span><span class="sxs-lookup"><span data-stu-id="f0f94-131">-m</span></span>         | <span data-ttu-id="f0f94-132"><*Modulo>* Merge Module da unire nel database.</span><span class="sxs-lookup"><span data-stu-id="f0f94-132"><*module*> Merge Module to merge into database.</span></span>                      |
| <span data-ttu-id="f0f94-133">-f</span><span class="sxs-lookup"><span data-stu-id="f0f94-133">-f</span></span>         | <span data-ttu-id="f0f94-134">\[Funzionalità:Funzionalità2 \] Funzionalità per la connessione al modulo di unione.</span><span class="sxs-lookup"><span data-stu-id="f0f94-134">Feature\[:Feature2\] Feature(s) to connect to Merge Module.</span></span>                |
| <span data-ttu-id="f0f94-135">-r</span><span class="sxs-lookup"><span data-stu-id="f0f94-135">-r</span></span>         | <span data-ttu-id="f0f94-136"><*ID directory>* directory per il reindirizzamento radice del modulo.</span><span class="sxs-lookup"><span data-stu-id="f0f94-136"><*directory id*> Directory entry for the module root redirection.</span></span>    |
| <span data-ttu-id="f0f94-137">-X</span><span class="sxs-lookup"><span data-stu-id="f0f94-137">-x</span></span>         | <span data-ttu-id="f0f94-138"><*directory*> estrai i file in un'immagine nella directory .</span><span class="sxs-lookup"><span data-stu-id="f0f94-138"><*directory*> Extract files to an image under the directory.</span></span>         |
| <span data-ttu-id="f0f94-139">-g</span><span class="sxs-lookup"><span data-stu-id="f0f94-139">-g</span></span>         | <span data-ttu-id="f0f94-140"><*language*> linguaggio usato per aprire un modulo.</span><span class="sxs-lookup"><span data-stu-id="f0f94-140"><*language*> Language used to open a module.</span></span>                         |
| <span data-ttu-id="f0f94-141">-l</span><span class="sxs-lookup"><span data-stu-id="f0f94-141">-l</span></span>         | <span data-ttu-id="f0f94-142"><*file di log*> file da usare come log, aggiungere se esiste già.</span><span class="sxs-lookup"><span data-stu-id="f0f94-142"><*log file*> File to use as a log, append if it already exists.</span></span>      |
| <span data-ttu-id="f0f94-143">-i</span><span class="sxs-lookup"><span data-stu-id="f0f94-143">-i</span></span>         | <span data-ttu-id="f0f94-144"><*directory*> estrai i file nell'immagine di origine nella directory .</span><span class="sxs-lookup"><span data-stu-id="f0f94-144"><*directory*> Extract files to the source image under the directory.</span></span> |
| <span data-ttu-id="f0f94-145">-cab</span><span class="sxs-lookup"><span data-stu-id="f0f94-145">-cab</span></span>       | <span data-ttu-id="f0f94-146"><*filename>* Extract the MSM cabinet to file.</span><span class="sxs-lookup"><span data-stu-id="f0f94-146"><*filename*> Extract the MSM cabinet to file.</span></span>                        |
| <span data-ttu-id="f0f94-147">-lfn</span><span class="sxs-lookup"><span data-stu-id="f0f94-147">-lfn</span></span>       | <span data-ttu-id="f0f94-148">Usare nomi file lunghi durante l'estrazione.</span><span class="sxs-lookup"><span data-stu-id="f0f94-148">Use Long File Names during the extraction.</span></span>                                 |
| <span data-ttu-id="f0f94-149">-configure</span><span class="sxs-lookup"><span data-stu-id="f0f94-149">-configure</span></span> | <span data-ttu-id="f0f94-150"><*nome*> configurare il modulo usando i dati di un file.</span><span class="sxs-lookup"><span data-stu-id="f0f94-150"><*filename*> Configure the module using data from a file.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="f0f94-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0f94-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0f94-152">Windows Installer di sviluppo</span><span class="sxs-lookup"><span data-stu-id="f0f94-152">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="f0f94-153">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="f0f94-153">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



