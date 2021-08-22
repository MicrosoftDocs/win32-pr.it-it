---
title: Interfaccia IMsRdpClient9
description: Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva dall'interfaccia IMsRdpClient8.
ms.assetid: 353f0328-d8a3-4466-bf23-c6d6b8a47e5d
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClient9 Servizi Desktop remoto
- Interfaccia IMsRdpClient9 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClient9
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a84530c401398f373d9ae7e2f02619f9b3abeaa9f1d51a9f550afe55a7347e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609282"
---
# <a name="imsrdpclient9-interface"></a>Interfaccia IMsRdpClient9

Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva [**dall'interfaccia IMsRdpClient8.**](imsrdpclient8.md)

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClient9** eredita da [**IMsRdpClient8**](imsrdpclient8.md). **IMsRdpClient9** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IMsRdpClient9.**



| Metodo                                                                             | Descrizione                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                   | Associa un evento.<br/>                                                                                                                                                               |
| [**Connettere**](imstscax-connect.md)                                                | Avvia una connessione usando le proprietà attualmente impostate nel controllo .<br/>                                                                                                        |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                    | Crea un oggetto canale virtuale sul lato client per ogni nome di canale virtuale specificato.<br/>                                                                                            |
| [**detachEvent**](imsrdpclient9-detachevent.md)                                   | Scollega un evento.<br/>                                                                                                                                                               |
| [**Disconnetti**](imstscax-disconnect.md)                                          | Disconnette la connessione attiva.<br/>                                                                                                                                               |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | Recupera la descrizione dell'errore per gli eventi di disconnessione della sessione.<br/>                                                                                                               |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | Recupera il testo dello stato per il codice di stato specificato.<br/>                                                                                                                         |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)          | Recupera le opzioni impostate per un canale virtuale.<br/>                                                                                                                                 |
| [**Riconnetti**](imsrdpclient8-reconnect.md)                                       | Si riconnette alla sessione remota con la nuova larghezza e altezza del desktop.<br/>                                                                                                          |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | Richiede un arresto normale del controllo Desktop remoto ActiveX normale.<br/>                                                                                                              |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                      | Invia dati al server Host sessione Desktop remoto tramite un canale virtuale creato in precedenza usando il [**metodo CreateVirtualChannels.**](imstscax-createvirtualchannels.md)<br/> |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                         | Determina l'esecuzione di un'azione nella sessione remota.<br/>                                                                                                                          |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)          | Imposta le opzioni del canale virtuale per il controllo Desktop remoto ActiveX virtuale.<br/>                                                                                                         |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | Sincronizza le impostazioni di visualizzazione della sessione.<br/>                                                                                                                                           |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Aggiorna le impostazioni di visualizzazione della sessione.<br/>                                                                                                                                                |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IMsRdpClient9.**



