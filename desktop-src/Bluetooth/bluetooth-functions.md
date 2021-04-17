---
title: Funzioni Bluetooth
description: Le funzioni in questa sezione vengono usate per gestire i dispositivi e i servizi Bluetooth.
ms.assetid: 5cd4a050-51f3-40f4-b434-be639e109f0f
keywords:
- Bluetooth, informazioni di riferimento, funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad5343f0d609185f3bb472570b8454931fc6a18b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473243"
---
# <a name="bluetooth-functions"></a>Funzioni Bluetooth

Le funzioni in questa sezione vengono usate per gestire i dispositivi e i servizi Bluetooth.

Bluetooth è supportato anche tramite l'interfaccia di programmazione Windows Sockets. Per ulteriori informazioni sulla programmazione di Bluetooth utilizzando l'interfaccia Windows Sockets, vedere [supporto di Windows Sockets per Bluetooth](windows-sockets-support-for-bluetooth.md).



| Sezione                                                                                | Content                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)                     | Invia una richiesta di autenticazione a un dispositivo Bluetooth remoto.                                                                                                                                 |
| [**BluetoothAuthenticateDeviceEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedeviceex)                 | Invia una richiesta di autenticazione a un dispositivo Bluetooth remoto. Questa funzione consente inoltre di passare i dati fuori banda alla chiamata di funzione per l'autenticazione del dispositivo. |
| [**BluetoothAuthenticateMultipleDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatemultipledevices)   | Consente al chiamante di richiedere l'autenticazione di più dispositivi durante una singola istanza della connessione guidata Bluetooth.                                                            |
| [**BluetoothDisplayDeviceProperties**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothdisplaydeviceproperties)           | Richiama la finestra delle proprietà informazioni sul dispositivo del pannello di controllo.                                                                                                                                  |
| [**BluetoothEnableDiscovery**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenablediscovery)                           | Modifica lo stato di individuazione di una radio o radio Bluetooth locale.                                                                                                                             |
| [**BluetoothEnableIncomingConnections**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenableincomingconnections)       | Modifica se una radio Bluetooth locale accetta connessioni in ingresso.                                                                                                                        |
| [**BluetoothEnumerateInstalledServices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenumerateinstalledservices)     | Enumera i GUID (identificatori univoci globali) dei servizi abilitati in un dispositivo Bluetooth.                                                                                    |
| [**BluetoothFindDeviceClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfinddeviceclose)                           | Chiude un handle di enumerazione associato a una query del dispositivo.                                                                                                                          |
| [**BluetoothFindFirstDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstdevice)                           | Inizia l'enumerazione dei dispositivi Bluetooth locali.                                                                                                                                            |
| [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)                             | Inizia l'enumerazione delle radio Bluetooth locali.                                                                                                                                             |
| [**BluetoothFindNextDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextdevice)                             | Trova il dispositivo Bluetooth successivo.                                                                                                                                                              |
| [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)                               | Trova la radio Bluetooth successiva.                                                                                                                                                               |
| [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)                             | Chiude l'handle di enumerazione associato alla ricerca di radio Bluetooth.                                                                                                               |
| [**BluetoothGetDeviceInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetdeviceinfo)                               | Recupera le informazioni su un dispositivo Bluetooth remoto. Il dispositivo Bluetooth deve essere stato identificato in precedenza tramite una chiamata di funzione del dispositivo con esito positivo.                           |
| [**BluetoothGetRadioInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetradioinfo)                                 | Ottiene informazioni su una radio Bluetooth.                                                                                                                                                  |
| [**BluetoothIsConnectable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisconnectable)                               | Determina se una radio o radio Bluetooth è connessa.                                                                                                                                |
| [**BluetoothIsDiscoverable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisdiscoverable)                             | Determina se una radio o radio Bluetooth è individuabile.                                                                                                                               |
| [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)       | Registra una funzione di callback che viene chiamata quando un particolare dispositivo Bluetooth richiede l'autenticazione.                                                                                      |
| [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)   | Registra un'applicazione per una richiesta PIN, un confronto numerico e una funzione di callback.                                                                                                         |
| [**BluetoothRemoveDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothremovedevice)                                 | Rimuove l'autenticazione tra un dispositivo Bluetooth e il computer, eliminando eventuali informazioni memorizzate nella cache relative al dispositivo.                                                                          |
| [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)                       | Enumera il flusso di record SDP e chiama la funzione di callback per ogni attributo nel record.                                                                                    |
| [**BluetoothSdpGetAttributeValue**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetattributevalue)                 | Recupera il valore dell'attributo per un identificatore di attributo.                                                                                                                                    |
| [**BluetoothSdpGetContainerElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata)     | Scorre un flusso del contenitore e restituisce ogni elemento contenuto all'interno dell'elemento contenitore.                                                                                     |
| [**BluetoothSdpGetElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetelementdata)                       | Recupera e analizza un singolo elemento da un flusso SDP.                                                                                                                                     |
| [**BluetoothSdpGetString**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetstring)                                 | Converte una stringa non elaborata incorporata nel record SDP in una stringa Unicode.                                                                                                               |
| [**BluetoothSelectDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                               | Abilita la selezione del dispositivo Bluetooth.                                                                                                                                                           |
| [**BluetoothSelectDevicesFree**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevicesfree)                       | Libera le risorse associate a una chiamata precedente alla funzione [**BluetoothSelectDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices) .                                                                     |
| [**BluetoothSendAuthenticationResponse**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponse)     | Chiamato quando viene ricevuta un'autenticazione Request to Send la risposta di passkey.                                                                                                               |
| [**BluetoothSendAuthenticationResponseEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponseex) | Chiamato quando viene ricevuta un'autenticazione Request to Send la passkey o la risposta di confronto numerica.                                                                                         |
| [**BluetoothSetLocalServiceInfo**](/previous-versions/windows/desktop/legacy/bb870603(v=vs.85))                   | Imposta le informazioni sul servizio locale per una specifica radio Bluetooth.                                                                                                                                |
| [**BluetoothSetServiceState**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsetservicestate)                           | Abilita o Disabilita i servizi per un dispositivo Bluetooth.                                                                                                                                          |
| [**BluetoothUnregisterAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothunregisterauthentication)         | Rimuove la registrazione per una routine di callback precedentemente registrata con una chiamata alla funzione [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .      |
| [**BluetoothUpdateDeviceRecord**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothupdatedevicerecord)                     | Aggiorna la cache del computer locale su un dispositivo Bluetooth.                                                                                                                                    |



 

 

 