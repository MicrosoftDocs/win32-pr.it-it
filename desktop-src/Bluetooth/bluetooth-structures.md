---
title: Strutture Bluetooth
description: In questa sezione vengono fornite le definizioni per le strutture utilizzate per la gestione dei dispositivi e dei servizi Bluetooth.
ms.assetid: bab27f5c-04c1-4fdc-91ff-249d1bfaef24
keywords:
- Bluetooth, riferimento, strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df10989e41814f6f750bdcc719f01b14ccae315
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855522"
---
# <a name="bluetooth-structures"></a>Strutture Bluetooth

In questa sezione vengono fornite le definizioni per le strutture utilizzate per la gestione dei dispositivi e dei servizi Bluetooth.

Bluetooth è supportato anche tramite l'interfaccia di programmazione Windows Sockets. Per ulteriori informazioni sulla programmazione di Bluetooth utilizzando l'interfaccia Windows Sockets, vedere [supporto di Windows Sockets per Bluetooth](windows-sockets-support-for-bluetooth.md).



| Sezione                                                                                       | Content                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_Indirizzo Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)                                               | Contiene l'indirizzo di un dispositivo Bluetooth.                                                                                      |
| [**parametri di callback di \_ autenticazione Bluetooth \_ \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authentication_callback_params) | Contiene informazioni di configurazione specifiche sul dispositivo Bluetooth che risponde a una richiesta di autenticazione.                  |
| [**\_risposta all'autenticazione \_ Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authenticate_response)                  | Contiene informazioni passate in risposta a un \_ evento di \_ richiesta di autenticazione remota BTH \_ .                                           |
| [**\_coppie di merluzzo Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_cod_pairs)                                          | Fornisce la specifica e il recupero delle informazioni di classe del dispositivo (COD) Bluetooth.                                         |
| [**\_informazioni sul dispositivo Bluetooth \_**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct)                                      | Fornisce informazioni su un dispositivo Bluetooth.                                                                                   |
| [**\_parametri di \_ ricerca del dispositivo Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_device_search_params)                   | Specifica i criteri di ricerca per le ricerche del dispositivo Bluetooth.                                                                         |
| [**\_ \_ Parametri radiofonici Find Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_find_radio_params)                         | Semplifica l'enumerazione delle radio Bluetooth installate.                                                                       |
| [**\_ \_ informazioni servizio locale \_ Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct)                       | Contiene informazioni sul servizio locale per una radio Bluetooth.                                                                        |
| [**\_informazioni sul \_ confronto \_ numerico Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_numeric_comparison_info)             | Contiene il valore numerico utilizzato per l'autenticazione tramite il confronto numerico.                                                       |
| [**\_ \_ informazioni sui dati di OOB Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_oob_data_info)                                 | Contiene i dati usati per eseguire l'autenticazione prima di stabilire un'associazione di dispositivi fuori banda.                                          |
| [**\_informazioni sulla passkey Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_passkey_info)                                    | Contiene la passkey utilizzata per l'autenticazione tramite passkey.                                                                        |
| [**\_informazioni pin \_ Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_pin_info)                                            | Contiene le informazioni usate per l'autenticazione tramite PIN.                                                                            |
| [**\_informazioni radio \_ Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_radio_info)                                        | Contiene informazioni su una radio Bluetooth.                                                                                    |
| [**\_parametri di selezione \_ dispositivo \_ Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_select_device_params)                   | Semplifica e gestisce la visibilità, l'autenticazione e la selezione di dispositivi e servizi Bluetooth.                         |
| [**\_informazioni sul dispositivo BTH \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)                                                  | Archivia le informazioni su un dispositivo Bluetooth.                                                                                     |
| [**\_ \_ informazioni evento BTH \_ HCI**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)                                           | Usato in connessione con l'ottenimento di \_ messaggi WM DEVICECHANGE per Bluetooth.                                                       |
| [**\_Informazioni sull' \_ evento \_ L2CAP di BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)                                       | Contiene i dati sugli eventi associati a un canale L2CAP.                                                        |
| [**\_dispositivo di query BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)                                                | Utilizzato quando si eseguono query per la presenza di un dispositivo Bluetooth.                                                                       |
| [**\_servizio query \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)                                              | Utilizzato per eseguire una query su un servizio Bluetooth.                                                                                               |
| [**BTH \_ Radio \_ nell' \_ intervallo**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)                                           | Archivia i dati relativi ai dispositivi Bluetooth che rientrano nell'intervallo di comunicazione.                                                     |
| [**\_servizio set \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)                                                  | Fornisce informazioni sul servizio per il servizio Bluetooth specificato.                                                                |
| [**\_dati elemento \_ SDP**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_element_data)                                                | Archivia i dati dell'elemento SDP.                                                                                                         |
| [**\_dati di \_ tipo \_ stringa SDP**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_string_type_data)                                       | Archivia informazioni sui tipi di stringa SDP.                                                                                       |
| [**SdpAttributeRange**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpattributerange)                                                | Utilizzato in una query Bluetooth per vincolare il set di attributi da restituire nella query.                                             |
| [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid)                                                          | Semplifica la ricerca di UUID.                                                                                                 |
| [**SdpQueryUuidUnion**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuidunion)                                                | Contiene l'UUID su cui eseguire una query SDP. Utilizzato insieme alla struttura [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid) . |
| [**\_BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)                                                         | Usato in combinazione con le operazioni socket Bluetooth come definito dalla \_ famiglia di indirizzi AF BTH.                                   |



 

 

 




