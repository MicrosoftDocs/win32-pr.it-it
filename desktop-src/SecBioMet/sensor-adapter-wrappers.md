---
title: Wrapper adattatore sensore
description: Funzioni che è possibile utilizzare per chiamare funzioni sulla scheda del sensore. Queste funzioni sono definite in WinBio \_ Adapter. h.
ms.assetid: 302a831c-38f7-4d32-8d9f-5ff58931224b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8887da38a7142c830f19a83b5950abea15791b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116869"
---
# <a name="sensor-adapter-wrappers"></a>Wrapper adattatore sensore

Le funzioni wrapper seguenti sono definite in WinBio \_ Adapter. h. È possibile usarli per chiamare funzioni sulla scheda del sensore.



| Funzione                                     | Descrizione                                                                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioSensorAcceptCalibrationData<br/>   | Chiama la funzione [**SensorAdapterAcceptCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>     |
| WbioSensorActivate<br/>                | Chiama la funzione [**SensorAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                               |
| WbioSensorAttach<br/>                  | Chiama la funzione [**SensorAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn) .<br/>                                                                                                         |
| WbioSensorCancel<br/>                  | Chiama la funzione [**SensorAdapterCancel**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn) .<br/>                                                                                                         |
| WbioSensorClearContext<br/>            | Chiama la funzione [**SensorAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn) .<br/>                                                                                             |
| WbioSensorControlUnit<br/>             | Chiama la funzione [**SensorAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn) .<br/>                                                                                               |
| WbioSensorControlUnitPrivileged<br/>   | Chiama la funzione [**SensorAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn) .<br/>                                                                           |
| WbioSensorDeactivate<br/>              | Chiama la funzione [**SensorAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                           |
| WbioSensorDetach<br/>                  | Chiama la funzione [**SensorAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn) .<br/>                                                                                                         |
| WbioSensorExportSensorData<br/>        | Chiama la funzione [**SensorAdapterExportSensorData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn) .<br/>                                                                                     |
| WbioSensorFinishCapture<br/>           | Chiama la funzione [**SensorAdapterFinishCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn) .<br/>                                                                                           |
| WbioSensorNotifyPowerChange<br/>       | Chiama la funzione [**SensorAdapterNotifyPowerChange**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 8.<br/>              |
| WbioSensorPipelineCleanup<br/>         | Chiama la funzione [**SensorAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                 |
| WbioSensorPipelineInit<br/>            | Chiama la funzione [**SensorAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>                       |
| WbioSensorPushDataToEngine<br/>        | Chiama la funzione [**SensorAdapterPushDataToEngine**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn) .<br/>                                                                                     |
| WbioSensorQueryCalibrationFormats<br/> | Chiama la funzione [**SensorAdapterQueryCalibrationFormats**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/> |
| WbioSensorQueryExtendedInfo<br/>       | Chiama la funzione [**SensorAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>             |
| WbioSensorQueryStatus<br/>             | Chiama la funzione [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn) .<br/>                                                                                               |
| WbioSensorReset<br/>                   | Chiama la funzione [**SensorAdapterReset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn) .<br/>                                                                                                           |
| WbioSensorSetCalibrationFormat<br/>    | Chiama la funzione [**SensorAdapterSetCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn) .<br/> Questa funzione wrapper è supportata a partire da Windows 10.<br/>       |
| WbioSensorSetMode<br/>                 | Chiama la funzione [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn) .<br/>                                                                                                       |
| WbioSensorStartCapture<br/>            | Chiama la funzione [**SensorAdapterStartCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn) .<br/>                                                                                             |



 

Non sono disponibili funzioni wrapper per le funzioni [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn) e [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni Adattatore sensore](sensor-adapter-functions.md)
</dt> <dt>

[Funzioni plug-in](plug-in-functions.md)
</dt> </dl>

 

 





