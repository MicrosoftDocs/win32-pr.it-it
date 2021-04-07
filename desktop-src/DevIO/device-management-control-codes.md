---
description: I codici di controllo seguenti vengono usati con i dispositivi Changer.
ms.assetid: b3a3ffa1-e710-4d96-aff8-5b6876ab032b
title: Codici di controllo della gestione dei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bd6aa147407618c6df82686f175cb92690ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049242"
---
# <a name="device-management-control-codes"></a>Codici di controllo della gestione dei dispositivi

I codici di controllo seguenti vengono usati con i dispositivi Changer.



| Valore                                                                                          | Significato                                                                                                                                              |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_media Changer \_ cambio \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_exchange_medium)                      | Sposta un elemento multimediale da un elemento di origine a una destinazione e la parte di supporti originariamente nella prima destinazione a una seconda destinazione. |
| [**\_ \_ \_ stato elemento Get Changer \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_element_status)               | Recupera lo stato di tutti gli elementi o di un numero specificato di elementi di un determinato tipo.                                                         |
| [**\_ \_ parametri Get del Changer IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_parameters)                        | Recupera i parametri del dispositivo specificato.                                                                                                    |
| [**\_Changer IOCTL \_ ottenere \_ \_ i dati del prodotto**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_product_data)                   | Recupera i dati del prodotto per il dispositivo specificato.                                                                                                 |
| [**\_ \_ stato Get Changer \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_status)                                | Recupera lo stato corrente del dispositivo specificato.                                                                                                |
| [**\_ \_ stato elemento inizializzatore IOCTL Changer \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_initialize_element_status) | Inizializza lo stato di tutti gli elementi o gli elementi specificati di un determinato tipo.                                                               |
| [**\_spostamento del commutatore IOCTL \_ \_ medio**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_move_medium)                              | Sposta un elemento multimediale in una destinazione.                                                                                                             |
| [**\_tag del \_ volume di query del commutatore IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_query_volume_tags)                 | Recupera le informazioni relative ai tag del volume per gli elementi specificati.                                                                                     |
| [**\_REinizializzazione del commutatore IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_reinitialize_transport)        | Ricalibra fisicamente un elemento trasporto.                                                                                                         |
| [**\_ \_ accesso al set di Changer IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_access)                                | Imposta lo stato della porta di inserimento/espulsione del dispositivo, dello sportello o della tastiera.                                                                                   |
| [**\_posizione del \_ set di Changer IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_position)                            | Imposta il meccanismo di trasporto robotizzato del juke-through sull'indirizzo dell'elemento specificato.                                                                     |



 

I codici di controllo seguenti vengono usati con la gestione dei dispositivi.



| Codice di controllo                                                                                      | Operazione                                                                                                    |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Verifica \_ archiviazione \_ IOCTL \_ Verifica**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_check_verify)                               | Verifica la presenza di modifiche in un dispositivo multimediale rimovibile.                                                               |
| [**\_supporto di \_ rimozione dell'archiviazione IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_eject_media)                                 | Espelle i supporti da un dispositivo SCSI.                                                                             |
| [**\_controllo di \_ espulsione dell'archiviazione IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_ejection_control)                       | Abilita o Disabilita il meccanismo che espelle i supporti.                                                         |
| [**\_numero di \_ \_ dispositivo Get archiviazione IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_device_number)                    | Recupera il tipo di dispositivo, il numero di dispositivo e, per un dispositivo partizionabile, il numero di partizione di un dispositivo. |
| [**\_Archivio IOCTL \_ ottenere \_ informazioni su HOTPLUG \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_hotplug_info)                      | Recupera la configurazione hotplug del dispositivo specificato.                                                 |
| [**\_numero di \_ \_ serie supporti \_ \_ per archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)       | Recupera il numero di serie di un dispositivo USB.                                                                 |
| [**\_tipi di supporti di archiviazione IOCTL \_ get \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types)                        | Recupera le informazioni sulla geometria del dispositivo.                                                            |
| [**\_archiviazione IOCTL \_ ottenere i tipi di \_ supporto \_ \_ es.**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types_ex)                 | Recupera le informazioni sui tipi di supporto supportati da un dispositivo.                                        |
| [**\_supporto di \_ caricamento dell'archiviazione IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_load_media)                                   | Carica i file multimediali in un dispositivo.                                                                                   |
| [**archiviazione IOCTL- \_ \_ Gestisci \_ \_ attributi set di dati \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_manage_data_set_attributes) |                                                                                                              |
| [**\_ \_ controllo MCN di archiviazione IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_mcn_control)                                 | Abilita o Disabilita la notifica di modifica del supporto.                                                               |
| [**\_rimozione del \_ supporto di archiviazione IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_media_removal)                             | Abilita o Disabilita il meccanismo di espulsione dei supporti.                                                               |
| [**\_ \_ capacità lettura archiviazione \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)                             | Recupera le informazioni sulla geometria per il dispositivo.                                                           |
| [**\_informazioni sul set di archiviazione IOCTL \_ \_ informazioni su HOTPLUG \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_set_hotplug_info)                      | Imposta la configurazione di hotplug del dispositivo specificato.                                                      |



 

 

 



