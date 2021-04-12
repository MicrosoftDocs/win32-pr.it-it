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
# <a name="general-information-messages"></a>Messaggi informativi generali

I messaggi di informazioni seguenti descrivono l'operazione del compilatore.

<dl> <dt>

<span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: versione <versione \#> le definizioni MIB compilate da <file name>**
</dt> <dd>

Questo messaggio viene visualizzato all'inizio di ogni compilazione di file. Significa che è possibile che il file sia stato specificato in modo esplicito nella riga di comando dall'utente oppure che sia stato eseguito il pull dal compilatore dalle directory di inclusione del registro di sistema o dalle directory di inclusione indicate nella riga di comando.

</dd> <dt>

<span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: controllo della sintassi non riuscito <file name>**
</dt> <dd>

I messaggi di errore specifici che precedono questo messaggio danno la natura degli errori di sintassi.

</dd> <dt>

<span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: controllo semantico non riuscito <file name>**
</dt> <dd>

I messaggi di errore specifici che precedono questo messaggio danno la natura degli errori semantici.

</dd> <dt>

<span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: non è stato possibile caricare <file name> in archivio SMIR**
</dt> <dd>

La sintassi o il controllo semantico non è riuscito nel modulo oppure l'interazione archivio SMIR non è stata completata.

</dd> <dt>

<span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: verifica della sintassi riuscita <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: verifica semantica riuscita <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: caricato <file name> correttamente in archivio SMIR**
</dt> <dd></dd> <dt>

<span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: non è stato possibile risolvere uno o più simboli in <module name>**
</dt> <dd>

I moduli corrispondenti a uno o più simboli importati nel modulo specificato non sono stati trovati o non possono essere compilati.

</dd> <dt>

<span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: non è stato possibile connettersi al archivio SMIR**
</dt> <dd>

Verificare che Smir.dll esista, sia stato registrato utilizzando il comando regsvr32 e che il server di Strumentazione gestione Windows (WMI) sia in esecuzione.

</dd> <dt>

<span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: moduli in archivio SMIR: <elenco di moduli, 1 in ogni riga>**
</dt> <dd>

Si tratta dell'output dell'opzione **/l** .

</dd> <dt>

<span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir non è riuscito a elencare i moduli in archivio SMIR**
</dt> <dd>

Ciò indica un errore dell'opzione **/l** a causa di una connessione archivio SMIR.

</dd> <dt>

<span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: il modulo è stato eliminato <module name>**
</dt> <dd>

L'opzione **/d** è riuscita.

</dd> <dt>

<span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: non è stato possibile eliminare il modulo <module name>**
</dt> <dd>

Ciò indica un errore dell'opzione **/d** a causa di una connessione archivio SMIR.

</dd> <dt>

<span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: tutti i moduli in archivio SMIR sono stati eliminati**
</dt> <dd>

L'opzione **/p** è riuscita.

</dd> <dt>

<span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: non è stato possibile eliminare tutti i moduli in archivio SMIR**
</dt> <dd>

L'opzione **/p** non è riuscita perché non esiste una connessione archivio SMIR.

</dd> <dt>

<span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: il modulo non <module name> esiste in archivio SMIR**
</dt> <dd>

L'opzione **/d** non è riuscita perché il modulo specificato non è presente in archivio SMIR.

</dd> <dt>

<span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: MOF generato correttamente**
</dt> <dd>

Il parametro **/g** o **/GC** ha funzionato correttamente.

</dd> <dt>

<span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: non è stato possibile generare MOF**
</dt> <dd>

Il funzionamento dell'opzione **/g** o **/GC** non è riuscito a causa di nessuna connessione archivio SMIR.

</dd> <dt>

<span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: nome del modulo: <module name>**
</dt> <dd>

Questo è l'output corretto dell'opzione **/n** .

</dd> <dt>

<span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: non è stato possibile analizzare <file name> correttamente**
</dt> <dd>

Ciò indica un errore dell'opzione **/n** o **/NI** perché il file specificato non è un file MIB valido.

</dd> <dt>

<span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: elaborazione dei <number> file completata**
</dt> <dd>

Specifica il numero di file analizzati correttamente quando è stata usata l'opzione **/r** o **/auto** .

</dd> <dt>

<span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: file ripetuti nell'input per il modulo <module name> . Verrà compilato solo il file <file name>**
</dt> <dd>

L'utente ha specificato in modo esplicito più di un file nella riga di comando e due o più file hanno lo stesso modulo MIB.

</dd> <dt>

<span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: aggiunta <directory name> della directory al registro di sistema**
</dt> <dd>

Esito positivo dell'opzione **/PA** .

</dd> <dt>

<span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Impossibile aggiungere la directory <directory name> al registro di sistema**
</dt> <dd>

Errore dell'opzione **/PA** , che si verifica solo se l'API del registro di sistema ha esito negativo.

</dd> <dt>

<span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: la directory è stata eliminata <directory name> dal registro di sistema**
</dt> <dd>

Esito positivo dell'opzione **/PD** .

</dd> <dt>

<span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: non è stato possibile eliminare <directory name> dal registro di sistema**
</dt> <dd>

Errore dell'opzione **/PD** . La directory specificata non esiste nell'elenco di directory nel registro di sistema.

</dd> <dt>

<span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> non è un file MIB valido**
</dt> <dd>

Nella riga di comando è stato specificato più di un file, uno dei quali non è un file MIB valido.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



