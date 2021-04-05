---
title: Callback Bluetooth
description: Le funzioni di callback Bluetooth in questa sezione vengono usate in combinazione con funzioni che consentono di gestire i dispositivi e i servizi Bluetooth.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708113"
---
# <a name="bluetooth-callbacks"></a>Callback Bluetooth

Le funzioni di callback Bluetooth in questa sezione vengono usate in combinazione con funzioni che consentono di gestire i dispositivi e i servizi Bluetooth.

Bluetooth è supportato anche tramite l'interfaccia di programmazione Windows Sockets. Per ulteriori informazioni sulla programmazione di Bluetooth utilizzando l'interfaccia Windows Sockets, vedere [supporto di Windows Sockets per Bluetooth](windows-sockets-support-for-bluetooth.md).



| Sezione                                                                                      | Content                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_callback di autenticazione PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | Utilizzato in combinazione con la funzione [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .                                                  |
| [**\_esempio di \_ callback di autenticazione PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | Utilizzato in combinazione con la funzione [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) .                                              |
| [**\_callback degli \_ attributi di enumerazione Bluetooth \_ PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | Viene chiamato una volta per ogni attributo trovato nel parametro *pSDPStream* passato alla chiamata di funzione [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) . |
| [**\_callback del dispositivo PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | Utilizzato in associazione alla selezione dei dispositivi Bluetooth.                                                                                                                    |



 

 

 




