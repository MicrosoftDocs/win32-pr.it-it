---
title: Funzioni api del dispositivo software
description: Questa sezione descrive le funzioni api del dispositivo software chiamate da un'app client e una funzione di callback implementata da un'app client.
ms.assetid: 68F142A9-08AD-4F74-A0C3-3DCC8F7449B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f5d525eb9a4d4bc9af4807a2b3ad069b109b17874040e84cb3a9059d31bb85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937091"
---
# <a name="software-device-api-functions"></a>Funzioni api del dispositivo software

Questa sezione descrive le funzioni api del dispositivo software chiamate da un'app client e una funzione di callback implementata da un'app client.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                           | Descrizione                                                                                                                                                      |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SwDeviceClose**](/windows/win32/api/swdevice/nf-swdevice-swdeviceclose)<br/>                               | Chiude l'handle del dispositivo software. Quando l'handle viene chiuso, PnP avvierà il processo di rimozione del dispositivo.<br/>                                   |
| [**CALLBACK \_ DI CREAZIONE DEL \_ DISPOSITIVO \_ SW**](/windows/win32/api/swdevice/nc-swdevice-sw_device_create_callback)<br/>    | Fornisce un dispositivo con supporto nel Registro di sistema e consente al chiamante di effettuare quindi chiamate alle funzioni API del dispositivo software con l'handle *hSwDevice.*<br/> |
| [**SwDeviceCrea**](/windows/win32/api/swdevice/nf-swdevice-swdevicecreate)<br/>                             | Avvia l'enumerazione di un dispositivo software.<br/>                                                                                                       |
| [**SwDeviceGetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicegetlifetime)<br/>                   | Ottiene la durata di un dispositivo software. <br/>                                                                                                              |
| [**SwDeviceInterfacePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacepropertyset)<br/> | Imposta le proprietà in un'interfaccia del dispositivo software. <br/>                                                                                                      |
| [**SwDeviceInterfaceRegister**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfaceregister)<br/>       | Registra un'interfaccia del dispositivo per un dispositivo software e facoltativamente imposta le proprietà su tale interfaccia. <br/>                                                 |
| [**SwDeviceInterfaceSetState**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacesetstate)<br/>       | Abilita o disabilita un'interfaccia del dispositivo per un dispositivo software. <br/>                                                                                        |
| [**SwDevicePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdevicepropertyset)<br/>                   | Imposta le proprietà in un dispositivo software. <br/>                                                                                                                |
| [**SwDeviceSetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicesetlifetime)<br/>                   | Gestisce la durata di un dispositivo software. <br/>                                                                                                           |
| [**SwMemFree**](/windows/win32/api/swdevice/nf-swdevice-swmemfree)<br/>                                       | Libera memoria allocata da altre funzioni api del dispositivo software.<br/>                                                                                      |



 

 

 

[Inviare commenti su questo argomento a Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20Functions%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Inviare commenti su questo argomento a Microsoft")