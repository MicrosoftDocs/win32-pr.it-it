---
title: Classe MsRdpClient6
description: Controllo client MICROSOFT RDP (ridistribuibile) - versione 7.
ms.assetid: 1E8F5EBE-AF25-481D-8F41-13AAAF9B4A34
ms.tgt_platform: multiple
keywords:
- Classe MsRdpClient6 Servizi Desktop remoto
- Classe MsRdpClient6 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- MsRdpClient6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db831abf9e421601230b8f459799f7ac574417ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475327"
---
# <a name="msrdpclient6-class"></a>Classe MsRdpClient6

Controllo client MICROSOFT RDP (ridistribuibile) - versione 7

Questa classe implementa le interfacce seguenti.

-   [**IMsRdpClient6**](imsrdpclient6.md)
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
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)

**MsRdpClient6** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MsRdpClient6** include questi metodi.



| Metodo                                                                                      | Descrizione                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Connessione**](imstscax-connect.md)                                                         | Avvia una connessione usando le proprietà attualmente impostate nel controllo .<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Crea un oggetto canale virtuale sul lato client per ogni nome di canale virtuale specificato.<br/>                                                                                                                                                                                              |
| [**Disconnetti**](imstscax-disconnect.md)                                                   | Disconnette la connessione attiva.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Recupera i codici di errore e i messaggi di errore.<br/>                                                                                                                                                                                                                                      |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Recupera le opzioni impostate per un canale virtuale.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Notifica al modulo di reindirizzamento del dispositivo Desktop remoto ActiveX controllo che si è verificata una modifica del dispositivo nel sistema. Questo metodo passa [**le \_ notifiche DEVICECHANGE WM**](/windows/desktop/DevIO/wm-devicechange) al controllo.<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | Chiamato dopo che un ActiveX controllo visualizza una finestra di dialogo di autenticazione, ad esempio la finestra di dialogo di errore del certificato.<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | Chiamato prima che un controllo ActiveX visualizza una finestra di dialogo di autenticazione, ad esempio la finestra di dialogo di errore del certificato.<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Chiamato quando il controllo client si è riconnesso automaticamente a una sessione remota.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Chiamato quando un client è in corso la riconnessione automatica di una sessione con un server Host sessione Desktop remoto.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Chiamato quando un client è in corso la riconnessione automatica di una sessione con un server Host sessione Desktop remoto.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Chiamato quando il client riceve dati in un canale virtuale che può essere eseguito da script.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Chiamato quando il client chiama il [**metodo IMsRdpClient::RequestClose.**](imsrdpclient-requestclose.md)<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | Chiamato quando il controllo client è in corso di stabilire una connessione con un server Host sessione Desktop remoto.<br/>                                                                                                                                                                       |
| [**OnConnecting**](imstscaxevents-onconnecting.md)                                         | Chiamato quando il controllo client inizia a connettersi a un server in risposta a una chiamata a [**IMsTscAx::Connessione**](imstscax-connect.md).<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Chiamato quando l'utente è stato trascinato verso il basso sulla barra di connessione.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Chiamato quando viene premuto il pulsante dispositivi nella barra di connessione.<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | Chiamato quando il controllo client è stato disconnesso dal server Host sessione Desktop remoto.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Chiamato quando il client entra in modalità schermo intero. Ad esempio, questo evento viene chiamato quando l'utente preme la combinazione di tasti di scelta rapida in modalità schermo intero (CTRL+ALT+INTERR). [](terminal-services-shortcut-keys.md)<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Chiamato quando il controllo client rileva un errore irreversibile.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Chiamato quando viene premuta la combinazione di tasti rilascia lo stato attivo. Ad esempio, questo evento viene chiamato quando l'utente preme CTRL+ALT+FRECCIA SINISTRA o la combinazione di tasti CTRL+ALT+FRECCIA DESTRA.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Chiamato quando l'utente non ha immesso mouse o tastiera durante il periodo di tempo impostato dal metodo [**IMsRdpClientAdvancedSettings::p ut \_ MinutesToIdleTimeout.**](imsrdpclientadvancedsettings-minutestoidletimeout.md)<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Chiamato quando il client esce dalla modalità schermo intero. Ad esempio, questo evento viene chiamato quando l'utente preme la combinazione di tasti di scelta rapida in modalità schermo intero (CTRL+ALT+INTERR). [](terminal-services-shortcut-keys.md)<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | Chiamato quando il controllo client ha eseguito correttamente l'accesso a un server Host sessione Desktop remoto, dopo la visualizzazione della finestra di dialogo Windows Accesso remoto.<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | Chiamato quando si verifica un errore di accesso o un altro evento di accesso.<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Chiamato quando la modalità di input del mouse è stata modificata.<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | Chiamato quando lo stato della rete è stato modificato.<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | Chiamato durante la sequenza di connessione quando il client recupera la chiave pubblica dal server. Questo evento viene chiamato solo se la **proprietà NotifyTSPublicKey** è **VARIANT \_ TRUE.**<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | Chiamato per indicare che le dimensioni del controllo client sul desktop remoto sono state modificate in risposta a un'operazione di controllo client.<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | Chiamato quando viene visualizzato un programma RemoteApp.<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | Chiamato quando un programma RemoteApp restituisce un risultato al controllo client.<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | Chiamato quando viene visualizzata una finestra di RemoteApp.<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | Chiamato quando l'utente preme il **pulsante Riduci** a icona sulla barra di connessione in modalità schermo intero. L'attivazione di questo evento è una richiesta ridotta al minimo dall'applicazione contenitore.<br/>                                                                                              |
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