| Proprietà                                                                             | Tipo di accesso           | Descrizione                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Impostazioni avanzate**](imstscax-advancedsettings.md)<br/>                     | Sola lettura<br/>  | Recupera un [**puntatore a interfaccia IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md)<br/>                                                                                                                                          |
| [**Impostazioni avanzate2**](imsrdpclient-advancedsettings2.md)<br/>               | Sola lettura<br/>  | Recupera un puntatore [**all'interfaccia IMsRdpClientAdvancedSettings.**](imsrdpclientadvancedsettings-interface.md) L'interfaccia può essere usata per impostare le impostazioni avanzate per il controllo client.<br/>                                             |
| [**Impostazioni avanzate3**](imsrdpclient2-advancedsettings3.md)<br/>              | Sola lettura<br/>  | Recupera un puntatore [**all'interfaccia IMsRdpClientAdvancedSettings2.**](imsrdpclientadvancedsettings2.md) L'interfaccia può essere usata per impostare le impostazioni avanzate per il controllo client.<br/>                                                     |
| [**Impostazioni avanzate4**](imsrdpclient3-advancedsettings4.md)<br/>              | Sola lettura<br/>  | Recupera un puntatore [**all'interfaccia IMsRdpClientAdvancedSettings3.**](imsrdpclientadvancedsettings3.md)<br/>                                                                                                                                |
| [**Impostazioni avanzate5**](imsrdpclient4-advancedsettings5.md)<br/>              | Sola lettura<br/>  | Recupera un puntatore a [**un'interfaccia IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md)<br/>                                                                                                                                 |
| [**Impostazioni avanzate6**](imsrdpclient5-advancedsettings6.md)<br/>              | Sola lettura<br/>  | Recupera [**l'interfaccia IMsRdpClientAdvancedSettings5.**](imsrdpclientadvancedsettings5.md)<br/>                                                                                                                                             |
| [**Impostazioni avanzate7**](imsrdpclient6-advancedsettings7.md)<br/>              | Sola lettura<br/>  | Recupera [**l'interfaccia IMsRdpClientAdvancedSettings6.**](imsrdpclientadvancedsettings5.md)<br/>                                                                                                                                             |
| [**Impostazioni avanzate8**](imsrdpclient7-advancedsettings8.md)<br/>              | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia IMsRdpClientAdvancedSettings7.**](imsrdpclientadvancedsettings7.md)<br/>                                                                                                                     |
| [**Impostazioni avanzate9**](imsrdpclient8-advancedsettings9.md)<br/>              | Sola lettura<br/>  | Contiene un oggetto che supporta [**l'interfaccia IMsRdpClientAdvancedSettings8.**](imsrdpclientadvancedsettings8.md)<br/>                                                                                                                      |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | Sola lettura<br/>  | Recupera il livello massimo di crittografia del controllo corrente.<br/>                                                                                                                                                                           |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lettura/Scrittura<br/> | Profondità del colore (in bit per pixel) per la connessione del controllo.<br/>                                                                                                                                                                           |
| [**Connesso**](imstscax-connected.md)<br/>                                   | Sola lettura<br/>  | Recupera lo stato di connessione del controllo corrente.<br/>                                                                                                                                                                                      |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Lettura/Scrittura<br/> | Contiene il testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.<br/>                                                                                                                          |
| [**Connessione di testo**](imstscax-connectingtext.md)<br/>                         | Lettura/Scrittura<br/> | Specifica il testo visualizzato al centro nel controllo mentre il controllo è connesso.<br/>                                                                                                                                                    |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | Lettura/Scrittura<br/> | Specifica l'altezza del controllo corrente, in pixel, sul desktop remoto iniziale.<br/>                                                                                                                                                           |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | Lettura/Scrittura<br/> | Specifica la larghezza del controllo corrente, in pixel, sul desktop remoto iniziale.<br/>                                                                                                                                                            |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | Lettura/Scrittura<br/> | Specifica il testo visualizzato centrato nel controllo prima che venga terminata una connessione.<br/>                                                                                                                                                  |
| [**Dominio**](imstscax-domain.md)<br/>                                         | Lettura/Scrittura<br/> | Specifica il dominio a cui l'utente corrente accede.<br/>                                                                                                                                                                                     |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Sola lettura<br/>  | Contiene informazioni estese sul motivo della disconnessione del controllo.<br/>                                                                                                                                                                 |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Lettura/Scrittura<br/> | Determina se il controllo client è in modalità schermo intero.<br/>                                                                                                                                                                               |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | Sola scrittura<br/> | Specifica il titolo della finestra visualizzato quando il controllo è in modalità schermo intero.<br/>                                                                                                                                                               |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | Sola lettura<br/>  | Indica se il controllo ha visualizzato una barra di scorrimento orizzontale.<br/>                                                                                                                                                                        |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Sola lettura<br/>  | Recupera l'interfaccia [**IMsRdpClientShell**](imsrdpclientshell.md)dell'interfaccia delle impostazioni client gestibile tramite script.<br/>                                                                                                                                           |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia ITSRemoteProgram.**](itsremoteprogram.md)<br/>                                                                                                                                               |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia ITSRemoteProgram2.**](itsremoteprogram2.md)<br/>                                                                                                                                             |
| [**Impostazioni protette**](imstscax-securedsettings.md)<br/>                       | Sola lettura<br/>  | Recupera un [**puntatore a interfaccia IMsTscSecuredSettings.**](imstscsecuredsettings-interface.md)<br/>                                                                                                                                            |
| [**Impostazioni protette2**](imsrdpclient-securedsettings2.md)<br/>                 | Sola lettura<br/>  | Recupera un puntatore [**all'interfaccia IMsRdpClientSecuredSettings.**](imsrdpclientsecuredsettings-interface.md) Questa interfaccia può essere usata per impostare impostazioni protette per il controllo client.<br/>                                               |
| [**Impostazioni protette3**](imsrdpclient7-securedsettings3.md)<br/>                | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia IMsRdpClientSecuredSettings2.**](imsrdpclientsecuredsettings2.md)<br/>                                                                                                                       |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | Sola lettura<br/>  | Indica se [**l'interfaccia IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) è disponibile. In altre informazioni, indica se la pagina Web che contiene il controllo si trova attualmente in una delle aree di sicurezza Internet Explorer URL consentite.<br/> |
| [**Server**](imstscax-server.md)<br/>                                         | Lettura/Scrittura<br/> | Specifica il nome del server a cui è connesso il controllo corrente.<br/>                                                                                                                                                                 |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | Lettura/Scrittura<br/> | Indica se il controllo stabilirà la connessione al server Host sessione Desktop remoto immediatamente all'avvio.<br/>                                                                                                                                |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Sola lettura<br/>  | Recupera ciò che è stato passato tramite uno script [**all'interfaccia IMsRdpClientTransportSettings.**](imsrdpclienttransportsettings.md)<br/>                                                                                                         |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Sola lettura<br/>  | Recupera [**l'interfaccia IMsRdpClientTransportSettings2.**](imsrdpclienttransportsettings2.md)<br/>                                                                                                                                           |
| [**Impostazioni di trasporto3**](imsrdpclient7-transportsettings3.md)<br/>            | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia IMsRdpClientTransportSettings3.**](imsrdpclienttransportsettings3.md)<br/>                                                                                                                   |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia IMsRdpClientTransportSettings4.**](imsrdpclienttransportsettings4.md)<br/>                                                                                                                   |
| [**Nome utente**](imstscax-username.md)<br/>                                     | Lettura/Scrittura<br/> | Specifica le credenziali di accesso del nome utente.<br/>                                                                                                                                                                                                   |
| [**Versione**](imstscax-version.md)<br/>                                       | Sola lettura<br/>  | Specifica il numero di versione del controllo corrente.<br/>                                                                                                                                                                                        |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Sola lettura<br/>  | Indica se il controllo visualizza una barra di scorrimento verticale.<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

**L'interfaccia IMsRdpClient9** è stata estesa dalle interfacce seguenti, con ogni nuova interfaccia che eredita tutti i metodi e le proprietà delle interfacce precedenti:

-   [**IMsRdpClient10**](imsrdpclient10.md)

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                                                                                                                          |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                                                                                                                                                                                                                                                                                               |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                          |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient9 è definito come 28904001-04B6-436C-A55B-0AF1A0883DC9<br/>                                                                                                                                                                                                                                                                                                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Connessione Web Desktop remoto riferimento](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

