---
title: Bluetooth Funzioni
description: Le funzioni di questa sezione vengono usate per la gestione Bluetooth dispositivi e servizi.
ms.assetid: 5cd4a050-51f3-40f4-b434-be639e109f0f
keywords:
- Bluetooth, riferimento, funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e8d945355b0bc25df4d91a96c30a4d20491eb3b0e86c3542e30c0f2b470833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701411"
---
# <a name="bluetooth-functions"></a>Bluetooth Funzioni

Le funzioni di questa sezione vengono usate per la gestione Bluetooth dispositivi e servizi.

Bluetooth è supportato anche tramite l'interfaccia di programmazione Windows Sockets. Per altre informazioni sulla programmazione Bluetooth tramite l'interfaccia Windows Sockets, vedere Supporto [di Windows Sockets per Bluetooth](windows-sockets-support-for-bluetooth.md).



| Sezione                                                                                | Content                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)                     | Invia una richiesta di autenticazione a un dispositivo Bluetooth remoto.                                                                                                                                 |
| [**BluetoothAuthenticateDeviceEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedeviceex)                 | Invia una richiesta di autenticazione a un dispositivo Bluetooth remoto. Questa funzione consente inoltre di passare dati fuori banda alla chiamata di funzione per il dispositivo da autenticare. |
| [**BluetoothAuthenticateMultipleDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatemultipledevices)   | Consente al chiamante di richiedere l'autenticazione di più dispositivi durante una singola istanza della Bluetooth connessione guidata.                                                            |
| [**BluetoothDisplayDeviceProperties**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothdisplaydeviceproperties)           | Richiama la finestra delle Pannello di controllo delle informazioni sul dispositivo.                                                                                                                                  |
| [**BluetoothEnableDiscovery**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenablediscovery)                           | Modifica lo stato di individuazione di un Bluetooth radio o radio locali.                                                                                                                             |
| [**BluetoothEnableIncomingConnections**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenableincomingconnections)       | Modifica se una radio locale Bluetooth accetta connessioni in ingresso.                                                                                                                        |
| [**BluetoothEnumerateInstalledServices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenumerateinstalledservices)     | Enumera i GUID (identificatori univoci globali) dei servizi abilitati in un Bluetooth dispositivo.                                                                                    |
| [**BluetoothFindDeviceClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfinddeviceclose)                           | Chiude un handle di enumerazione associato a una query sul dispositivo.                                                                                                                          |
| [**BluetoothFindFirstDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstdevice)                           | Avvia l'enumerazione dei dispositivi Bluetooth locale.                                                                                                                                            |
| [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)                             | Avvia l'enumerazione delle radio Bluetooth locali.                                                                                                                                             |
| [**BluetoothFindNextDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextdevice)                             | Trova il dispositivo Bluetooth successivo.                                                                                                                                                              |
| [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)                               | Trova la radio Bluetooth successiva.                                                                                                                                                               |
| [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)                             | Chiude l'handle di enumerazione associato alla ricerca Bluetooth radio.                                                                                                               |
| [**BluetoothGetDeviceInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetdeviceinfo)                               | Recupera informazioni su un dispositivo Bluetooth remoto. Il Bluetooth dispositivo deve essere stato identificato in precedenza tramite una chiamata di funzione di richiesta del dispositivo riuscita.                           |
| [**BluetoothGetRadioInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetradioinfo)                                 | Ottiene informazioni su una Bluetooth radio.                                                                                                                                                  |
| [**BluetoothIsConnectable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisconnectable)                               | Determina se una Bluetooth radio o radio è collegabile.                                                                                                                                |
| [**BluetoothIsDiscoverable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisdiscoverable)                             | Determina se una Bluetooth radio o radio è individuabile.                                                                                                                               |
| [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)       | Registra una funzione di callback che viene chiamata quando un determinato Bluetooth richiede l'autenticazione.                                                                                      |
| [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)   | Registra un'applicazione per una richiesta di aggiunta, un confronto numerico e una funzione di callback.                                                                                                         |
| [**BluetoothRemoveDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothremovedevice)                                 | Rimuove l'autenticazione tra Bluetooth dispositivo e il computer, cancellando tutte le informazioni memorizzate nella cache del dispositivo.                                                                          |
| [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)                       | Enumera tramite il flusso di record SDP e chiama la funzione di callback per ogni attributo nel record.                                                                                    |
| [**BluetoothSdpGetAttributeValue**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetattributevalue)                 | Recupera il valore dell'attributo per un identificatore di attributo.                                                                                                                                    |
| [**BluetoothSdpGetContainerElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata)     | Scorre un flusso del contenitore e restituisce ogni elemento contenuto nell'elemento contenitore.                                                                                     |
| [**BluetoothSdpGetElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetelementdata)                       | Recupera e analizza un singolo elemento da un flusso SDP.                                                                                                                                     |
| [**BluetoothSdpGetString**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetstring)                                 | Converte una stringa non elaborata incorporata nel record SDP in una stringa Unicode.                                                                                                               |
| [**BluetoothSelectDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                               | Abilita Bluetooth del dispositivo.                                                                                                                                                           |
| [**BluetoothSelectDevicesFree**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevicesfree)                       | Libera le risorse associate a una chiamata precedente alla [**funzione BluetoothSelectDevices.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                                                                     |
| [**BluetoothSendAuthenticationResponse**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponse)     | Chiamato quando viene ricevuta una richiesta di autenticazione per inviare la risposta della passkey.                                                                                                               |
| [**BluetoothSendAuthenticationResponseEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponseex) | Chiamato quando viene ricevuta una richiesta di autenticazione per inviare la passkey o la risposta di confronto numerico.                                                                                         |
| [**BluetoothSetLocalServiceInfo**](/previous-versions/windows/desktop/legacy/bb870603(v=vs.85))                   | Imposta le informazioni sul servizio locale per una Bluetooth radio specifica.                                                                                                                                |
| [**BluetoothSetServiceState**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsetservicestate)                           | Abilita o disabilita i servizi per un Bluetooth dispositivo.                                                                                                                                          |
| [**BluetoothUnregisterAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothunregisterauthentication)         | Rimuove la registrazione per una routine di callback registrata in precedenza con una chiamata alla [**funzione BluetoothRegisterForAuthentication.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)      |
| [**BluetoothUpdateDeviceRecord**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothupdatedevicerecord)                     | Aggiorna la cache del computer locale su un Bluetooth locale.                                                                                                                                    |



 

 

 