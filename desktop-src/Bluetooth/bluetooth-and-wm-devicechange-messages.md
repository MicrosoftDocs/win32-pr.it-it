---
title: Bluetooth e WM_DEVICECHANGE messaggi
description: Bluetooth include messaggi DEVICECHANGE WM specifici che consentono agli sviluppatori di ottenere messaggi quando Bluetooth \_ dispositivi subiscono modifiche dello stato.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b22c08c4243ce33f7d3146e96a3fcdd5c937b4781fd783918c148939ca0e22e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588411"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a>Bluetooth e WM \_ DEVICECHANGE

Bluetooth include messaggi [**\_ DEVICECHANGE WM**](/windows/desktop/DevIO/wm-devicechange) specifici che consentono agli sviluppatori di ottenere messaggi quando Bluetooth dispositivi subiscono modifiche dello stato. Questo argomento descrive come ricevere messaggi **WM \_ DEVICECHANGE** Bluetooth specifici ed elenca Bluetooth specifici.

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a>Ricezione Bluetooth messaggi DEVICECHANGE WM \_ specifici

Per ricevere [**messaggi \_ DEVICECHANGE WM,**](/windows/desktop/DevIO/wm-devicechange) è prima necessario aprire un handle per la radio locale. A tale scopo, adottare uno dei metodi seguenti:

-   Usare la funzione [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) con i parametri seguenti: (GUID \_ BTHPORT \_ DEVICE \_ INTERFACE, ..., DIGCF PRESENT DIGCF DEVICEINTERFACE), quindi usare le funzioni \_ \| \_ [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)e [SetupDiDestroyDeviceInfoList.](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
-   Usare le [**funzioni BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)e [**BluetoothFindRadioClose.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)

Quando viene aperto Bluetooth handle radio, chiamare la funzione [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) e registrarsi per le notifiche sull'handle usando **DBT \_ DEVTYP \_ HANDLE** come tipo di dispositivo. Dopo la registrazione, vengono inviati i GUID seguenti e il membro dati [**\_ DEV BROADCAST \_ HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch \_** è il buffer associato.

## <a name="bluetooth-specific-messages"></a>Bluetooth specifici dei messaggi

Nella tabella seguente sono elencati Bluetooth [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) specifici.

| GUID                                   | BUFFER                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID \_ BLUETOOTH \_ HCI \_ EVENT            | [**INFORMAZIONI \_ SULL'EVENTO BTH HCI \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | Questo messaggio viene inviato quando un dispositivo Bluetooth remoto si connette o si disconnette a livello di ACL.                                                                                                                                                                                                                                                                    |
| GUID \_ BLUETOOTH \_ L2CAP \_ EVENT          | [**INFORMAZIONI \_ SULL'EVENTO BTH \_ \_ L2CAP**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | Questo messaggio viene inviato quando viene stabilito o terminato un canale L2CAP tra la radio locale e Bluetooth remoto. Per i canali L2CAP che sono multiplexer, ad esempio RFCOMM, questo messaggio viene inviato solo quando viene stabilito il canale sottostante, non quando viene stabilito o terminato ogni canale con multiplexed, ad esempio un canale RFCOMM. |
| RICHIESTA PIN \_ BLUETOOTH \_ \_ GUID          | Non applicabile.                                         | Questo messaggio deve essere ignorato dall'applicazione. Se l'applicazione deve ricevere richieste PIN, è necessario usare [**la funzione BluetoothRegisterForAuthentication.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)                                                                                                                                                   |
| GUID \_ BLUETOOTH \_ RADIO \_ IN \_ RANGE      | [**BTH \_ RADIO \_ \_ NELL'INTERVALLO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | Questo messaggio viene inviato quando viene modificato uno degli attributi seguenti di un dispositivo Bluetooth remoto: il dispositivo è stato individuato, la classe del dispositivo, il nome, lo stato connesso o lo stato di memoria del dispositivo. Questo messaggio viene inviato anche quando questi attributi vengono impostati o cancellati.                                                                                  |
| GUID \_ BLUETOOTH \_ RADIO \_ OUT \_ OF \_ RANGE | [**INDIRIZZO \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | Questo messaggio viene inviato quando un dispositivo individuato in precedenza non viene trovato dopo il completamento dell'ultima richiesta. Questo messaggio non verrà inviato per i dispositivi memorizzati. La **struttura \_ BTH ADDRESS** è l'indirizzo del dispositivo che non è stato trovato.                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[**INDIRIZZO \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[**INFORMAZIONI \_ SULL'EVENTO BTH HCI \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[**INFORMAZIONI \_ SULL'EVENTO BTH \_ \_ L2CAP**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[**BTH \_ RADIO \_ \_ NELL'INTERVALLO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[**HANDLE \_ DI TRASMISSIONE \_ DI SVILUPPO**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 