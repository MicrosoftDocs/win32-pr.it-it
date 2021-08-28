---
title: Bluetooth Callback
description: Le Bluetooth di callback in questa sezione vengono usate in combinazione con funzioni che rendono possibile la gestione Bluetooth dispositivi e servizi.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad822a0c7af4b0bbc5d649919bda638776014dfe7e8195ed1f45bb99032c6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588361"
---
# <a name="bluetooth-callbacks"></a>Bluetooth Callback

Le Bluetooth di callback in questa sezione vengono usate in combinazione con funzioni che rendono possibile la gestione Bluetooth dispositivi e servizi.

Bluetooth è supportato anche tramite l'interfaccia di programmazione Windows Sockets. Per altre informazioni sulla programmazione Bluetooth tramite l'interfaccia Windows Sockets, vedere Supporto [di Windows Sockets per Bluetooth](windows-sockets-support-for-bluetooth.md).



| Sezione                                                                                      | Content                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CALLBACK DI AUTENTICAZIONE PFN \_ \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | Usato in combinazione con la [**funzione BluetoothRegisterForAuthentication.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)                                                  |
| [**CALLBACK DI AUTENTICAZIONE PFN \_ \_ \_ EX**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | Usato in combinazione con la [**funzione BluetoothRegisterForAuthenticationEx.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)                                              |
| [**CALLBACK DEGLI ATTRIBUTI \_ DI ENUMERAZIONE BLUETOOTH PFN \_ \_ \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | Chiamato una volta per ogni attributo trovato nel *parametro pSDPStream* passato alla chiamata di funzione [**BluetoothSdpEnumAttributes.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) |
| [**CALLBACK DEL DISPOSITIVO PFN \_ \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | Usato in associazione con la selezione Bluetooth dispositivi.                                                                                                                    |



 

 

 




