---
description: I messaggi di informazioni seguenti descrivono l'operazione del compilatore.
ms.assetid: 838e598d-871d-4015-a372-4d94cacf8048
ms.tgt_platform: multiple
title: Messaggi informativi generali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0997fad497299c7598fc1130edace49c20d7bb76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344911"
---
# <a name="general-information-messages"></a><span data-ttu-id="7fb72-103">Messaggi informativi generali</span><span class="sxs-lookup"><span data-stu-id="7fb72-103">General Information Messages</span></span>

<span data-ttu-id="7fb72-104">I messaggi di informazioni seguenti descrivono l'operazione del compilatore.</span><span class="sxs-lookup"><span data-stu-id="7fb72-104">The following information messages describe the compiler operation.</span></span>

<dl> <dt>

<span data-ttu-id="7fb72-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: versione <versione \#> le definizioni MIB compilate da <file name>**</span><span class="sxs-lookup"><span data-stu-id="7fb72-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: Version <version \#> MIB definitions compiled from <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-106">Questo messaggio viene visualizzato all'inizio di ogni compilazione di file.</span><span class="sxs-lookup"><span data-stu-id="7fb72-106">This message appears at the beginning of every file compilation.</span></span> <span data-ttu-id="7fb72-107">Significa che è possibile che il file sia stato specificato in modo esplicito nella riga di comando dall'utente oppure che sia stato eseguito il pull dal compilatore dalle directory di inclusione del registro di sistema o dalle directory di inclusione indicate nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="7fb72-107">It means the file may have been explicitly specified on the command line by the user, or it may have been pulled in by the compiler from the registry include directories or the include directories mentioned on the command line.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: controllo della sintassi non riuscito <file name>**</span><span class="sxs-lookup"><span data-stu-id="7fb72-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Syntax check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-109">I messaggi di errore specifici che precedono questo messaggio danno la natura degli errori di sintassi.</span><span class="sxs-lookup"><span data-stu-id="7fb72-109">The specific error messages that precede this message give the nature of the syntax errors.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: controllo semantico non riuscito <file name>**</span><span class="sxs-lookup"><span data-stu-id="7fb72-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Semantic check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-111">I messaggi di errore specifici che precedono questo messaggio danno la natura degli errori semantici.</span><span class="sxs-lookup"><span data-stu-id="7fb72-111">The specific error messages that precede this message give the nature of the semantic errors.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: non è stato possibile caricare <file name> in archivio SMIR**</span><span class="sxs-lookup"><span data-stu-id="7fb72-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: Could not load <file name> into the smir**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-113">La sintassi o il controllo semantico non è riuscito nel modulo oppure l'interazione archivio SMIR non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7fb72-113">Syntax or semantic check failed on the module, or SMIR interaction was not complete.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: verifica della sintassi riuscita <file name>**</span><span class="sxs-lookup"><span data-stu-id="7fb72-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Syntax check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7fb72-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: verifica semantica riuscita <file name>**</span><span class="sxs-lookup"><span data-stu-id="7fb72-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Semantic check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7fb72-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: caricato <file name> correttamente in archivio SMIR**</span><span class="sxs-lookup"><span data-stu-id="7fb72-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: Loaded <file name> successfully into the smir**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7fb72-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: non è stato possibile risolvere uno o più simboli in <module name>**</span><span class="sxs-lookup"><span data-stu-id="7fb72-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: Could not resolve one or more symbols in <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-118">I moduli corrispondenti a uno o più simboli importati nel modulo specificato non sono stati trovati o non possono essere compilati.</span><span class="sxs-lookup"><span data-stu-id="7fb72-118">The modules corresponding to one or more of the imported symbols in the specified module were not found or could not be compiled.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: non è stato possibile connettersi al archivio SMIR**</span><span class="sxs-lookup"><span data-stu-id="7fb72-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: Could not connect to the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-120">Verificare che Smir.dll esista, sia stato registrato utilizzando il comando regsvr32 e che il server di Strumentazione gestione Windows (WMI) sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7fb72-120">Ensure that Smir.dll exists, has been registered using the regsvr32 command, and that the Windows Management Instrumentation (WMI) server is up and running.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: moduli in archivio SMIR: <elenco di moduli, 1 in ogni riga>**</span><span class="sxs-lookup"><span data-stu-id="7fb72-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: Modules in the SMIR: <list of modules, 1 on each line>**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-122">Si tratta dell'output dell'opzione **/l** .</span><span class="sxs-lookup"><span data-stu-id="7fb72-122">This is the output of the **/l** switch.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir non è riuscito a elencare i moduli in archivio SMIR**</span><span class="sxs-lookup"><span data-stu-id="7fb72-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir Could not list the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-124">Ciò indica un errore dell'opzione **/l** a causa di una connessione archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="7fb72-124">This indicates a failure of the **/l** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: il modulo è stato eliminato <module name>**</span><span class="sxs-lookup"><span data-stu-id="7fb72-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: Deleted module <module name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-126">L'opzione **/d** è riuscita.</span><span class="sxs-lookup"><span data-stu-id="7fb72-126">The **/d** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: non è stato possibile eliminare il modulo <module name>**</span><span class="sxs-lookup"><span data-stu-id="7fb72-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: Could not delete module <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-128">Ciò indica un errore dell'opzione **/d** a causa di una connessione archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="7fb72-128">This indicates a failure of the **/d** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: tutti i moduli in archivio SMIR sono stati eliminati**</span><span class="sxs-lookup"><span data-stu-id="7fb72-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Deleted all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-130">L'opzione **/p** è riuscita.</span><span class="sxs-lookup"><span data-stu-id="7fb72-130">The **/p** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: non è stato possibile eliminare tutti i moduli in archivio SMIR**</span><span class="sxs-lookup"><span data-stu-id="7fb72-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Could not delete all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-132">L'opzione **/p** non è riuscita perché non esiste una connessione archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="7fb72-132">The **/p** switch failed because there is no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: il modulo non <module name> esiste in archivio SMIR**</span><span class="sxs-lookup"><span data-stu-id="7fb72-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: Module <module name> does not exist in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-134">L'opzione **/d** non è riuscita perché il modulo specificato non è presente in archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="7fb72-134">The **/d** switch failed because the specified module is not in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: MOF generato correttamente**</span><span class="sxs-lookup"><span data-stu-id="7fb72-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: Generated MOF successfully**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-136">Il parametro **/g** o **/GC** ha funzionato correttamente.</span><span class="sxs-lookup"><span data-stu-id="7fb72-136">The **/g** or **/gc** switch worked successfully.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: non è stato possibile generare MOF**</span><span class="sxs-lookup"><span data-stu-id="7fb72-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: Could not generate MOF**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-138">Il funzionamento dell'opzione **/g** o **/GC** non è riuscito a causa di nessuna connessione archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="7fb72-138">The **/g** or **/gc** switch did not work successfully due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: nome del modulo: <module name>**</span><span class="sxs-lookup"><span data-stu-id="7fb72-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: Name of the module: <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-140">Questo è l'output corretto dell'opzione **/n** .</span><span class="sxs-lookup"><span data-stu-id="7fb72-140">This is the successful output of the **/n** switch.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: non è stato possibile analizzare <file name> correttamente**</span><span class="sxs-lookup"><span data-stu-id="7fb72-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: Could not parse <file name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-142">Ciò indica un errore dell'opzione **/n** o **/NI** perché il file specificato non è un file MIB valido.</span><span class="sxs-lookup"><span data-stu-id="7fb72-142">This indicates failure of the **/n** or **/ni** switch because the specified file is not a valid MIB file.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: elaborazione dei <number> file completata**</span><span class="sxs-lookup"><span data-stu-id="7fb72-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: Processed <number> files successfully**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-144">Specifica il numero di file analizzati correttamente quando è stata usata l'opzione **/r** o **/auto** .</span><span class="sxs-lookup"><span data-stu-id="7fb72-144">This specifies the number of files that were successfully parsed when the **/r** or the **/auto** switch were used.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: file ripetuti nell'input per il modulo <module name> . Verrà compilato solo il file <file name>**</span><span class="sxs-lookup"><span data-stu-id="7fb72-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: Repeated files in the input for module <module name>. Only the file <file name> will be compiled**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-146">L'utente ha specificato in modo esplicito più di un file nella riga di comando e due o più file hanno lo stesso modulo MIB.</span><span class="sxs-lookup"><span data-stu-id="7fb72-146">The user has explicitly specified more than one file on the command line, and two or more of these files have the same MIB module.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: aggiunta <directory name> della directory al registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="7fb72-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Added directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-148">Esito positivo dell'opzione **/PA** .</span><span class="sxs-lookup"><span data-stu-id="7fb72-148">Success of the **/pa** switch.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Impossibile aggiungere la directory <directory name> al registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="7fb72-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Could not add directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-150">Errore dell'opzione **/PA** , che si verifica solo se l'API del registro di sistema ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="7fb72-150">Failure of the **/pa** switch, which happens only if the registry API fails.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: la directory è stata eliminata <directory name> dal registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="7fb72-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Deleted directory <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-152">Esito positivo dell'opzione **/PD** .</span><span class="sxs-lookup"><span data-stu-id="7fb72-152">Success of the **/pd** switch.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: non è stato possibile eliminare <directory name> dal registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="7fb72-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Could not delete <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-154">Errore dell'opzione **/PD** .</span><span class="sxs-lookup"><span data-stu-id="7fb72-154">Failure of the **/pd** switch.</span></span> <span data-ttu-id="7fb72-155">La directory specificata non esiste nell'elenco di directory nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7fb72-155">The specified directory does not exist in the list of directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="7fb72-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> non è un file MIB valido**</span><span class="sxs-lookup"><span data-stu-id="7fb72-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> is not a valid mib file**</span></span>
</dt> <dd>

<span data-ttu-id="7fb72-157">Nella riga di comando è stato specificato più di un file, uno dei quali non è un file MIB valido.</span><span class="sxs-lookup"><span data-stu-id="7fb72-157">More than one file has been specified on the command line, one of which is not a valid MIB file.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="7fb72-158">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fb72-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fb72-159">Configurazione dell'ambiente WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="7fb72-159">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



