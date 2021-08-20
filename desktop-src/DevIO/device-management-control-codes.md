---
description: I codici di controllo seguenti vengono usati con i dispositivi di modifica.
ms.assetid: b3a3ffa1-e710-4d96-aff8-5b6876ab032b
title: Codici di controllo per la gestione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1cc7c254524bc942a146f785a37a7a26531152058b4643f76d618f28e5d3a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004609"
---
# <a name="device-management-control-codes"></a>Codici di controllo per la gestione dei dispositivi

I codici di controllo seguenti vengono usati con i dispositivi di modifica.



| Valore                                                                                          | Significato                                                                                                                                              |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOCTL \_ CHANGER \_ EXCHANGE \_ MEDIUM**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_exchange_medium)                      | Sposta un elemento multimediale da un elemento di origine a una destinazione e il supporto originariamente nella prima destinazione a una seconda destinazione. |
| [**IOCTL \_ CHANGER \_ GET \_ ELEMENT \_ STATUS**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_element_status)               | Recupera lo stato di tutti gli elementi o di un numero specificato di elementi di un tipo specifico.                                                         |
| [**PARAMETRI GET DI IOCTL \_ CHANGER \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_parameters)                        | Recupera i parametri del dispositivo specificato.                                                                                                    |
| [**IOCTL \_ CHANGER \_ GET \_ PRODUCT \_ DATA**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_product_data)                   | Recupera i dati del prodotto per il dispositivo specificato.                                                                                                 |
| [**IOCTL \_ CHANGER \_ GET \_ STATUS**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_status)                                | Recupera lo stato corrente del dispositivo specificato.                                                                                                |
| [**STATO DELL'ELEMENTO INITIALIZE DI IOCTL \_ CHANGER \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_initialize_element_status) | Inizializza lo stato di tutti gli elementi o gli elementi specificati di un tipo specifico.                                                               |
| [**IOCTL \_ CHANGER \_ MOVE \_ MEDIUM**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_move_medium)                              | Sposta un elemento multimediale in una destinazione.                                                                                                             |
| [**TAG DEL VOLUME \_ DI \_ QUERY DI IOCTL CHANGER \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_query_volume_tags)                 | Recupera le informazioni sui tag di volume per gli elementi specificati.                                                                                     |
| [**IOCTL \_ CHANGER \_ REINITIALIZE \_ TRANSPORT**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_reinitialize_transport)        | Ricalibra fisicamente un elemento di trasporto.                                                                                                         |
| [**IOCTL \_ CHANGER \_ SET \_ ACCESS**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_access)                                | Imposta lo stato della porta di inserimento/espulso del dispositivo, della porta o del tastierino.                                                                                   |
| [**POSIZIONE SET \_ DI IOCTL CHANGER \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_position)                            | Imposta il meccanismo di trasporto robotico del modificatore sull'indirizzo dell'elemento specificato.                                                                     |



 

I codici di controllo seguenti vengono usati con la gestione dei dispositivi.



| Codice di controllo                                                                                      | Operazione                                                                                                    |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**VERIFICA CONTROLLO \_ ARCHIVIAZIONE IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_check_verify)                               | Verifica la presenza di modifiche in un dispositivo con supporti rimovibili.                                                               |
| [**IOCTL \_ STORAGE \_ EJECT \_ MEDIA**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_eject_media)                                 | Espulse supporti da un dispositivo SCSI.                                                                             |
| [**CONTROLLO \_ \_ DELL'EJECTION DI ARCHIVIAZIONE IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_ejection_control)                       | Abilita o disabilita il meccanismo che espulse i supporti.                                                         |
| [**IOCTL \_ STORAGE \_ GET \_ DEVICE \_ NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_device_number)                    | Recupera il tipo di dispositivo, il numero di dispositivo e, per un dispositivo partizionabile, il numero di partizione di un dispositivo. |
| [**IOCTL \_ STORAGE \_ GET \_ HOTPLUG \_ INFO**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_hotplug_info)                      | Recupera la configurazione hotplug del dispositivo specificato.                                                 |
| [**IOCTL \_ STORAGE \_ GET \_ MEDIA \_ SERIAL \_ NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)       | Recupera il numero di serie di un dispositivo USB.                                                                 |
| [**IOCTL \_ STORAGE \_ GET \_ MEDIA \_ TYPES**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types)                        | Recupera le informazioni sulla geometria del dispositivo.                                                            |
| [**IOCTL \_ STORAGE \_ GET \_ MEDIA \_ TYPES \_ EX**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types_ex)                 | Recupera informazioni sui tipi di supporti supportati da un dispositivo.                                        |
| [**SUPPORTO DI CARICAMENTO ARCHIVIAZIONE IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_load_media)                                   | Carica i supporti in un dispositivo.                                                                                   |
| [**GESTIONE DEGLI ATTRIBUTI \_ DEL SET DI DATI \_ \_ \_ NELL'ARCHIVIAZIONE \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_manage_data_set_attributes) |                                                                                                              |
| [**CONTROLLO MCN DI ARCHIVIAZIONE IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_mcn_control)                                 | Abilita o disabilita la notifica di modifica dei supporti.                                                               |
| [**RIMOZIONE DEI SUPPORTI DI ARCHIVIAZIONE IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_media_removal)                             | Abilita o disabilita il meccanismo di inserimento dei supporti.                                                               |
| [**CAPACITÀ DI LETTURA \_ DELL'ARCHIVIAZIONE IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)                             | Recupera le informazioni sulla geometria per il dispositivo.                                                           |
| [**IOCTL \_ STORAGE \_ SET \_ HOTPLUG \_ INFO**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_set_hotplug_info)                      | Imposta la configurazione hotplug del dispositivo specificato.                                                      |



 

 

 



