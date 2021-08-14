---
title: Archiviazione Funzioni dell'adapter
description: Un adattatore di archiviazione gestisce i database modello.
ms.assetid: bfb0c9e5-a95e-4054-bc83-98ff682994a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7072847c6d1ca653bd9e8edad9c51b7736354b447feeafda7c465973d4c25aea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911803"
---
# <a name="storage-adapter-functions"></a>Archiviazione Funzioni dell'adapter

Un adattatore di archiviazione gestisce i database modello. Le funzioni seguenti devono essere implementate dallo sviluppatore dell'adapter. Vengono chiamati dal Windows biometrico.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                         | Descrizione                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn)<br/>                           | Offre all Archiviazione adapter la possibilità di eseguire tutte le operazioni necessarie per portare il componente di archiviazione fuori da uno stato di inattività.<br/>         |
| [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn)<br/>                         | Aggiunge un modello al database.<br/>                                                                                             |
| [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn)<br/>                               | Aggiunge un adattatore di archiviazione alla pipeline di elaborazione dell'unità biometrica.<br/>                                                     |
| [**StorageAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn)<br/>                   | Prepara la pipeline di elaborazione dell'unità biometrica per una nuova operazione.<br/>                                                  |
| [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn)<br/>                 | Chiude il database associato alla pipeline e libera tutte le risorse correlate.<br/>                                            |
| [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn)<br/>                     | Esegue un'operazione di controllo definita dal fornitore che non richiede privilegi elevati.<br/>                                        |
| [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn)<br/> | Esegue un'operazione di controllo definita dal fornitore che richiede privilegi elevati.<br/>                                                |
| [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn)<br/>               | Crea e configura un nuovo database.<br/>                                                                                       |
| [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn)<br/>                       | Offre all Archiviazione adapter la possibilità di eseguire qualsiasi operazione necessaria per impostare il componente di archiviazione in uno stato di inattività.<br/>             |
| [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn)<br/>                   | Elimina uno o più modelli dal database.<br/>                                                                             |
| [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn)<br/>                               | Rilascia le risorse specifiche dell'adapter collegate alla pipeline.<br/>                                                                |
| [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn)<br/>                 | Cancella il database e lo contrassegna per l'eliminazione.<br/>                                                                               |
| [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn)<br/>                     | Posiziona il cursore del set di risultati sul primo record del set.<br/>                                                              |
| [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn)<br/>           | Recupera il contenuto del record corrente nel set di risultati della pipeline.<br/>                                                     |
| [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn)<br/>             | Recupera le dimensioni del database e lo spazio disponibile.<br/>                                                                             |
| [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn)<br/>                 | Recupera le informazioni sul formato e sulla versione usate dal database corrente associato alla pipeline.<br/>                          |
| [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn)<br/>               | Recupera il numero di record di modello nel set di risultati della pipeline.<br/>                                                         |
| [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn)<br/>                       | Sposta in avanti di un record il cursore del set di risultati.<br/>                                                                                |
| [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn)<br/>           | Riceve una notifica su una modifica dello stato di alimentazione del computer e prepara la scheda di archiviazione di conseguenza.<br/>               |
| [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn)<br/>                   | Apre un database per l'uso da parte dell'adattatore di archiviazione.<br/>                                                                             |
| [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn)<br/>             | Offre all Archiviazione adapter la possibilità di eseguire qualsiasi pulizia in preparazione alla chiusura del database modello.<br/>                |
| [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn)<br/>                   | Offre all Archiviazione adapter la possibilità di eseguire qualsiasi inizializzazione che rimane incompleta.<br/>                                  |
| [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn)<br/>               | Esegue una query sul database attualmente aperto per i modelli associati a un vettore di indice specificato.<br/>                          |
| [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn)<br/>               | Esegue una query sul database attualmente aperto per i modelli associati a un'identità e a un fattore secondario specificati.<br/>               |
| [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn)<br/>         | Determina le funzionalità e le limitazioni del componente di archiviazione biometrica.<br/>                                              |
| [**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)<br/>                     | Recupera un puntatore alla struttura [**WINBIO \_ STORAGE \_ INTERFACE**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface) per l'adattatore di archiviazione.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni plug-in](plug-in-functions.md)
</dt> </dl>

 

 





