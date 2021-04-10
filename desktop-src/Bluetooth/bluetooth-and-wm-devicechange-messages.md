---
title: Messaggi Bluetooth e WM_DEVICECHANGE
description: Bluetooth include \_ messaggi DEVICECHANGE WM specifici che consentono agli sviluppatori di ottenere messaggi quando i dispositivi Bluetooth subiscono modifiche di stato.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963170"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a>Messaggi Bluetooth e WM \_ DEVICECHANGE

Bluetooth include messaggi [**\_ DEVICECHANGE WM**](/windows/desktop/DevIO/wm-devicechange) specifici che consentono agli sviluppatori di ottenere messaggi quando i dispositivi Bluetooth subiscono modifiche di stato. Questo argomento descrive come ricevere messaggi **WM \_ DEVICECHANGE** specifici di Bluetooth ed elenca i messaggi specifici di Bluetooth.

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a>Ricezione di messaggi WM DEVICECHANGE specifici per Bluetooth \_

Per ricevere i messaggi [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) , è necessario innanzitutto aprire un handle per la radio locale. A tale scopo, adottare uno dei metodi seguenti:

-   Usare la funzione [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) con i parametri seguenti: ( \_ interfaccia del dispositivo GUID bthport \_ \_ ,..., DIGCF \_ presente \| DIGCF \_ DEVICEINTERFACE), quindi usare le funzioni [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)e [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) .
-   Usare le funzioni [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)e [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) .

Quando viene aperto l'handle di radio Bluetooth, chiamare la funzione [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) e registrarsi per le notifiche sull'handle usando l' **\_ \_ handle DBT DEVTYP** come DeviceType. Una volta registrati, vengono inviati i GUID seguenti e il membro **\_ dati** [**dev \_ broadcast \_ handle**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle):: dbch è il buffer associato.

## <a name="bluetooth-specific-messages"></a>Messaggi specifici di Bluetooth

La tabella seguente elenca i messaggi [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) specifici per Bluetooth.

| GUID                                   | BUFFER                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ evento HCI Bluetooth \_ GUID            | [**\_ \_ informazioni evento BTH \_ HCI**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | Questo messaggio viene inviato quando un dispositivo Bluetooth remoto si connette o si disconnette a livello di ACL.                                                                                                                                                                                                                                                                    |
| \_ \_ Evento L2CAP Bluetooth \_ GUID          | [**\_Informazioni sull' \_ evento \_ L2CAP di BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | Questo messaggio viene inviato quando viene stabilito o terminato un canale L2CAP tra la radio locale e un dispositivo Bluetooth remoto. Per i canali L2CAP che sono multiplexer, ad esempio RFCOMM, questo messaggio viene inviato solo quando viene stabilito il canale sottostante, non quando viene stabilito o terminato ogni canale multiplex, ad esempio un canale RFCOMM. |
| \_ \_ richiesta PIN Bluetooth \_ GUID          | Non applicabile.                                         | Questo messaggio deve essere ignorato dall'applicazione. Se l'applicazione deve ricevere richieste PIN, è necessario usare la funzione [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .                                                                                                                                                   |
| \_radio Bluetooth \_ GUID \_ nell' \_ intervallo      | [**BTH \_ Radio \_ nell' \_ intervallo**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | Questo messaggio viene inviato quando uno degli attributi seguenti di un dispositivo Bluetooth remoto è stato modificato: il dispositivo è stato individuato, la classe del dispositivo, il nome, lo stato connesso o lo stato del dispositivo memorizzato. Questo messaggio viene inviato anche quando questi attributi sono impostati o cancellati.                                                                                  |
| \_radio Bluetooth GUID non \_ compresa nell' \_ \_ \_ intervallo | [**\_Indirizzo Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | Questo messaggio viene inviato quando un dispositivo individuato in precedenza non è stato trovato dopo il completamento dell'ultima richiesta. Questo messaggio non verrà inviato per i dispositivi memorizzati. La struttura dell' **\_ Indirizzo BTH** è l'indirizzo del dispositivo che non è stato trovato.                                                                                                      |



 

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

[**\_Indirizzo Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[**\_ \_ informazioni evento BTH \_ HCI**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[**\_Informazioni sull' \_ evento \_ L2CAP di BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[**BTH \_ Radio \_ nell' \_ intervallo**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[**\_handle broadcast \_ dev**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[**\_DEVICECHANGE WM**](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 