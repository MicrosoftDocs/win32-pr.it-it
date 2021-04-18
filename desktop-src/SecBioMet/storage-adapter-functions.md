---
title: Funzioni adattatore di archiviazione
description: Un adattatore di archiviazione gestisce i database modello.
ms.assetid: bfb0c9e5-a95e-4054-bc83-98ff682994a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b5b864ab37416bb215769a700bae410c9b882c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298288"
---
# <a name="storage-adapter-functions"></a>Funzioni adattatore di archiviazione

Un adattatore di archiviazione gestisce i database modello. Le funzioni seguenti devono essere implementate dallo sviluppatore dell'adattatore. Vengono chiamati dal servizio biometrico di Windows.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                         | Descrizione                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn)<br/>                           | Fornisce all'adattatore di archiviazione la possibilità di eseguire qualsiasi operazione necessaria per portare il componente di archiviazione fuori da uno stato inattivo.<br/>         |
| [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn)<br/>                         | Aggiunge un modello al database.<br/>                                                                                             |
| [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn)<br/>                               | Aggiunge un adattatore di archiviazione alla pipeline di elaborazione dell'unità biometrica.<br/>                                                     |
| [**StorageAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn)<br/>                   | Prepara la pipeline di elaborazione dell'unità biometrica per una nuova operazione.<br/>                                                  |
| [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn)<br/>                 | Chiude il database associato alla pipeline e libera tutte le risorse correlate.<br/>                                            |
| [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn)<br/>                     | Esegue un'operazione di controllo definita dal fornitore che non richiede privilegi elevati.<br/>                                        |
| [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn)<br/> | Esegue un'operazione di controllo definita dal fornitore che richiede privilegi elevati.<br/>                                                |
| [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn)<br/>               | Crea e configura un nuovo database.<br/>                                                                                       |
| [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn)<br/>                       | Fornisce all'adattatore di archiviazione la possibilità di eseguire qualsiasi operazione necessaria per impostare il componente di archiviazione in uno stato di inattività.<br/>             |
| [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn)<br/>                   | Elimina uno o più modelli dal database.<br/>                                                                             |
| [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn)<br/>                               | Rilascia le risorse specifiche dell'adapter collegate alla pipeline.<br/>                                                                |
| [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn)<br/>                 | Cancella il database e lo contrassegna per l'eliminazione.<br/>                                                                               |
| [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn)<br/>                     | Posiziona il cursore del set di risultati sul primo record nel set.<br/>                                                              |
| [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn)<br/>           | Recupera il contenuto del record corrente nel set di risultati della pipeline.<br/>                                                     |
| [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn)<br/>             | Recupera le dimensioni del database e lo spazio disponibile.<br/>                                                                             |
| [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn)<br/>                 | Recupera le informazioni sul formato e sulla versione utilizzate dal database corrente associato alla pipeline.<br/>                          |
| [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn)<br/>               | Recupera il numero di record modello nel set di risultati della pipeline.<br/>                                                         |
| [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn)<br/>                       | Sposta in avanti di un record il cursore del set di risultati.<br/>                                                                                |
| [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn)<br/>           | Riceve una notifica relativa a una modifica nello stato di alimentazione del computer e prepara l'adattatore di archiviazione di conseguenza.<br/>               |
| [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn)<br/>                   | Apre un database per l'utilizzo da parte dell'adattatore di archiviazione.<br/>                                                                             |
| [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn)<br/>             | Fornisce all'adattatore di archiviazione la possibilità di eseguire operazioni di pulizia in preparazione alla chiusura del database modello.<br/>                |
| [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn)<br/>                   | Fornisce all'adattatore di archiviazione la possibilità di eseguire qualsiasi inizializzazione che rimanga incompleta.<br/>                                  |
| [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn)<br/>               | Esegue una query sul database attualmente aperto per i modelli associati a un vettore di indice specificato.<br/>                          |
| [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn)<br/>               | Esegue una query sul database attualmente aperto per i modelli associati a un'identità e a un Sottofattore specificati.<br/>               |
| [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn)<br/>         | Determina le funzionalità e le limitazioni del componente di archiviazione biometrico.<br/>                                              |
| [**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)<br/>                     | Recupera un puntatore alla struttura [**dell' \_ \_ interfaccia di archiviazione WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface) per l'adattatore di archiviazione.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni plug-in](plug-in-functions.md)
</dt> </dl>

 

 





