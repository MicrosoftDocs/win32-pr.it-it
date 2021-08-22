---
title: Bluetooth Strutture
description: Questa sezione fornisce le definizioni per le strutture usate per la gestione Bluetooth dispositivi e servizi.
ms.assetid: bab27f5c-04c1-4fdc-91ff-249d1bfaef24
keywords:
- Bluetooth, riferimento, strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a2208902360b4f1161f9586e41f59f062972efbbba7eeb0cfb8ffbbc3c6b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588281"
---
# <a name="bluetooth-structures"></a>Bluetooth Strutture

Questa sezione fornisce le definizioni per le strutture usate per la gestione Bluetooth dispositivi e servizi.

Bluetooth è supportato anche tramite l'interfaccia di programmazione Windows Sockets. Per altre informazioni sulla programmazione Bluetooth tramite l'interfaccia Windows Sockets, vedere Supporto [di Windows Sockets per Bluetooth](windows-sockets-support-for-bluetooth.md).



| Sezione                                                                                       | Content                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**INDIRIZZO \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)                                               | Contiene l'indirizzo di un Bluetooth dispositivo.                                                                                      |
| [**PARAMS \_ DI CALLBACK DI AUTENTICAZIONE \_ \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authentication_callback_params) | Contiene informazioni di configurazione specifiche sul dispositivo Bluetooth che risponde a una richiesta di autenticazione.                  |
| [**RISPOSTA \_ DI AUTENTICAZIONE \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authenticate_response)                  | Contiene le informazioni passate in risposta a un evento BTH \_ REMOTE \_ AUTHENTICATE \_ REQUEST.                                           |
| [**COPPIE \_ DI CODICI \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_cod_pairs)                                          | Fornisce la specifica e il recupero Bluetooth informazioni sulla classe del dispositivo (COD).                                         |
| [**INFORMAZIONI \_ SUL \_ DISPOSITIVO BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct)                                      | Fornisce informazioni su un Bluetooth dispositivo.                                                                                   |
| [**PARAMS \_ \_ DI RICERCA DISPOSITIVI \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_device_search_params)                   | Specifica i criteri di ricerca per Bluetooth ricerche nel dispositivo.                                                                         |
| [**BLUETOOTH \_ FIND \_ RADIO \_ PARAMS**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_find_radio_params)                         | Facilita l'enumerazione delle radio Bluetooth installate.                                                                       |
| [**INFORMAZIONI \_ SUL SERVIZIO LOCALE \_ \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct)                       | Contiene informazioni sul servizio locale per una Bluetooth radio.                                                                        |
| [**INFORMAZIONI \_ DI CONFRONTO NUMERICO \_ \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_numeric_comparison_info)             | Contiene il valore numerico utilizzato per l'autenticazione tramite confronto numerico.                                                       |
| [**INFORMAZIONI \_ SUI DATI OOB \_ \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_oob_data_info)                                 | Contiene i dati usati per l'autenticazione prima di stabilire un'associazione di dispositivi fuori banda.                                          |
| [**INFORMAZIONI \_ SULLA PASSKEY \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_passkey_info)                                    | Contiene la passkey usata per l'autenticazione tramite passkey.                                                                        |
| [**INFORMAZIONI \_ SUL PIN \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_pin_info)                                            | Contiene le informazioni usate per l'autenticazione tramite PIN.                                                                            |
| [**INFORMAZIONI \_ RADIO \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_radio_info)                                        | Contiene informazioni su una Bluetooth radio.                                                                                    |
| [**PARAMS \_ DEL DISPOSITIVO BLUETOOTH \_ \_ SELECT**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_select_device_params)                   | Facilita e gestisce la visibilità, l'autenticazione e la selezione Bluetooth dispositivi e servizi.                         |
| [**INFORMAZIONI SUL DISPOSITIVO BTH \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)                                                  | Archivia le informazioni su un Bluetooth dispositivo.                                                                                     |
| [**INFORMAZIONI \_ SULL'EVENTO BTH HCI \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)                                           | Usato in connessione con l'ottenimento di messaggi DEVICECHANGE WM \_ per Bluetooth.                                                       |
| [**INFORMAZIONI \_ SULL'EVENTO BTH L2CAP \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)                                       | Contiene dati sugli eventi associati a un canale L2CAP.                                                        |
| [**DISPOSITIVO DI QUERY BTH \_ \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)                                                | Usato quando si esegue una query per la presenza di un Bluetooth dispositivo.                                                                       |
| [**SERVIZIO QUERY BTH \_ \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)                                              | Usato per eseguire query su Bluetooth servizio.                                                                                               |
| [**BTH \_ RADIO \_ \_ NELL'INTERVALLO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)                                           | Archivia i dati sui dispositivi Bluetooth all'interno dell'intervallo di comunicazione.                                                     |
| [**SERVIZIO SET \_ \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)                                                  | Fornisce informazioni sul servizio per il servizio Bluetooth specificato.                                                                |
| [**DATI DEGLI ELEMENTI SDP \_ \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_element_data)                                                | Archivia i dati degli elementi SDP.                                                                                                         |
| [**DATI DI TIPO STRINGA SDP \_ \_ \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_string_type_data)                                       | Archivia informazioni sui tipi di stringa SDP.                                                                                       |
| [**SdpAttributeRange**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpattributerange)                                                | Usato in una Bluetooth query per vincolare il set di attributi da restituire nella query.                                             |
| [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid)                                                          | Facilita la ricerca di UUID.                                                                                                 |
| [**SdpQueryUuidUnion**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuidunion)                                                | Contiene l'UUID su cui eseguire una query SDP. Usato in combinazione con la [**struttura SdpQueryUuid.**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid) |
| [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)                                                         | Usato in combinazione con Bluetooth socket, come definito dalla famiglia di indirizzi \_ AF BTH.                                   |



 

 

 




