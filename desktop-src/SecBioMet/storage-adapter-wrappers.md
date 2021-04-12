---
title: Wrapper dell'adattatore di archiviazione
description: Funzioni che è possibile utilizzare per chiamare funzioni sull'adattatore di archiviazione. Queste funzioni sono definite in WinBio \_ Adapter. h.
ms.assetid: 3e7ff098-b8f3-4745-aa75-712a392c6c78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5dfdf562546e1520ee85c5a9a0164acdff53904
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396099"
---
# <a name="storage-adapter-wrappers"></a>Wrapper dell'adattatore di archiviazione

Le funzioni wrapper seguenti sono definite in WinBio \_ Adapter. h. È possibile usarli per chiamare funzioni sull'adattatore di archiviazione.



| Funzione                                    | Descrizione                                                                                                                                                                     |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioStorageActivate<br/>              | Chiama la funzione [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                   |
| WbioStorageAddRecord<br/>             | Chiama la funzione [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn) .<br/>                                                                                       |
| WbioStorageAttach<br/>                | Chiama la funzione [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn) .<br/>                                                                                             |
| WbioStorageClearContext<br/>          | Chiama la funzione [**StorageAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn) .<br/>                                                                                 |
| WbioStorageCloseDatabase<br/>         | Chiama la funzione [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn) .<br/>                                                                               |
| WbioStorageControlUnit<br/>           | Chiama la funzione [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn) .<br/>                                                                                   |
| WbioStorageControlUnitPrivileged<br/> | Chiama la funzione [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn) .<br/>                                                               |
| WbioStorageCreateDatabase<br/>        | Chiama la funzione [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn) .<br/>                                                                             |
| WbioStorageDeactivate<br/>            | Chiama la funzione [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>               |
| WbioStorageDeleteRecord<br/>          | Chiama la funzione [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn) .<br/>                                                                                 |
| WbioStorageDetach<br/>                | Chiama la funzione [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn) .<br/>                                                                                             |
| WbioStorageEraseDatabase<br/>         | Chiama la funzione [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn) .<br/>                                                                               |
| WbioStorageFirstRecord<br/>           | Chiama la funzione [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn) .<br/>                                                                                   |
| WbioStorageGetCurrentRecord<br/>      | Chiama la funzione [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn) .<br/>                                                                         |
| WbioStorageGetDatabaseSize<br/>       | Chiama la funzione [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn) .<br/>                                                                           |
| WbioStorageGetDataFormat<br/>         | Chiama la funzione [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn) .<br/>                                                                               |
| WbioStorageGetRecordCount<br/>        | Chiama la funzione [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn) .<br/>                                                                             |
| WbioStorageNextRecord<br/>            | Chiama la funzione [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn) .<br/>                                                                                     |
| WbioStorageNotifyPowerChange<br/>     | Chiama la funzione [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 8.<br/>    |
| WbioStorageOpenDatabase<br/>          | Chiama la funzione [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn) .<br/>                                                                                 |
| WbioStoragePipelineCleanup<br/>       | Chiama la funzione [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>     |
| WbioStoragePipelineInit<br/>          | Chiama la funzione [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>           |
| WbioStorageQueryByContent<br/>        | Chiama la funzione [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn) .<br/>                                                                             |
| WbioStorageQueryBySubject<br/>        | Chiama la funzione [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn) .<br/>                                                                             |
| WbioStorageQueryExtendedInfo<br/>     | Chiama la funzione [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni adattatore di archiviazione](storage-adapter-functions.md)
</dt> <dt>

[Funzioni plug-in](plug-in-functions.md)
</dt> </dl>

 

 





