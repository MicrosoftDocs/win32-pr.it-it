---
description: Codici di controllo usati per la gestione dei file.
ms.assetid: e27ded4b-d104-4244-b38e-5fed10d32e1e
title: Codici di controllo della gestione dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cb3baf78c4066a640242afe8465592bc9a6f8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884886"
---
# <a name="file-management-control-codes"></a>Codici di controllo della gestione dei file

I codici di controllo seguenti vengono usati per la gestione dei file.

## <a name="in-this-section"></a>Contenuto della sezione



| Codice di controllo                                                                                    | Descrizione                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ allow \_ Extended \_ DASD \_ io**](/windows/win32/api/winioctl/ni-winioctl-fsctl_allow_extended_dasd_io)<br/>             | Segnala al driver file system di non eseguire alcun controllo dei limiti di I/O sulle chiamate di lettura o scrittura della partizione.<br/>                                                                                  |
| [**FSCTL \_ creare \_ o \_ ottenere \_ l' \_ ID oggetto**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)<br/>          | Recupera l'identificatore di oggetto per il file o la directory specificata. Se non esiste alcun identificatore di oggetto, l'uso di **FSCTL \_ Create \_ o \_ get \_ Object \_ ID** ne crea uno.<br/>                           |
| [**\_controllo CSV \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control)<br/>                                     | Recupera i risultati di un'operazione di controllo CSV.<br/>                                                                                                                                        |
| [**\_ \_ ID oggetto Delete \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)<br/>                          | Rimuove l'identificatore di oggetto da un file o da una directory specificata.<br/>                                                                                                                        |
| [**FSCTL \_ gli \_ extent duplicati \_ nel \_ file**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)<br/>       | Indica al file system di copiare un intervallo di byte di file per conto di un'applicazione.<br/>                                                                                                     |
| [**\_trim a \_ livello di file FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_file_level_trim)<br/>                            | Indica al sistema di archiviazione che non è necessario archiviare gli intervalli del file.<br/>                                                                                                    |
| [**FSCTL \_ filesystem \_ get \_ Statistics**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics)<br/>        | Recupera le informazioni da vari contatori delle prestazioni file system.<br/>                                                                                                                 |
| [**FSCTL \_ filesystem \_ get \_ Statistics \_ es**](/windows/win32/api/winioctl/ni-winioctl-fsctl_filesystem_get_statistics_ex)<br/> | Recupera le informazioni da vari contatori delle prestazioni file system.<br/> Il supporto per questo codice di controllo è stato avviato con Windows 10.<br/>                                               |
| [**FSCTL \_ trovare \_ i file \_ per \_ SID**](/windows/win32/api/winioctl/ni-winioctl-fsctl_find_files_by_sid)<br/>                       | Cerca in una directory un file il cui proprietario dell'autore corrisponda al SID specificato.<br/>                                                                                                           |
| [**\_compressione FSCTL Get \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)<br/>                             | Recupera lo stato di compressione corrente di un file o di una directory in un volume il cui file system supporta la compressione per flusso.<br/>                                                            |
| [**FSCTL \_ ottenere \_ un \_ record di file NTFS \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_file_record)<br/>                 | Recupera il primo record di file in uso ed è di un valore ordinale minore o uguale al numero di riferimento del file richiesto.<br/>                                                    |
| [**\_ \_ ID oggetto FSCTL \_ Get**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)<br/>                                | Recupera l'identificatore di oggetto per il file o la directory specificata.<br/>                                                                                                                     |
| [**FSCTL \_ ottenere la \_ riparazione**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)<br/>                                       | Recupera le informazioni sul meccanismo di correzione automatica del file system NTFS.<br/>                                                                                                               |
| [**\_ripristino di avvio \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)<br/>                             | Attiva il file system NTFS per avviare un ciclo di correzione automatica in un singolo file.<br/>                                                                                                            |
| [**FSCTL \_ rende \_ compatibili i supporti \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)<br/>                | Chiude una sessione UDF aperta su un supporto di scrittura-una volta per rendere compatibile il supporto ROM.<br/>                                                                                                         |
| [**\_ \_ chiusura ACK FSCTL \_ OPBATCH \_ in sospeso**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)<br/>       | Notifica a un server che un'applicazione client è pronta per chiudere un file.<br/>                                                                                                                    |
| [**FSCTL \_ blocco opportunistico \_ break \_ ACK \_ No \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)<br/>              | Risponde alla notifica che un blocco opportunistico su un file sta per essere violato. Usare questa operazione per sbloccare tutti i blocchi opportunistici sul file, mantenendo il file aperto.<br/>            |
| [**\_conferma FSCTL \_ blocco opportunistico \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)<br/>          | Risponde alla notifica che un blocco opportunistico esclusivo su un file sta per essere violato. Utilizzare questa operazione per indicare che il file deve ricevere un blocco opportunistico di livello 2.<br/> |
| [**notifica di FSCTL \_ blocco opportunistico \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)<br/>                    | Consente all'applicazione chiamante di attendere il completamento di un'arresto di blocco opportunistico.<br/>                                                                                                   |
| [**\_ \_ intervalli allocati per le query FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)<br/>              | Analizza un file o un flusso alternativo che cerca gli intervalli che possono contenere dati diversi da zero.<br/>                                                                                                       |
| [**\_query FSCTL \_ su \_ informazioni sul volume del disco \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)<br/>      | Richiede informazioni sul volume specifiche della funzione definita dall'utente.<br/>                                                                                                                                                |
| [**informazioni su FSCTL \_ query \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)<br/>                      | Recupera le proprietà di gestione dei difetti del volume. Utilizzato per i file System UDF.<br/>                                                                                                     |
| [**\_file di richiamo FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_recall_file)<br/>                                     | Richiama un file dal supporto di archiviazione gestito da archiviazione remota, ovvero il software di gestione dell'archiviazione gerarchico.<br/>                                                                    |
| [**\_ \_ blocco opportunistico batch richieste \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)<br/>                  | Richiede un blocco opportunistico batch su un file.<br/>                                                                                                                                           |
| [**\_ \_ blocco opportunistico filtro richieste \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)<br/>                | Richiede un blocco opportunistico di filtro su un file.<br/>                                                                                                                                          |
| [**\_blocco opportunistico richiesta \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)<br/>                               | Richiede un blocco opportunistico (blocco opportunistico) su un file e conferma che si è verificata un'eccezione blocco opportunistico.<br/>                                                                                    |
| [**FSCTL \_ richiesta \_ blocco opportunistico \_ livello \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)<br/>             | Richiede un blocco opportunistico di livello 1 su un file.<br/>                                                                                                                                         |
| [**FSCTL \_ richiesta \_ blocco opportunistico \_ livello \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)<br/>             | Richiede un blocco opportunistico di livello 2 su un file.<br/>                                                                                                                                         |
| [**\_compressione FSCTL set \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                             | Imposta lo stato di compressione di un file o di una directory in un volume il cui file system supporta la compressione per file e per directory.<br/>                                                         |
| [**\_ \_ \_ gestione dei difetti della serie FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)<br/>                | Imposta lo stato di gestione dei difetti software per il file specificato. Utilizzato per i file System UDF.<br/>                                                                                             |
| [**\_ \_ ID oggetto set \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)<br/>                                | Imposta l'identificatore di oggetto per il file o la directory specificata.<br/>                                                                                                                          |
| [**\_ \_ ID oggetto set \_ FSCTL \_ esteso**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)<br/>             | Modifica i dati utente associati all'identificatore di oggetto per il file o la directory specificata.<br/>                                                                                            |
| [**FSCTL \_ impostare il \_ ripristino**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)<br/>                                       | Imposta la modalità della funzionalità di correzione automatica di un file system NTFS.<br/>                                                                                                                          |
| [**FSCTL \_ set \_ sparse**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)<br/>                                       | Contrassegna il file indicato come sparse o non di tipo sparse. In un file sparse, i grandi intervalli di zeri potrebbero non richiedere l'allocazione dei dischi.<br/>                                                               |
| [**FSCTL ha \_ impostato \_ zero \_ dati**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)<br/>                                | Compila un intervallo specificato di un file con zeri (0).<br/>                                                                                                                                        |
| [**FSCTL \_ imposta \_ zero \_ per la \_ deallocazione**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_on_deallocation)<br/>         | Indica che i cluster di un handle di file di file system NTFS devono essere riempiti con zeri quando vengono deallocati.<br/>                                                                             |
| [**FSCTL \_ attendere \_ la \_ riparazione**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)<br/>                            | Restituisce il momento in cui vengono completate le riparazioni specificate.<br/>                                                                                                                                        |



 

I codici di controllo seguenti vengono utilizzati con la [compressione e la decompressione di file](file-compression-and-decompression.md).

<dl>

[**\_compressione FSCTL Get \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression)  
[**\_compressione FSCTL set \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)  
</dl>

Con gli [identificatori di oggetto](distributed-link-tracking-and-object-identifiers.md)vengono usati i codici di controllo seguenti.

<dl>

[**FSCTL \_ creare \_ o \_ ottenere \_ l' \_ ID oggetto**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_or_get_object_id)  
[**\_ \_ ID oggetto Delete \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_object_id)  
[**\_ \_ ID oggetto FSCTL \_ Get**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_object_id)  
[**\_ \_ ID oggetto set \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id)  
[**\_ \_ ID oggetto set \_ FSCTL \_ esteso**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_object_id_extended)  
</dl>

I codici di controllo seguenti vengono utilizzati con [blocchi opportunistici](opportunistic-locks.md).

<dl>

[**\_ \_ chiusura ACK FSCTL \_ OPBATCH \_ in sospeso**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**FSCTL \_ blocco opportunistico \_ break \_ ACK \_ No \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**\_conferma FSCTL \_ blocco opportunistico \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**notifica di FSCTL \_ blocco opportunistico \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**\_ \_ blocco opportunistico batch richieste \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**\_ \_ blocco opportunistico filtro richieste \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**\_blocco opportunistico richiesta \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**FSCTL \_ richiesta \_ blocco opportunistico \_ livello \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**FSCTL \_ richiesta \_ blocco opportunistico \_ livello \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

I codici di controllo seguenti vengono utilizzati con [i file sparse](sparse-files.md).

<dl>

[**\_ \_ intervalli allocati per le query FSCTL \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges)  
[**FSCTL \_ set \_ sparse**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)  
[**FSCTL ha \_ impostato \_ zero \_ dati**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)  
</dl>

I codici di controllo seguenti vengono utilizzati con il meccanismo di correzione automatica NTFS.

<dl>

[**FSCTL \_ ottenere la \_ riparazione**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_repair)  
[**\_ripristino di avvio \_ FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_initiate_repair)  
[**FSCTL \_ impostare il \_ ripristino**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_repair)  
[**FSCTL \_ attendere \_ la \_ riparazione**](/windows/win32/api/winioctl/ni-winioctl-fsctl_wait_for_repair)  
</dl>

I codici di controllo seguenti vengono usati con la funzione definita dall'utente.

<dl>

[**FSCTL \_ rende \_ compatibili i supporti \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_make_media_compatible)  
[**\_query FSCTL \_ su \_ informazioni sul volume del disco \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_on_disk_volume_info)  
[**informazioni su FSCTL \_ query \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_sparing_info)  
[**\_ \_ \_ gestione dei difetti della serie FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_defect_management)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici di controllo della gestione delle directory](directory-management-control-codes.md)
</dt> <dt>

[Codici di controllo della gestione del volume](volume-management-control-codes.md)
</dt> </dl>

 

