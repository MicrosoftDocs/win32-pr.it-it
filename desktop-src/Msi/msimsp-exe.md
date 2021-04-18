---
description: Il metodo consigliato per la generazione di un pacchetto di patch consiste nell'usare strumenti per la creazione di patch, ad esempio Msimsp.exe e Patchwiz.dll. Lo strumento Msimsp.exe è disponibile solo nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320937"
---
# <a name="msimspexe"></a><span data-ttu-id="5c6e4-104">Msimsp.exe</span><span class="sxs-lookup"><span data-stu-id="5c6e4-104">Msimsp.exe</span></span>

<span data-ttu-id="5c6e4-105">Il metodo consigliato per la generazione di un pacchetto di patch consiste nell'usare strumenti per la creazione di patch, ad esempio Msimsp.exe e [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="5c6e4-105">The recommended method for generating a patch package is to use patch creation tools such as Msimsp.exe and [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="5c6e4-106">Lo strumento Msimsp.exe è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="5c6e4-106">The Msimsp.exe tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="5c6e4-107">Msimsp.exe è un file eseguibile che chiama [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="5c6e4-107">Msimsp.exe is a executable file that calls [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="5c6e4-108">Lo strumento può essere usato per creare un pacchetto di patch passando il percorso di un file delle proprietà di creazione della patch (file con estensione PCP) e il percorso del pacchetto di patch in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-108">The tool can be used to create a patch package by passing in the path to a patch creation properties file (.pcp file) and the path to the patch package that is being created.</span></span> <span data-ttu-id="5c6e4-109">Msimsp. es può inoltre essere utilizzato per creare un file di log e per specificare una cartella temporanea in cui vengono salvati le trasformazioni, i file CAB e i file utilizzati per creare il pacchetto di patch.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-109">Msimsp.ex can also be used to create a log file and to specify a temporary folder in which the transforms, cabinets, and files that are used to create the patch package are saved.</span></span>

<span data-ttu-id="5c6e4-110">La sintassi della riga di comando per Msimsp.exe è:</span><span class="sxs-lookup"><span data-stu-id="5c6e4-110">The command-line syntax for Msimsp.exe is:</span></span>

<span data-ttu-id="5c6e4-111">Percorso **Msimsp.exe-s del** *\[ file \] . PCP* **-p** *\[ percorso del file \] con estensione msp* **{options}**</span><span class="sxs-lookup"><span data-stu-id="5c6e4-111">**Msimsp.exe -s** *\[path to .pcp file\]* **-p** *\[path to .msp file\]* **{options}**</span></span>

<span data-ttu-id="5c6e4-112">Le opzioni della riga di comando non fanno distinzione tra maiuscole e minuscole e i delimitatori barra possono essere utilizzati al posto di un trattino.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-112">The command-line options are not case-sensitive, and slash delimiters can be used instead of a dash.</span></span> <span data-ttu-id="5c6e4-113">Se non viene specificata alcuna opzione, Msimsp.exe Visualizza i valori correnti delle proprietà delle informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-113">If no options are specified, Msimsp.exe displays the current values of the summary Information properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c6e4-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ percorso del file \] . PCP_</span><span class="sxs-lookup"><span data-stu-id="5c6e4-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[path to .pcp file\]_</span></span>
</dt> <dd>

