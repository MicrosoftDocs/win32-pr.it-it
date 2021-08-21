---
title: Classe MsRdpClient4
description: Controllo client RDP Microsoft (ridistribuibile) - versione 5.
ms.assetid: 3F238C63-E860-4F27-B3D6-29F03B22E49E
ms.tgt_platform: multiple
keywords:
- Classe MsRdpClient4 Servizi Desktop remoto
- Classe MsRdpClient4 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- MsRdpClient4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6b4300bcad7544793f3c958809f78a0c1b1203618ccf21688f9fc0ac483faa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350243"
---
# <a name="msrdpclient4-class"></a>Classe MsRdpClient4

Controllo client RDP Microsoft (ridistribuibile) - versione 5

Questa classe implementa le interfacce seguenti.

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

**MsRdpClient4 include** questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe MsRdpClient4** include questi metodi.



| Metodo                                                                                      | Descrizione                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Connettere**](imstscax-connect.md)                                                         | Avvia una connessione utilizzando le proprietà attualmente impostate sul controllo .<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Crea un oggetto canale virtuale lato client per ogni nome di canale virtuale specificato.<br/>                                                                                                                                                                                              |
| [**Disconnetti**](imstscax-disconnect.md)                                                   | Disconnette la connessione attiva.<br/>                                                                                                                                                                                                                                                 |
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
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Invia una serie di sequenze di tasti al controllo . Le sequenze di tasti sono in formato di codice di analisi, ovvero i dati della tastiera dei tasti fisici effettivi.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Invia dati al server Host sessione Desktop remoto tramite un canale virtuale creato in precedenza usando il metodo [**IMsTscAx::CreateVirtualChannels.**](imstscax-createvirtualchannels.md)<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Imposta le opzioni del canale virtuale per il controllo client.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Proprietà

La **classe MsRdpClient4** dispone di queste proprietà.



| Proprietà                                                                                   | Tipo di accesso           | Descrizione                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Impostazioni avanzate**](imstscax-advancedsettings.md)<br/>                           | Sola lettura<br/>  | Puntatore [**a interfaccia IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md)<br/>                                                                                                          |
| [**Impostazioni avanzate2**](imsrdpclient-advancedsettings2.md)<br/>                     | Sola lettura<br/>  | Puntatore [**all'interfaccia IMsRdpClientAdvancedSettings,**](imsrdpclientadvancedsettings-interface.md) usata per impostare le impostazioni avanzate per il controllo client.<br/>                                    |
| [**Impostazioni avanzate3**](imsrdpclient2-advancedsettings3.md)<br/>                    | Sola lettura<br/>  | Puntatore [**all'interfaccia IMsRdpClientAdvancedSettings2,**](imsrdpclientadvancedsettings2.md) usata per impostare le impostazioni avanzate per il controllo client.<br/>                                            |
| [**Impostazioni avanzate4**](imsrdpclient3-advancedsettings4.md)<br/>                    | Sola lettura<br/>  | Puntatore [**all'interfaccia IMsRdpClientAdvancedSettings3,**](imsrdpclientadvancedsettings3.md) usata per impostare le impostazioni avanzate per il controllo client.<br/>                                            |
| [**Impostazioni avanzate5**](imsrdpclient4-advancedsettings5.md)<br/>                    | Sola lettura<br/>  | Puntatore [**a interfaccia IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md)<br/>                                                                                                      |
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>                    | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                                                                                                                                                   |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>                            | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                                                                                                                                                   |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                               | Sola lettura<br/>  | Livello massimo di crittografia del controllo corrente.<br/>                                                                                                                                           |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/>              | Sola scrittura<br/> | La Desktop remoto ActiveX password di controllo, in formato testo non crittografato.<br/>                                                                                                                                 |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                                   | Lettura/Scrittura<br/> | Profondità del colore del controllo corrente.<br/>                                                                                                                                                               |
| [**Connesso**](imstscax-connected.md)<br/>                                         | Sola lettura<br/>  | Stato di connessione del controllo corrente.<br/>                                                                                                                                                      |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>                | Lettura/Scrittura<br/> | Testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.<br/>                                                                                             |
| [**Connessione del testo**](imstscax-connectingtext.md)<br/>                               | Lettura/Scrittura<br/> | Testo visualizzato al centro nel controllo mentre il controllo è connesso.<br/>                                                                                                                    |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                                 | Lettura/Scrittura<br/> | Altezza del controllo corrente, in pixel, sul desktop remoto iniziale.<br/>                                                                                                                           |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                                   | Lettura/Scrittura<br/> | Larghezza del controllo corrente, in pixel, sul desktop remoto iniziale.<br/>                                                                                                                            |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                           | Lettura/Scrittura<br/> | Testo visualizzato al centro nel controllo prima che venga terminata una connessione.<br/>                                                                                                                  |
| [**Dominio**](imstscax-domain.md)<br/>                                               | Lettura/Scrittura<br/> | Dominio a cui l'utente corrente accede.<br/>                                                                                                                                                     |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/>       | Sola lettura<br/>  | Informazioni estese sul motivo della disconnessione del controllo client.<br/>                                                                                                                         |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                                   | Lettura/Scrittura<br/> | Indica se il controllo è in modalità schermo intero.<br/>                                                                                                                                             |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                             | Sola scrittura<br/> | Titolo della finestra visualizzato quando il controllo è in modalità schermo intero.<br/>                                                                                                                               |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/>       | Sola lettura<br/>  | Indica se il controllo ha visualizzato una barra di scorrimento orizzontale.<br/>                                                                                                                              |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>                | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                                                                                                                                                   |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>                        | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                                                                                                                                                   |
| [**Impostazioni protette**](imstscax-securedsettings.md)<br/>                             | Sola lettura<br/>  | Puntatore [**a interfaccia IMsTscSecuredSettings.**](imstscsecuredsettings-interface.md)<br/>                                                                                                             |
| [**Impostazioni protette2**](imsrdpclient-securedsettings2.md)<br/>                       | Sola lettura<br/>  | Puntatore [**all'interfaccia IMsRdpClientSecuredSettings,**](imsrdpclientsecuredsettings-interface.md) usata per impostare le impostazioni protette per il controllo client.<br/>                                       |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>               | Sola lettura<br/>  | Indica se [**l'interfaccia IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) è disponibile.<br/>                                                                                    |
| [**Server**](imstscax-server.md)<br/>                                               | Lettura/Scrittura<br/> | Nome del server a cui è connesso il controllo corrente.<br/>                                                                                                                                 |
| [**StartConnected**](imstscax-startconnected.md)<br/>                               | Lettura/Scrittura<br/> | Indica se il controllo stabilirà la connessione al server Host sessione Desktop remoto immediatamente all'avvio.<br/>                                                                                      |
| [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)<br/> | Lettura/Scrittura<br/> | Handle di finestra che deve essere la finestra padre per il controllo . In questo modo tutte le finestre visualizzate dal controllo saranno correttamente modali rispetto alle finestre visualizzate dall'applicazione padre.<br/> |
| [**Nome utente**](imstscax-username.md)<br/>                                           | Lettura/Scrittura<br/> | Credenziali di accesso del nome utente.<br/>                                                                                                                                                                   |
| [**Versione**](imstscax-version.md)<br/>                                             | Sola lettura<br/>  | Numero di versione del controllo corrente.<br/>                                                                                                                                                        |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>           | Sola lettura<br/>  | Indica se il controllo visualizza una barra di scorrimento verticale.<br/>                                                                                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsRdpClient4 è definito come 4EDCB26C-D24C-4E72-AF07-B576699AC0DE<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Desktop remoto ActiveX classi di controllo](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

