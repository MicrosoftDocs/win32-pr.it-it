---
title: Classe MsRdpClient5NotSafeForScripting
description: Controllo client MICROSOFT RDP - versione 6.
ms.assetid: 0DC46910-D77E-47CF-92C3-4019D79C783C
ms.tgt_platform: multiple
keywords:
- Classe MsRdpClient5NotSafeForScripting Servizi Desktop remoto
- Classe MsRdpClient5NotSafeForScripting Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- MsRdpClient5NotSafeForScripting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23c525a779429eef31204c7f54fa9b4a15aa67f2a84c3f65f5a3cc0f8816d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605341"
---
# <a name="msrdpclient5notsafeforscripting-class"></a>Classe MsRdpClient5NotSafeForScripting

Controllo client MICROSOFT RDP - versione 6

Questa classe implementa le interfacce seguenti.

-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**Idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)

**MsRdpClient5NotSafeForScripting** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MsRdpClient5NotSafeForScripting** include questi metodi.



| Metodo                                                                                      | Descrizione                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Connettere**](imstscax-connect.md)                                                         | Avvia una connessione utilizzando le proprietà attualmente impostate sul controllo .<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Crea un oggetto canale virtuale lato client per ogni nome di canale virtuale specificato.<br/>                                                                                                                                                                                              |
| [**Disconnetti**](imstscax-disconnect.md)                                                   | Disconnette la connessione attiva.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Recupera i codici di errore e i messaggi di errore.<br/>                                                                                                                                                                                                                                      |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Recupera le opzioni impostate per un canale virtuale.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Notifica al modulo di reindirizzamento del dispositivo il controllo Desktop remoto ActiveX che si è verificata una modifica del dispositivo nel sistema. Questo metodo passa [**le \_ notifiche DEVICECHANGE WM**](/windows/desktop/DevIO/wm-devicechange) al controllo.<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | Chiamato dopo che un ActiveX visualizza una finestra di dialogo di autenticazione, ad esempio la finestra di dialogo di errore del certificato.<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | Chiamato prima che un ActiveX di autenticazione visualizzi una finestra di dialogo di autenticazione, ad esempio la finestra di dialogo di errore del certificato.<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Chiamato quando il controllo client si è riconnesso automaticamente a una sessione remota.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Chiamato quando un client sta per riconnettersi automaticamente a una sessione con un server Host sessione Desktop remoto.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Chiamato quando un client sta per riconnettersi automaticamente a una sessione con un server Host sessione Desktop remoto.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Chiamato quando il client riceve i dati in un canale virtuale gestibile da script.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Chiamato quando il client chiama il [**metodo IMsRdpClient::RequestClose.**](imsrdpclient-requestclose.md)<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | Chiamato quando il controllo client sta per stabilire una connessione con un server Host sessione Desktop remoto.<br/>                                                                                                                                                                       |
| [**OnConnecting**](imstscaxevents-onconnecting.md)                                         | Chiamato quando il controllo client inizia a connettersi a un server in risposta a una chiamata a [**IMsTscAx::Connessione**](imstscax-connect.md).<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Chiamato quando l'utente è stato trascinato verso il basso sulla barra delle connessioni.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Chiamato quando viene premuto il pulsante dispositivi nella barra delle connessioni.<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | Chiamato quando il controllo client è stato disconnesso dal server Host sessione Desktop remoto.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Chiamato quando il client entra in modalità schermo intero. Ad esempio, questo evento viene chiamato quando l'utente preme la combinazione di tasti di scelta rapida per la modalità schermo intero (CTRL+ALT+INTERR). [](terminal-services-shortcut-keys.md)<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Chiamato quando il controllo client rileva un errore irreversibile.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Chiamato quando viene premuta la combinazione di tasti rilascia lo stato attivo. Ad esempio, questo evento viene chiamato quando l'utente preme CTRL+ALT+FRECCIA SINISTRA o la combinazione di tasti CTRL+ALT+FRECCIA DESTRA.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Chiamato quando l'utente non ha avuto input da mouse o tastiera durante il periodo di tempo impostato dal metodo [**IMsRdpClientAdvancedSettings::p ut \_ MinutesToIdleTimeout.**](imsrdpclientadvancedsettings-minutestoidletimeout.md)<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Chiamato quando il client esce dalla modalità schermo intero. Ad esempio, questo evento viene chiamato quando l'utente preme la combinazione di tasti di scelta rapida per la modalità schermo intero (CTRL+ALT+INTERR). [](terminal-services-shortcut-keys.md)<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | Chiamato quando il controllo client ha eseguito correttamente l'accesso a un server Host sessione Desktop remoto, dopo la visualizzazione della finestra Windows di accesso remoto.<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | Chiamato quando si verifica un errore di accesso o un altro evento di accesso.<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Chiamato quando viene modificata la modalità di input del mouse.<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | Chiamato quando lo stato della rete viene modificato.<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | Chiamato durante la sequenza di connessione quando il client recupera la chiave pubblica dal server. Questo evento viene chiamato solo se la **proprietà NotifyTSPublicKey** è **VARIANT \_ TRUE.**<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | Chiamato per indicare che le dimensioni del controllo client sul desktop remoto sono state modificate in risposta a un'operazione di controllo client.<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | Chiamato quando viene visualizzato un programma RemoteApp.<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | Chiamato quando un programma RemoteApp restituisce un risultato al controllo client.<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | Chiamato quando viene visualizzata una finestra di RemoteApp.<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | Viene chiamato quando l'utente preme il **pulsante Riduci** a icona sulla barra delle connessioni in modalità schermo intero. La generazione di questo evento è una richiesta che l'applicazione contenitore riduce a icona.<br/>                                                                                              |
| [**OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md)                       | Chiamato quando il client richiede di passare alla modalità schermo intero e il metodo [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) viene chiamato per impostare la proprietà **ContainerHandledFullScreen** su un valore diverso da zero.<br/> |
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Chiamato quando il client richiede di uscire dalla modalità schermo intero e la proprietà [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) è stata impostata su un valore diverso da zero.<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | Chiamato quando il client riceve un messaggio di sistema.<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Chiamato quando il nome utente è stato acquisito dal controllo .<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Chiamato quando il controllo client rileva una condizione di errore non irreversibile.<br/>                                                                                                                                                                                                    |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Richiede un arresto normale del controllo client.<br/>                                                                                                                                                                                                                                |
| [**Resetpassword**](imstscnonscriptable-resetpassword.md)                                  | Reimposta tutti gli stati della password nel controllo .<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Invia una serie di sequenze di tasti al controllo. Le sequenze di tasti sono in formato codice di analisi, ovvero i dati della tastiera dei tasti fisici effettivi.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Invia dati al server Host sessione Desktop remoto tramite un canale virtuale creato in precedenza usando il metodo [**IMsTscAx::CreateVirtualChannels.**](imstscax-createvirtualchannels.md)<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Imposta le opzioni del canale virtuale per il controllo client.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Proprietà