La **classe MsRdpClient6** ha queste proprietà.




| Proprietà | Tipo di accesso | Descrizione | 
|----------|-------------|-------------|
| <a href="imstscax-advancedsettings.md"><strong>Impostazioni avanzate</strong></a><br /> | Sola lettura<br /> | Puntatore <a href="imstscadvancedsettings-interface.md"><strong>a interfaccia IMsTscAdvancedSettings.</strong></a><br /> | 
| <a href="imsrdpclient-advancedsettings2.md"><strong>Impostazioni avanzate2</strong></a><br /> | Sola lettura<br /> | Puntatore <a href="imsrdpclientadvancedsettings-interface.md"><strong>all'interfaccia IMsRdpClientAdvancedSettings,</strong></a> usata per impostare le impostazioni avanzate per il controllo client.<br /> | 
| <a href="imsrdpclient2-advancedsettings3.md"><strong>Impostazioni avanzate3</strong></a><br /> | Sola lettura<br /> | Puntatore <a href="imsrdpclientadvancedsettings2.md"><strong>all'interfaccia IMsRdpClientAdvancedSettings2,</strong></a> usata per impostare le impostazioni avanzate per il controllo client.<br /> | 
| <a href="imsrdpclient3-advancedsettings4.md"><strong>Impostazioni avanzate4</strong></a><br /> | Sola lettura<br /> | Puntatore <a href="imsrdpclientadvancedsettings3.md"><strong>all'interfaccia IMsRdpClientAdvancedSettings3,</strong></a> usata per impostare le impostazioni avanzate per il controllo client.<br /> | 
| <a href="imsrdpclient4-advancedsettings5.md"><strong>Impostazioni avanzate5</strong></a><br /> | Sola lettura<br /> | Puntatore <a href="imsrdpclientadvancedsettings4.md"><strong>a interfaccia IMsRdpClientAdvancedSettings4.</strong></a><br /> | 
| <a href="imsrdpclient5-advancedsettings6.md"><strong>Impostazioni avanzate6</strong></a><br /> | Sola lettura<br /> | Interfaccia di <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5.</strong></a><br /> | 
| <a href="imsrdpclient6-advancedsettings7.md"><strong>Impostazioni avanzate7</strong></a><br /> | Sola lettura<br /> | Interfaccia di <a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6.</strong></a><br /> | 
| <a href="imsrdpclientnonscriptable4-allowcredentialsaving.md"><strong>AllowCredentialSaving</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se nella finestra di dialogo delle credenziali viene visualizzata una casella di controllo per abilitare il salvataggio delle credenziali.<br /> | 
| <a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a><br /> | Lettura/Scrittura<br /> | Questa proprietà non è supportata.<br /> | 
| <a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a><br /> | Lettura/Scrittura<br /> | Questa proprietà non è supportata.<br /> | 
| <a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a><br /> | Sola lettura<br /> | Livello massimo di crittografia del controllo corrente.<br /> | 
| <a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a><br /> | Sola scrittura<br /> | La Desktop remoto ActiveX password di controllo, in formato testo non crittografato.<br /> | 
| <a href="imsrdpclient-colordepth.md"><strong>ColorDepth</strong></a><br /> | Lettura/Scrittura<br /> | Profondità del colore del controllo corrente.<br /> | 
| <a href="imstscax-connected.md"><strong>Connesso</strong></a><br /> | Sola lettura<br /> | Stato di connessione del controllo corrente.<br /> | 
| <a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a><br /> | Lettura/Scrittura<br /> | Testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.<br /> | 
| <a href="imstscax-connectingtext.md"><strong>Connessione di testo</strong></a><br /> | Lettura/Scrittura<br /> | Testo visualizzato al centro nel controllo mentre il controllo è connesso.<br /> | 
| <a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br /> | Lettura/Scrittura<br /> | Stringa di testo da visualizzare per la barra di connessione.<br /> | 
| <a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br /> | Lettura/Scrittura<br /> | Altezza del controllo corrente, in pixel, sul desktop remoto iniziale.<br /> | 
| <a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br /> | Lettura/Scrittura<br /> | Larghezza del controllo corrente, in pixel, sul desktop remoto iniziale.<br /> | 
| <a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br /> | Sola lettura<br /> | Raccolta di dispositivi PnP disponibili per il reindirizzamento.<br /> | 
| <a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a><br /> | Lettura/Scrittura<br /> | Testo visualizzato centrato nel controllo prima che venga terminata una connessione.<br /> | 
| <a href="imstscax-domain.md"><strong>Dominio</strong></a><br /> | Lettura/Scrittura<br /> | Dominio a cui l'utente corrente accede.<br /> | 
| <a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br /> | Sola lettura<br /> | Raccolta di unità disco disponibili per il reindirizzamento.<br /> | 
| <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se CredSSP è abilitato per questa connessione.<br /> | 
| <a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br /> | Sola lettura<br /> | Informazioni estese sul motivo della disconnessione del controllo client.<br /> | 
| <a href="imsrdpclient-fullscreen.md"><strong>FullScreen</strong></a><br /> | Lettura/Scrittura<br /> | Indica se il controllo è in modalità schermo intero.<br /> | 
| <a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br /> | Sola scrittura<br /> | Titolo della finestra visualizzato quando il controllo è in modalità schermo intero.<br /> | 
| <a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br /> | Sola lettura<br /> | Indica se il controllo ha visualizzato una barra di scorrimento orizzontale.<br /> | 
| <a href="imsrdpclientnonscriptable4-launchedviaclientshellinterface.md"><strong>LaunchedViaClientShellInterface</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se l'utente ha avviato il controllo client usando l'interfaccia Accesso Web Desktop remoto.<br /> | 
| <a href="imsrdpclientnonscriptable4-markrdpsettingssecure.md"><strong>MarkRdpSettingsSecure</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se le impostazioni RDP sono contrassegnate come sicure.<br /> | 
| <a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br /> | Sola lettura<br /> | Impostazioni client per l'utilità di avvio del portale Web.<br /> | 
| <a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se l'impostazione NegotiateSecurityLayer è supportata per questa connessione.<br /><blockquote>[!Note]<br />Quando <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> è abilitato e presente nel client o quando Secure Sockets Layer (SSL) è abilitato con l'autenticazione utente, NegotiateSecurityLayer viene ignorato.</blockquote><br /> | 
| <a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br /> | Lettura/Scrittura<br /> | Questa proprietà non è supportata.<br /> | 
| <a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br /> | Lettura/Scrittura<br /> | Questa proprietà non è supportata.<br /> | 
| <a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se deve essere visualizzata la finestra di dialogo Richiedi credenziali.<br /> | 
| <a href="imsrdpclientnonscriptable4-promptforcredsonclient.md"><strong>PromptForCredsOnClient</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se il controllo client visualizza una finestra di dialogo che richiede le credenziali.<br /> | 
| <a href="imsrdpclientnonscriptable4-publishercertificatechain.md"><strong>PublisherCertificateChain</strong></a><br /> | Lettura/Scrittura<br /> | Specifica la catena di certificati dell'editore. La catena viene archiviata in una variante di tipo VT_BYREF che contiene un puntatore a una <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context"><strong>CERT_CHAIN_CONTEXT</strong></a> struttura.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se i dispositivi PnP collegati dinamicamente enumerati durante una sessione sono disponibili per il reindirizzamento.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se le unità PnP collegate in modo dinamico enumerate durante una sessione sono disponibili per il reindirizzamento.<br /> | 
| <a href="imsrdpclientnonscriptable4-redirectionwarningtype.md"><strong>RedirectionWarningType</strong></a><br /> | Lettura/Scrittura<br /> | Controlla la presenza e l'aspetto della finestra di dialogo di reindirizzamento.<br /> | 
| <a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br /> | Sola lettura<br /> | Impostazione remoteApp client.<br /> | 
| <a href="imstscax-securedsettings.md"><strong>Impostazioni protette</strong></a><br /> | Sola lettura<br /> | Puntatore <a href="imstscsecuredsettings-interface.md"><strong>a interfaccia IMsTscSecuredSettings.</strong></a><br /> | 
| <a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br /> | Sola lettura<br /> | Puntatore <a href="imsrdpclientsecuredsettings-interface.md"><strong>all'interfaccia IMsRdpClientSecuredSettings,</strong></a> usata per impostare le impostazioni protette per il controllo client.<br /> | 
| <a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br /> | Sola lettura<br /> | Indica se <a href="imstscsecuredsettings-interface.md"><strong>l'interfaccia IMsTscSecuredSettings</strong></a> è disponibile.<br /> | 
| <a href="imstscax-server.md"><strong>Server</strong></a><br /> | Lettura/Scrittura<br /> | Nome del server a cui è connesso il controllo corrente.<br /> | 
| <a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se la finestra di dialogo di avviso di sicurezza di reindirizzamento deve essere visualizzata prima di avviare una sessione.<br /> | 
| <a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br /> | Lettura/Scrittura<br /> | Indica se il controllo stabilirà la connessione al server Host sessione Desktop remoto immediatamente all'avvio.<br /> | 
| <a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br /> | Sola lettura<br /> | Impostazione di Gateway Desktop remoto client.<br /> | 
| <a href="imsrdpclient6-transportsettings2.md"><strong>TransportSettings2</strong></a><br /> | Sola lettura<br /> | Interfaccia di <a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2.</strong></a><br /> | 
| <a href="imsrdpclientnonscriptable4-trustedzonesite.md"><strong>TrustedZoneSite</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se il sito Web da cui l'utente ha avviato la connessione si trova nell'elenco dei siti attendibili del computer client.<br /> | 
| <a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br /> | Lettura/Scrittura<br /> | Handle di finestra che deve essere la finestra padre per il controllo . In questo modo tutte le finestre visualizzate dal controllo possono essere modali correttamente rispetto alle finestre visualizzate dall'applicazione padre.<br /> | 
| <a href="imstscax-username.md"><strong>Nome utente</strong></a><br /> | Lettura/Scrittura<br /> | Credenziali di accesso del nome utente.<br /> | 
| <a href="imstscax-version.md"><strong>Versione</strong></a><br /> | Sola lettura<br /> | Numero di versione del controllo corrente.<br /> | 
| <a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br /> | Sola lettura<br /> | Indica se il controllo visualizza una barra di scorrimento verticale.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se la finestra di dialogo di avviso di sicurezza deve includere un avviso sul reindirizzamento degli Appunti prima di avviare una sessione.<br /> | 
| <a href="imsrdpclientnonscriptable4-warnaboutprinterredirection.md"><strong>WarnAboutPrinterRedirection</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se nella finestra di dialogo di reindirizzamento viene visualizzato un messaggio sul reindirizzamento della stampante prima di avviare una sessione.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br /> | Lettura/Scrittura<br /> | Specifica se l'avviso di sicurezza deve includere un avviso sull'invio di credenziali al server remoto prima di avviare una sessione.<br /> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsRdpClient6 è definito come 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Desktop remoto ActiveX classi di controlli](remote-desktop-activex-control-classes.md)
</dt> </dl>

