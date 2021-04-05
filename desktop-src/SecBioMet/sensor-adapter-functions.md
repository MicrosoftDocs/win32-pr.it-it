---
title: Funzioni Adattatore sensore
description: Un adattatore del sensore esegue il wrapping di un dispositivo biometrico e fornisce un'interfaccia standard che consente al servizio biometrico di Windows di configurare il sensore, acquisire esempi e controllare il flusso dei dati biometrici nel motore di elaborazione.
ms.assetid: 32cf28d3-cb78-442d-81db-7827f55b0ba8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cefc5e9221a56a7766e6af6a47449db4405b369
ms.sourcegitcommit: 8a30948ba97ab969fcaa7f7ff05b853f59d8bd5c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/14/2020
ms.locfileid: "103724323"
---
# <a name="sensor-adapter-functions"></a>Funzioni Adattatore sensore

Un adattatore del sensore esegue il wrapping di un dispositivo biometrico e fornisce un'interfaccia standard che consente al servizio biometrico di Windows di configurare il sensore, acquisire esempi e controllare il flusso dei dati biometrici nel motore di elaborazione. Le funzioni seguenti devono essere implementate dallo sviluppatore dell'adapter. Vengono chiamati dal servizio biometrico di Windows.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                           | Descrizione                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SensorAdapterAcceptCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn)<br/>     | Passa i dati di calibrazione dall'adattatore del motore alla scheda del sensore.<br/>                                                                                            |
| [**SensorAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn)<br/>                               | Fornisce all'adattatore del sensore la possibilità di eseguire qualsiasi lavoro necessario per riportare il componente del sensore fuori da uno stato inattivo.<br/>                                                |
| [**SensorAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn)<br/>                                   | Aggiunge un adattatore del sensore alla pipeline di elaborazione dell'unità biometrica.<br/>                                                                                           |
| [**SensorAdapterCancel**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn)<br/>                                   | Annulla tutte le operazioni del sensore in sospeso.<br/>                                                                                                                            |
| [**SensorAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn)<br/>                       | Prepara la pipeline di elaborazione dell'unità biometrica per una nuova operazione.<br/>                                                                                       |
| [**SensorAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn)<br/>                         | Esegue un'operazione di controllo definita dal fornitore che non richiede privilegi elevati.<br/>                                                                             |
| [**SensorAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn)<br/>     | Esegue un'operazione di controllo definita dal fornitore che richiede privilegi elevati.<br/>                                                                                     |
| [**SensorAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn)<br/>                           | Fornisce all'adattatore del sensore la possibilità di eseguire qualsiasi lavoro necessario per impostare il componente del sensore in uno stato di inattività.<br/>                                                    |
| [**SensorAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn)<br/>                                   | Rilascia le risorse specifiche dell'adapter collegate alla pipeline.<br/>                                                                                                     |
| [**SensorAdapterExportSensorData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn)<br/>               | Recupera l'esempio di biometrico acquisito più di recente formattato come struttura [**WINBIO \_ Bir**](winbio-bir.md) standard.<br/>                                        |
| [**SensorAdapterFinishCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn)<br/>                     | Chiamato dal Windows Biometric Framework per attendere il completamento di un'operazione di acquisizione avviata dalla funzione SensorAdapterStartCapture.<br/>                                                                                       |
| [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)<br/>           | Recupera un valore che indica se l'indicatore del sensore è on o off.<br/>                                                                                       |
| [*SensorAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn)<br/>               | Riceve una notifica relativa a una modifica nello stato di alimentazione del computer e prepara la scheda del sensore di conseguenza.<br/>                                                     |
| [**SensorAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn)<br/>                 | Fornisce all'adattatore del sensore la possibilità di eseguire operazioni di pulizia in che richiedono assistenza dai componenti del motore o dell'adattatore di archiviazione.<br/>                                   |
| [**SensorAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn)<br/>                       | Fornisce all'adattatore del sensore la possibilità di eseguire qualsiasi inizializzazione che rimanga incompleta e che richiede assistenza per i componenti del motore o dell'adattatore di archiviazione.<br/> |
| [**SensorAdapterPushDataToEngine**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn)<br/>               | Rende disponibile il contenuto corrente del buffer di esempio per l'adattatore del motore.<br/>                                                                                  |
| [**SensorAdapterQueryCalibrationFormats**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn)<br/> | Determina il set di formati di calibrazione supportati dall'adattatore del sensore.<br/>                                                                                        |
| [**SensorAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn)<br/>             | Determina le funzionalità e le limitazioni del componente sensore biometrico.<br/>                                                                                    |
| [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)<br/>                         | Recupera le informazioni sullo stato corrente del dispositivo del sensore.<br/>                                                                                              |
| [**SensorAdapterReset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn)<br/>                                     | Reinizializza il sensore.<br/>                                                                                                                                         |
| [**SensorAdapterSetCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn)<br/>       | Notifica all'adattatore del sensore che è stato selezionato un particolare formato dati di calibrazione dall'adattatore del motore.<br/>                                                    |
| [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)<br/>           | Attiva o disattiva l'indicatore del sensore.<br/>                                                                                                                           |
| [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn)<br/>                                 | Imposta la modalità adattatore del sensore.<br/>                                                                                                                                     |
| [**SensorAdapterStartCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn)<br/>                       | Inizia un'acquisizione di biometrica asincrona.<br/>                                                                                                                         |
| [**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)<br/>                         | Recupera un puntatore alla struttura [**dell' \_ \_ interfaccia del sensore WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface) per l'adattatore del sensore.<br/>                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni plug-in](plug-in-functions.md)
</dt> </dl>

 

 





