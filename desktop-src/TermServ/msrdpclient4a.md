---
title: Classe MsRdpClient4a
description: Controllo client RDP Microsoft (ridistribuibile)-versione 5a.
ms.assetid: D025E5A2-9A04-44BC-BE6C-581E6B34ABCF
ms.tgt_platform: multiple
keywords:
- Classe MsRdpClient4a Servizi Desktop remoto
- Classe MsRdpClient4a Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- MsRdpClient4a
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 656309444cbd39128f8c84753caebce4a12819bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963960"
---
# <a name="msrdpclient4a-class"></a>Classe MsRdpClient4a

Controllo client RDP Microsoft (ridistribuibile)-versione 5a

Questa classe implementa le interfacce seguenti.

-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)

**MsRdpClient4a** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **MsRdpClient4a** dispone di questi metodi.



| Metodo                                                                                      | Descrizione                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Connettersi**](imstscax-connect.md)                                                         | Avvia una connessione utilizzando le proprietà attualmente impostate nel controllo.<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Crea un oggetto canale virtuale sul lato client per ogni nome di canale virtuale specificato.<br/>                                                                                                                                                                                              |
| [**Disconnetti**](imstscax-disconnect.md)                                                   | Disconnette la connessione attiva.<br/>                                                                                                                                                                                                                                                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Recupera le opzioni impostate per un canale virtuale.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Notifica al modulo di reindirizzamento del dispositivo del Desktop remoto controllo ActiveX che si è verificata una modifica del dispositivo nel sistema. Questo metodo passa le notifiche di [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) al controllo.<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | Viene chiamato dopo che un controllo ActiveX Visualizza una finestra di dialogo di autenticazione (ad esempio, la finestra di dialogo errore certificato).<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | Chiamato prima che un controllo ActiveX visualizzi una finestra di dialogo di autenticazione (ad esempio, la finestra di dialogo errore certificato).<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Chiamato quando il controllo client si è riconnesso automaticamente a una sessione remota.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Chiamato quando un client è in fase di riconnessione automatica di una sessione con un server Host sessione Desktop remoto.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Chiamato quando un client è in fase di riconnessione automatica di una sessione con un server Host sessione Desktop remoto.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Chiamato quando il client riceve i dati su un canale virtuale con script.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Chiamato quando il client chiama il metodo [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) .<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | Chiamato quando il controllo client è in fase di creazione di una connessione con un server Host sessione Desktop remoto.<br/>                                                                                                                                                                       |
| [**Onconnecting**](imstscaxevents-onconnecting.md)                                         | Chiamato quando il controllo client inizia a connettersi a un server in risposta a una chiamata a [**IMsTscAx:: Connect**](imstscax-connect.md).<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Chiamato quando l'utente è stato trascinato sulla barra di connessione.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Chiamato quando viene premuto il pulsante dispositivi nella barra delle connessioni.<br/>                                                                                                                                                                                                             |
| [**Disconnected**](imstscaxevents-ondisconnected.md)                                     | Chiamato quando il controllo client è stato disconnesso dal server Host sessione Desktop remoto.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Chiamato quando il client entra in modalità schermo intero. Questo evento, ad esempio, viene chiamato quando l'utente preme la combinazione di tasti di [scelta rapida](terminal-services-shortcut-keys.md) per la modalità schermo intero (CTRL + ALT + INTERR).<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Chiamato quando il controllo client rileva un errore irreversibile.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Chiamato quando viene premuta la combinazione di tasti di attivazione della versione. Questo evento, ad esempio, viene chiamato quando l'utente preme CTRL + ALT + freccia sinistra o la combinazione di tasti CTRL + ALT + freccia destra.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Chiamato quando l'utente non dispone di input del mouse o della tastiera durante il periodo di tempo impostato dal metodo [**IMsRdpClientAdvancedSettings::p UT \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Chiamato quando il client lascia la modalità a schermo intero. Questo evento, ad esempio, viene chiamato quando l'utente preme la combinazione di tasti di [scelta rapida](terminal-services-shortcut-keys.md) per la modalità schermo intero (CTRL + ALT + INTERR).<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | Chiamato quando il controllo client ha effettuato l'accesso a un server Host sessione Desktop remoto, dopo la visualizzazione della finestra di dialogo di accesso di Windows.<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | Chiamato quando si verifica un errore di accesso o un altro evento di accesso.<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Chiamato quando viene modificata la modalità di input del mouse.<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | Chiamato quando lo stato della rete è stato modificato.<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | Chiamato durante la sequenza di connessione quando il client recupera la chiave pubblica dal server. Questo evento viene chiamato solo se la proprietà **NotifyTSPublicKey** è **Variant \_ true**.<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | Chiamato per indicare che la dimensione del controllo client sul desktop remoto è cambiata in risposta a un'operazione di controllo client.<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | Chiamato quando viene visualizzato un programma RemoteApp.<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | Chiamato quando un programma RemoteApp restituisce un risultato al controllo client.<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | Chiamato quando viene visualizzata una finestra di RemoteApp.<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | Chiamato quando l'utente preme il pulsante **Riduci a icona** sulla barra delle connessioni in modalità schermo intero. L'attivazione di questo evento è una richiesta che l'applicazione contenitore è ridotta a icona.<br/>                                                                                              |
| [**OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md)                       | Chiamato quando il client richiede di passare alla modalità a schermo intero e viene chiamato il metodo [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) per impostare la proprietà **ContainerHandledFullScreen** su un valore diverso da zero.<br/> |
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Chiamato quando il client richiede di uscire dalla modalità a schermo intero e la proprietà [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) è stata impostata su un valore diverso da zero.<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | Chiamato quando il client riceve un messaggio di sistema.<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Chiamato quando il nome utente è stato acquisito dal controllo.<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Chiamato quando il controllo client rileva una condizione di errore non irreversibile.<br/>                                                                                                                                                                                                    |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Richiede un arresto normale del controllo client.<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | Reimposta tutti gli Stati delle password nel controllo.<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Invia una serie di sequenze di tasti al controllo. Le sequenze di tasti sono nel formato del codice di analisi, ovvero i dati della tastiera delle chiavi fisiche effettive.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Invia i dati al server Host sessione Desktop remoto tramite un canale virtuale creato in precedenza tramite il metodo [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md) .<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Imposta le opzioni del canale virtuale per il controllo client.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Proprietà