La **classe MsRdpClient5NotSafeForScripting** ha queste proprietà.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Proprietà</th>
<th style="text-align: left;">Tipo di accesso</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-advancedsettings.md"><strong>Impostazioni avanzate</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Puntatore <a href="imstscadvancedsettings-interface.md"><strong>a interfaccia IMsTscAdvancedSettings.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-advancedsettings2.md"><strong>Impostazioni avanzate2</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Puntatore <a href="imsrdpclientadvancedsettings-interface.md"><strong>all'interfaccia IMsRdpClientAdvancedSettings,</strong></a> usata per impostare le impostazioni avanzate per il controllo client.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient2-advancedsettings3.md"><strong>Impostazioni avanzate3</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Puntatore <a href="imsrdpclientadvancedsettings2.md"><strong>all'interfaccia IMsRdpClientAdvancedSettings2,</strong></a> usata per impostare le impostazioni avanzate per il controllo client.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient3-advancedsettings4.md"><strong>Impostazioni avanzate4</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Puntatore <a href="imsrdpclientadvancedsettings3.md"><strong>all'interfaccia IMsRdpClientAdvancedSettings3,</strong></a> usata per impostare le impostazioni avanzate per il controllo client.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient4-advancedsettings5.md"><strong>Impostazioni avanzate5</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Puntatore <a href="imsrdpclientadvancedsettings4.md"><strong>a interfaccia IMsRdpClientAdvancedSettings4.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-advancedsettings6.md"><strong>Impostazioni avanzate6</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Interfaccia di <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5.</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Questa proprietà non è supportata.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Questa proprietà non è supportata.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Livello massimo di crittografia del controllo corrente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a><br/></td>
<td style="text-align: left;">Sola scrittura<br/></td>
<td style="text-align: left;">La Desktop remoto ActiveX password di controllo, in formato testo non crittografato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient-colordepth.md"><strong>ColorDepth</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Profondità del colore del controllo corrente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-connected.md"><strong>Connesso</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Stato di connessione del controllo corrente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-connectingtext.md"><strong>Connessione di testo</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Testo visualizzato al centro nel controllo mentre il controllo è connesso.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Stringa di testo da visualizzare per la barra di connessione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Altezza del controllo corrente, in pixel, sul desktop remoto iniziale.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Larghezza del controllo corrente, in pixel, sul desktop remoto iniziale.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Raccolta di dispositivi PnP disponibili per il reindirizzamento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Testo visualizzato centrato nel controllo prima che venga terminata una connessione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-domain.md"><strong>Dominio</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Dominio a cui l'utente corrente accede.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Raccolta di unità disco disponibili per il reindirizzamento.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se CredSSP è abilitato per questa connessione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Informazioni estese sul motivo della disconnessione del controllo client.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-fullscreen.md"><strong>FullScreen</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Indica se il controllo è in modalità schermo intero.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br/></td>
<td style="text-align: left;">Sola scrittura<br/></td>
<td style="text-align: left;">Titolo della finestra visualizzato quando il controllo è in modalità schermo intero.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Indica se il controllo ha visualizzato una barra di scorrimento orizzontale.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Impostazioni client per l'utilità di avvio del portale Web.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se l'impostazione NegotiateSecurityLayer è supportata per questa connessione.<br/>
<blockquote>
[!Note]<br />
Quando <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> è abilitato e presente nel client o quando Secure Sockets Layer (SSL) è abilitato con l'autenticazione utente, NegotiateSecurityLayer viene ignorato.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Questa proprietà non è supportata.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Questa proprietà non è supportata.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se deve essere visualizzata la finestra di dialogo di richiesta delle credenziali.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se i dispositivi PnP collegati dinamicamente enumerati durante una sessione sono disponibili per il reindirizzamento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se le unità PnP collegate dinamicamente enumerate durante una sessione sono disponibili per il reindirizzamento.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Impostazione di RemoteApp client.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-securedsettings.md"><strong>Impostazioni protette</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Puntatore <a href="imstscsecuredsettings-interface.md"><strong>a interfaccia IMsTscSecuredSettings.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-securedsettings2.md"><strong>Impostazioni protette2</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Puntatore <a href="imsrdpclientsecuredsettings-interface.md"><strong>all'interfaccia IMsRdpClientSecuredSettings,</strong></a> usata per impostare le impostazioni protette per il controllo client.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Indica se <a href="imstscsecuredsettings-interface.md"><strong>l'interfaccia IMsTscSecuredSettings</strong></a> è disponibile.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-server.md"><strong>Server</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Nome del server a cui è connesso il controllo corrente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se la finestra di dialogo di avviso di sicurezza di reindirizzamento deve essere visualizzata prima di avviare una sessione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Indica se il controllo stabilirà la connessione al server Host sessione Desktop remoto immediatamente all'avvio.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Impostazione di Gateway Desktop remoto del client.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Handle di finestra che deve essere la finestra padre per il controllo . In questo modo tutte le finestre visualizzate dal controllo saranno correttamente modali rispetto alle finestre visualizzate dall'applicazione padre.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-username.md"><strong>Nome utente</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Credenziali di accesso del nome utente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-version.md"><strong>Versione</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Numero di versione del controllo corrente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br/></td>
<td style="text-align: left;">Sola lettura<br/></td>
<td style="text-align: left;">Indica se il controllo visualizza una barra di scorrimento verticale.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se la finestra di dialogo di avviso di sicurezza deve includere un avviso sul reindirizzamento degli Appunti prima di avviare una sessione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br/></td>
<td style="text-align: left;">Lettura/Scrittura<br/></td>
<td style="text-align: left;">Specifica se l'avviso di sicurezza deve includere un avviso sull'invio di credenziali al server remoto prima di avviare una sessione.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                             |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                       |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>               |
| CLSID<br/>                    | CLSID \_ MsRdpClient5NotSafeForScripting è definito come 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Desktop remoto ActiveX classi di controllo](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

