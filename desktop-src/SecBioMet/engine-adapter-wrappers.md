---
title: Wrapper dell'adattatore del motore
description: Funzioni che è possibile utilizzare per chiamare funzioni sull'adattatore del motore. Queste funzioni sono definite in WinBio \_ Adapter. h.
ms.assetid: b3d6d617-e423-4ed5-9d29-be72c5dd8b49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5ec0fcc3b6ea358e8238061bc74e2933d8bf87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298707"
---
# <a name="engine-adapter-wrappers"></a>Wrapper dell'adattatore del motore

Le funzioni wrapper seguenti sono definite in WinBio \_ Adapter. h. È possibile usarli per chiamare funzioni sull'adattatore del motore.



| Funzione                                           | Descrizione                                                                                                                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioEngineAcceptSampleData<br/>              | Chiama la funzione [**EngineAdapterAcceptSampleData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn) .<br/>                                                                                                 |
| WbioEngineActivate<br/>                      | Chiama la funzione [**EngineAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_activate_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                                           |
| WbioEngineAttach<br/>                        | Chiama la funzione [**EngineAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn) .<br/>                                                                                                                     |
| WbioEngineCheckForDuplicate<br/>             | Chiama la funzione [**EngineAdapterCheckForDuplicate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn) .<br/>                                                                                               |
| WbioEngineClearContext<br/>                  | Chiama la funzione [**EngineAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn) .<br/>                                                                                                         |
| WbioEngineCommitEnrollment<br/>              | Chiama la funzione [**EngineAdapterCommitEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn) .<br/>                                                                                                 |
| WbioEngineControlUnit<br/>                   | Chiama la funzione [**EngineAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn) .<br/>                                                                                                           |
| WbioEngineControlUnitPrivileged<br/>         | Chiama la funzione [**EngineAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_privileged_fn) .<br/>                                                                                       |
| WbioEngineCreateEnrollment<br/>              | Chiama la funzione [**EngineAdapterCreateEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn) .<br/>                                                                                                 |
| WbioEngineDeactivate<br/>                    | Chiama la funzione [**EngineAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_deactivate_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                                       |
| WbioEngineDetach<br/>                        | Chiama la funzione [**EngineAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_detach_fn) .<br/>                                                                                                                     |
| WbioEngineDiscardEnrollment<br/>             | Chiama la funzione [**EngineAdapterDiscardEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn) .<br/>                                                                                               |
| WbioEngineExportEngineData<br/>              | Chiama la funzione [**EngineAdapterExportEngineData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_export_engine_data_fn) .<br/>                                                                                                 |
| WbioEngineGetEnrollmentHash<br/>             | Chiama la funzione [**EngineAdapterGetEnrollmentHash**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn) .<br/>                                                                                               |
| WbioEngineGetEnrollmentStatus<br/>           | Chiama la funzione [**EngineAdapterGetEnrollmentStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_status_fn) .<br/>                                                                                           |
| WbioEngineIdentifyAll<br/>                   | Chiama la funzione [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                                     |
| WbioEngineIdentifyFeatureSet<br/>            | Chiama la funzione [**EngineAdapterIdentifyFeatureSet**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn) .<br/>                                                                                             |
| WbioEngineNotifyPowerChange<br/>             | Chiama la funzione [*EngineAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_notify_power_change_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 8.<br/>                            |
| WbioEnginePipelineCleanup<br/>               | Chiama la funzione [**EngineAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_cleanup_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                             |
| WbioEnginePipelineInit<br/>                  | Chiama la funzione [**EngineAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_init_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                                   |
| WbioEngineQueryCalibrationData<br/>          | Chiama la funzione [**EngineAdapterQueryCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_calibration_data_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                   |
| WbioEngineQueryExtendedEnrollmentStatus<br/> | Chiama la funzione [**EngineAdapterQueryExtendedEnrollmentStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/> |
| WbioEngineQueryExtendedInfo<br/>             | Chiama la funzione [**EngineAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                         |
| WbioEngineQueryHashAlgorithms<br/>           | Chiama la funzione [**EngineAdapterQueryHashAlgorithms**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn) .<br/>                                                                                           |
| WbioEngineQueryIndexVectorSize<br/>          | Chiama la funzione [**EngineAdapterQueryIndexVectorSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_index_vector_size_fn) .<br/>                                                                                         |
| WbioEngineQueryPreferredFormat<br/>          | Chiama la funzione [**EngineAdapterQueryPreferredFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_preferred_format_fn) .<br/>                                                                                         |
| WbioEngineQuerySampleHint<br/>               | Chiama la funzione [**EngineAdapterQuerySampleHint**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_sample_hint_fn) .<br/>                                                                                                   |
| WbioEngineRefreshCache<br/>                  | Chiama la funzione [**EngineAdapterRefreshCache**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_refresh_cache_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                                   |
| WbioEngineSelectCalibrationFormat<br/>       | Chiama la funzione [**EngineAdapterSelectCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_select_calibration_format_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>             |
| WbioEngineSetAccountPolicy<br/>              | Chiama la funzione [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                           |
| WbioEngineSetEnrollmentParameters<br/>       | Chiama la funzione [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>             |
| WbioEngineSetEnrollmentSelector<br/>         | Chiama la funzione [**EngineAdapterSetEnrollmentSelector**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_selector_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                 |
| WbioEngineSetHashAlgorithm<br/>              | Chiama la funzione [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) .<br/>                                                                                                 |
| WbioEngineUpdateEnrollment<br/>              | Chiama la funzione [**EngineAdapterUpdateEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn) .<br/>                                                                                                 |
| WbioEngineVerifyFeatureSet<br/>              | Chiama la funzione [**EngineAdapterVerifyFeatureSet**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_verify_feature_set_fn) .<br/>                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni dell'adattatore del motore](engine-adapter-functions.md)
</dt> <dt>

[Funzioni plug-in](plug-in-functions.md)
</dt> </dl>

 

 