La classe **MsRdpClient4a** dispone di queste proprietà.



| Proprietà                                                                                   | Tipo di accesso           | Descrizione                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                           | Sola lettura<br/>  | Puntatore di interfaccia [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .<br/>                                                                                                          |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>                     | Sola lettura<br/>  | Puntatore all'interfaccia [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) , utilizzata per impostare le impostazioni avanzate per il controllo client.<br/>                                    |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>                    | Sola lettura<br/>  | Puntatore all'interfaccia [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) , utilizzata per impostare le impostazioni avanzate per il controllo client.<br/>                                            |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>                    | Sola lettura<br/>  | Puntatore all'interfaccia [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) , utilizzata per impostare le impostazioni avanzate per il controllo client.<br/>                                            |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>                    | Sola lettura<br/>  | Puntatore di interfaccia [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .<br/>                                                                                                      |
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>                    | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                                                                                                                                                   |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>                            | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                                                                                                                                                   |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                               | Sola lettura<br/>  | Livello massimo di crittografia del controllo corrente.<br/>                                                                                                                                           |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/>              | Sola scrittura<br/> | Password del controllo ActiveX Desktop remoto in formato testo non crittografato.<br/>                                                                                                                                 |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                                   | Lettura/Scrittura<br/> | Profondità di colore del controllo corrente.<br/>                                                                                                                                                               |
| [**Connesso**](imstscax-connected.md)<br/>                                         | Sola lettura<br/>  | Stato di connessione del controllo corrente.<br/>                                                                                                                                                      |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>                | Lettura/Scrittura<br/> | Testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.<br/>                                                                                             |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                               | Lettura/Scrittura<br/> | Testo visualizzato al centro del controllo mentre è in corso la connessione del controllo.<br/>                                                                                                                    |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                                 | Lettura/Scrittura<br/> | Altezza del controllo corrente, in pixel, sul desktop remoto iniziale.<br/>                                                                                                                           |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                                   | Lettura/Scrittura<br/> | Larghezza del controllo corrente, in pixel, sul desktop remoto iniziale.<br/>                                                                                                                            |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                           | Lettura/Scrittura<br/> | Testo visualizzato al centro del controllo prima che venga terminata una connessione.<br/>                                                                                                                  |
| [**Dominio**](imstscax-domain.md)<br/>                                               | Lettura/Scrittura<br/> | Dominio a cui l'utente corrente esegue l'accesso.<br/>                                                                                                                                                     |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/>       | Sola lettura<br/>  | Informazioni estese sul motivo del controllo client per la disconnessione.<br/>                                                                                                                         |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                                   | Lettura/Scrittura<br/> | Indica se il controllo è in modalità schermo intero.<br/>                                                                                                                                             |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                             | Sola scrittura<br/> | Titolo della finestra visualizzato quando il controllo è in modalità schermo intero.<br/>                                                                                                                               |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/>       | Sola lettura<br/>  | Indica se il controllo ha visualizzato una barra di scorrimento orizzontale.<br/>                                                                                                                              |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>                | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                                                                                                                                                   |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>                        | Lettura/Scrittura<br/> | Questa proprietà non è supportata.<br/>                                                                                                                                                                   |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                             | Sola lettura<br/>  | Puntatore di interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .<br/>                                                                                                             |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                       | Sola lettura<br/>  | Puntatore all'interfaccia [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , utilizzata per impostare le impostazioni protette per il controllo client.<br/>                                       |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>               | Sola lettura<br/>  | Indica se l'interfaccia [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) è disponibile.<br/>                                                                                    |
| [**Server**](imstscax-server.md)<br/>                                               | Lettura/Scrittura<br/> | Nome del server a cui è connesso il controllo corrente.<br/>                                                                                                                                 |
| [**StartConnected**](imstscax-startconnected.md)<br/>                               | Lettura/Scrittura<br/> | Indica se il controllo stabilirà la connessione al server Host sessione Desktop remoto immediatamente all'avvio.<br/>                                                                                      |
| [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)<br/> | Lettura/Scrittura<br/> | Handle della finestra che deve essere la finestra padre del controllo. Ciò consente a qualsiasi finestra visualizzata dal controllo di essere modale correttamente rispetto a qualsiasi finestra visualizzata dall'applicazione padre.<br/> |
| [**Nome utente**](imstscax-username.md)<br/>                                           | Lettura/Scrittura<br/> | Credenziali di accesso del nome utente.<br/>                                                                                                                                                                   |
| [**Versione**](imstscax-version.md)<br/>                                             | Sola lettura<br/>  | Numero di versione del controllo corrente.<br/>                                                                                                                                                        |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>           | Sola lettura<br/>  | Indica se il controllo Visualizza una barra di scorrimento verticale.<br/>                                                                                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsRdpClient4a è definito come 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi di controlli ActiveX Desktop remoto](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

