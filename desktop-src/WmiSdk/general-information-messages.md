---
description: I messaggi informativi seguenti descrivono l'operazione del compilatore.
ms.assetid: 838e598d-871d-4015-a372-4d94cacf8048
ms.tgt_platform: multiple
title: Messaggi informativi generali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680bcf7c2b9cbea5e60d13a7dd2aa6be93d9fad0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882723"
---
# <a name="general-information-messages"></a>Messaggi informativi generali

I messaggi informativi seguenti descrivono l'operazione del compilatore.

<dl> <dt>

<span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: versione <versione \#> definizioni MIB compilate da <file name>**
</dt> <dd>

Questo messaggio viene visualizzato all'inizio di ogni compilazione di file. Ciò significa che il file potrebbe essere stato specificato in modo esplicito nella riga di comando dall'utente oppure che è stato estratto dal compilatore dalle directory di inclusione del Registro di sistema o dalle directory di inclusione indicate nella riga di comando.

</dd> <dt>

<span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Controllo della sintassi non riuscito in <file name>**
</dt> <dd>

I messaggi di errore specifici che precedono questo messaggio forniscono la natura degli errori di sintassi.

</dd> <dt>

<span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Controllo semantico non riuscito in <file name>**
</dt> <dd>

I messaggi di errore specifici che precedono questo messaggio forniscono la natura degli errori semantici.

</dd> <dt>

<span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: Non è stato possibile caricare <file name> nel controllo**
</dt> <dd>

Controllo semantico o sintassi non riuscito nel modulo oppure l'interazione SMIR non è stata completata.

</dd> <dt>

<span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Controllo della sintassi riuscito in <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Controllo semantico riuscito in <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: caricato <file name> correttamente nello smir**
</dt> <dd></dd> <dt>

<span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: Impossibile risolvere uno o più simboli in <module name>**
</dt> <dd>

I moduli corrispondenti a uno o più simboli importati nel modulo specificato non sono stati trovati o non possono essere compilati.

</dd> <dt>

<span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: Impossibile connettersi a SMIR**
</dt> <dd>

Assicurarsi che Smir.dll esistente, che sia stato registrato usando il comando regsvr32 e che il server di Strumentazione gestione Windows (WMI) sia operativo.

</dd> <dt>

<span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: Modules in the SMIR: <list of modules, 1 on each line>**
</dt> <dd>

Questo è l'output **dell'opzione /l.**

</dd> <dt>

<span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir Non è stato possibile elencare i moduli in SMIR**
</dt> <dd>

Ciò indica un errore dell'opzione **/l** a causa di nessuna connessione SMIR.

</dd> <dt>

<span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: Modulo eliminato <module name> correttamente**
</dt> <dd>

**L'opzione /d** ha avuto esito positivo.

</dd> <dt>

<span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: Non è stato possibile eliminare il modulo <module name>**
</dt> <dd>

Ciò indica un errore dell'opzione **/d** a causa di nessuna connessione SMIR.

</dd> <dt>

<span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Sono stati eliminati tutti i moduli in SMIR**
</dt> <dd>

**L'opzione /p** ha avuto esito positivo.

</dd> <dt>

<span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Non è stato possibile eliminare tutti i moduli in SMIR**
</dt> <dd>

**L'opzione /p** non è riuscita perché non è presente alcuna connessione SMIR.

</dd> <dt>

<span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: Il <module name> modulo non esiste in SMIR**
</dt> <dd>

**L'opzione /d** non è riuscita perché il modulo specificato non è in SMIR.

</dd> <dt>

<span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: MoF generato correttamente**
</dt> <dd>

**L'opzione /g** o **/gc** ha funzionato correttamente.

</dd> <dt>

<span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: Impossibile generare MOF**
</dt> <dd>

**L'opzione /g** o **/gc** non funziona correttamente a causa di nessuna connessione SMIR.

</dd> <dt>

<span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: nome del modulo: <module name>**
</dt> <dd>

Si tratta dell'output corretto **dell'opzione /n.**

</dd> <dt>

<span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: Impossibile analizzare <file name> correttamente**
</dt> <dd>

Ciò indica un errore **dell'opzione /n** **o /ni** perché il file specificato non è un file MIB valido.

</dd> <dt>

<span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: Elaborazione &lt; dei file &gt; numerici completata**
</dt> <dd>

Specifica il numero di file analizzati correttamente quando è stata usata l'opzione **/r** o **/auto.**

</dd> <dt>

<span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: file ripetuti nell'input per il modulo <module name> . Verrà compilato <file name> solo il file**
</dt> <dd>

L'utente ha specificato in modo esplicito più di un file nella riga di comando e due o più di questi file hanno lo stesso modulo MIB.

</dd> <dt>

<span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Aggiunta della directory <directory name> al Registro di sistema**
</dt> <dd>

Esito positivo **dell'opzione /pa.**

</dd> <dt>

<span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Impossibile aggiungere la directory <directory name> al Registro di sistema**
</dt> <dd>

Errore **dell'opzione /pa,** che si verifica solo se l'API del Registro di sistema non riesce.

</dd> <dt>

<span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: directory <directory name> eliminata dal Registro di sistema**
</dt> <dd>

Esito positivo **dell'opzione /pd.**

</dd> <dt>

<span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Impossibile eliminare <directory name> dal Registro di sistema**
</dt> <dd>

Errore **dell'opzione /pd.** La directory specificata non esiste nell'elenco delle directory nel Registro di sistema.

</dd> <dt>

<span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> non è un file mib valido**
</dt> <dd>

Nella riga di comando è stato specificato più di un file, uno dei quali non è un file MIB valido.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dell'ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