<span data-ttu-id="5c6e4-115">Questa operazione è obbligatoria e deve essere seguita dal percorso del file delle proprietà di creazione della patch (estensione PCP).</span><span class="sxs-lookup"><span data-stu-id="5c6e4-115">This is required and must be followed by the path to the patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="5c6e4-116">Per ulteriori informazioni, vedere [PatchWiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="5c6e4-116">For more information, see [PatchWiz.dll](patchwiz-dll.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c6e4-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_percorso del file con estensione msp_</span><span class="sxs-lookup"><span data-stu-id="5c6e4-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_path to .msp file_</span></span>
</dt> <dd>

<span data-ttu-id="5c6e4-118">Questa operazione è obbligatoria e seguita dal percorso del pacchetto di patch creato (estensione msp).</span><span class="sxs-lookup"><span data-stu-id="5c6e4-118">This is required and followed by the path to patch package that is being created (.msp extension).</span></span>

</dd> <dt>

<span data-ttu-id="5c6e4-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_percorso alla cartella temporanea_</span><span class="sxs-lookup"><span data-stu-id="5c6e4-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_path to temporary folder_</span></span>
</dt> <dd>

<span data-ttu-id="5c6e4-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-120">Optional.</span></span> <span data-ttu-id="5c6e4-121">Seguito dal percorso alla cartella temporanea.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-121">Followed by path to temporary folder.</span></span> <span data-ttu-id="5c6e4-122">Il percorso predefinito è% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="5c6e4-122">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="5c6e4-123"><span id="-k"></span><span id="-K"></span>**-k**</span><span class="sxs-lookup"><span data-stu-id="5c6e4-123"><span id="-k"></span><span id="-K"></span>**-k**</span></span>
</dt> <dd>

<span data-ttu-id="5c6e4-124">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-124">Optional.</span></span> <span data-ttu-id="5c6e4-125">Esito negativo se la cartella temporanea esiste già.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-125">Fail if the temporary folder already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5c6e4-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_percorso del file di log_</span><span class="sxs-lookup"><span data-stu-id="5c6e4-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_path to log file_</span></span>
</dt> <dd>

<span data-ttu-id="5c6e4-127">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-127">Optional.</span></span> <span data-ttu-id="5c6e4-128">Seguito dal percorso del file di log che descrive il processo di creazione della patch ed errori.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-128">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="5c6e4-129">Per ulteriori informazioni, vedere [valori restituiti per UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="5c6e4-129">For more information, see [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c6e4-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-LP**_percorso del file di log con dati sulle prestazioni_</span><span class="sxs-lookup"><span data-stu-id="5c6e4-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-lp**_path to log file with performance data_</span></span>
</dt> <dd>

<span data-ttu-id="5c6e4-131">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-131">Optional.</span></span> <span data-ttu-id="5c6e4-132">Seguito dal percorso del file di log che descrive il processo di creazione della patch ed errori.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-132">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="5c6e4-133">Questa opzione scrive i dati sulle prestazioni in un file di log.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-133">This option writes performance data to log file.</span></span> <span data-ttu-id="5c6e4-134">Questa opzione richiede la versione 4,0 di Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-134">This option requires version 4.0 of Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="5c6e4-135"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="5c6e4-135"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="5c6e4-136">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-136">Optional.</span></span> <span data-ttu-id="5c6e4-137">Visualizza una finestra di dialogo se la creazione della patch viene completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-137">Displays a dialog if the patch creation completes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="5c6e4-138"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="5c6e4-138"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="5c6e4-139">Visualizza la guida della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-139">Displays command-line help.</span></span>

</dd> </dl>

> [!Note]
> <span data-ttu-id="5c6e4-140">Msimsp.exe possono avere esito negativo quando chiama Makecab.exe se nella colonna file della [tabella di file](file-table.md) del pacchetto di installazione sono presenti valori che differiscono solo per le maiuscole/minuscole.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-140">Msimsp.exe can fail when it calls Makecab.exe if there are values in the File column of the [File table](file-table.md) of the installation package that differ only by case.</span></span> <span data-ttu-id="5c6e4-141">Windows Installer fa distinzione tra maiuscole e minuscole e consente un pacchetto di installazione, ad esempio nella tabella seguente, solo quando comp1 e comp2 sono installati in directory diverse.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-141">Windows Installer is case-sensitive and allows an installation package such as in the table below only when Comp1 and Comp2 are installed into different directories.</span></span> <span data-ttu-id="5c6e4-142">Tuttavia, in questo scenario non è possibile utilizzare Msimsp.exe o [Patchwiz.dll](patchwiz-dll.md) per generare una patch per il pacchetto, poiché Msimsp.exe e Patchwiz.dll chiamare Makecab.exe, che non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-142">However, in this scenario you cannot use Msimsp.exe or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package, because Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive.</span></span>
> 
> <span data-ttu-id="5c6e4-143">Evitare di creare un pacchetto di installazione come la seguente [tabella file](file-table.md)parziale.</span><span class="sxs-lookup"><span data-stu-id="5c6e4-143">Avoid authoring an installation package such as the following partial [File table](file-table.md).</span></span>
> 
> | <span data-ttu-id="5c6e4-144">File</span><span class="sxs-lookup"><span data-stu-id="5c6e4-144">File</span></span>       | <span data-ttu-id="5c6e4-145">Componente\_</span><span class="sxs-lookup"><span data-stu-id="5c6e4-145">Component\_</span></span> | <span data-ttu-id="5c6e4-146">FileName</span><span class="sxs-lookup"><span data-stu-id="5c6e4-146">FileName</span></span>   |
> |------------|-------------|------------|
> | <span data-ttu-id="5c6e4-147">readme.txt</span><span class="sxs-lookup"><span data-stu-id="5c6e4-147">readme.txt</span></span> | <span data-ttu-id="5c6e4-148">Comp1</span><span class="sxs-lookup"><span data-stu-id="5c6e4-148">Comp1</span></span>       | <span data-ttu-id="5c6e4-149">readme.txt</span><span class="sxs-lookup"><span data-stu-id="5c6e4-149">readme.txt</span></span> |
> | <span data-ttu-id="5c6e4-150">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="5c6e4-150">ReadMe.txt</span></span> | <span data-ttu-id="5c6e4-151">Comp2</span><span class="sxs-lookup"><span data-stu-id="5c6e4-151">Comp2</span></span>       | <span data-ttu-id="5c6e4-152">readme.txt</span><span class="sxs-lookup"><span data-stu-id="5c6e4-152">readme.txt</span></span> |


## <a name="related-topics"></a><span data-ttu-id="5c6e4-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c6e4-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c6e4-154">Creazione di un pacchetto di patch</span><span class="sxs-lookup"><span data-stu-id="5c6e4-154">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="5c6e4-155">Un piccolo esempio di patch di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5c6e4-155">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)
</dt> <dt>

[<span data-ttu-id="5c6e4-156">Strumenti di sviluppo Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5c6e4-156">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="5c6e4-157">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="5c6e4-157">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



