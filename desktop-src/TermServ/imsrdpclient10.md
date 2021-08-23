---
title: Interfaccia IMsRdpClient10
description: Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva dall'interfaccia IMsRdpClient9.
ms.assetid: 601f70aa-85f1-4180-921b-9f1bb31d4def
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClient10 Servizi Desktop remoto
- Interfaccia IMsRdpClient10 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClient10
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561541f170fbe6dc5342b359e5deae69d0c92469ad2d692ee4ea3b9d59904885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737241"
---
# <a name="imsrdpclient10-interface"></a>Interfaccia IMsRdpClient10

Fornisce i metodi e le proprietà necessari per configurare e usare il controllo client. Deriva [**dall'interfaccia IMsRdpClient9.**](imsrdpclient9.md)

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClient10** eredita da [**IMsRdpClient9.**](imsrdpclient9.md) **IMsRdpClient10** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IMsRdpClient10** include questi metodi.



| Metodo                                                                             | Descrizione                                                                         |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                   | Associa un evento.<br/>                                                       |
| [**detachEvent**](imsrdpclient9-detachevent.md)                                   | Scollega un evento.<br/>                                                       |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | Recupera la descrizione dell'errore per gli eventi di disconnessione della sessione.<br/>       |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | Recupera il testo dello stato per il codice di stato specificato.<br/>                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)          | Recupera le opzioni impostate per un canale virtuale.<br/>                         |
| [**Riconnetti**](imsrdpclient8-reconnect.md)                                       | Si riconnette alla sessione remota con la nuova larghezza e altezza del desktop.<br/>  |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | Richiede un arresto normale del controllo Desktop remoto ActiveX normale.<br/>      |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                         | Determina l'esecuzione di un'azione nella sessione remota.<br/>                  |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)          | Imposta le opzioni del canale virtuale per il controllo Desktop remoto ActiveX virtuale.<br/> |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | Sincronizza le impostazioni di visualizzazione della sessione.<br/>                                   |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Aggiorna le impostazioni di visualizzazione della sessione.<br/>                                        |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IMsRdpClient10.**



| Proprietà                                                                             | Tipo di accesso           | Descrizione                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Impostazioni avanzate2**](imsrdpclient-advancedsettings2.md)<br/>               | Sola lettura<br/>  | Recupera un puntatore [**all'interfaccia IMsRdpClientAdvancedSettings.**](imsrdpclientadvancedsettings-interface.md) L'interfaccia può essere usata per impostare le impostazioni avanzate per il controllo client.<br/> |
| [**Impostazioni avanzate3**](imsrdpclient2-advancedsettings3.md)<br/>              | Sola lettura<br/>  | Recupera un puntatore [**all'interfaccia IMsRdpClientAdvancedSettings2.**](imsrdpclientadvancedsettings2.md) L'interfaccia può essere usata per impostare le impostazioni avanzate per il controllo client.<br/>         |
| [**Impostazioni avanzate4**](imsrdpclient3-advancedsettings4.md)<br/>              | Sola lettura<br/>  | Recupera un puntatore [**all'interfaccia IMsRdpClientAdvancedSettings3.**](imsrdpclientadvancedsettings3.md)<br/>                                                                                    |
| [**Impostazioni avanzate5**](imsrdpclient4-advancedsettings5.md)<br/>              | Sola lettura<br/>  | Recupera un puntatore a [**un'interfaccia IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md)<br/>                                                                                     |
| [**Impostazioni avanzate6**](imsrdpclient5-advancedsettings6.md)<br/>              | Sola lettura<br/>  | Recupera [**l'interfaccia IMsRdpClientAdvancedSettings5.**](imsrdpclientadvancedsettings5.md)<br/>                                                                                                 |
| [**Impostazioni avanzate7**](imsrdpclient6-advancedsettings7.md)<br/>              | Sola lettura<br/>  | Recupera [**l'interfaccia IMsRdpClientAdvancedSettings6.**](imsrdpclientadvancedsettings5.md)<br/>                                                                                                 |
| [**Impostazioni avanzate8**](imsrdpclient7-advancedsettings8.md)<br/>              | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia IMsRdpClientAdvancedSettings7.**](imsrdpclientadvancedsettings7.md)<br/>                                                                         |
| [**Impostazioni avanzate9**](imsrdpclient8-advancedsettings9.md)<br/>              | Sola lettura<br/>  | Contiene un oggetto che supporta [**l'interfaccia IMsRdpClientAdvancedSettings8.**](imsrdpclientadvancedsettings8.md)<br/>                                                                          |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lettura/Scrittura<br/> | Profondità del colore (in bit per pixel) per la connessione del controllo.<br/>                                                                                                                               |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Lettura/Scrittura<br/> | Contiene il testo visualizzato nell'area client del controllo mentre il controllo è nello stato connesso.<br/>                                                                              |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Sola lettura<br/>  | Contiene informazioni estese sul motivo della disconnessione del controllo.<br/>                                                                                                                     |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Lettura/Scrittura<br/> | Determina se il controllo client è in modalità schermo intero.<br/>                                                                                                                                   |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Sola lettura<br/>  | Recupera l'interfaccia [**IMsRdpClientShell dell'impostazione**](imsrdpclientshell.md)client che può essere impostata tramite script.<br/>                                                                                               |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia ITSRemoteProgram.**](itsremoteprogram.md)<br/>                                                                                                   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia ITSRemoteProgram2.**](itsremoteprogram2.md)<br/>                                                                                                 |
| [**RemoteProgram3**](imsrdpclient10-remoteprogram3.md)<br/>                   | Sola lettura<br/>  | Oggetto che supporta [**l'interfaccia ITSRemoteProgram3.**](itsremoteprogram3.md)<br/>                                                                                                           |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Sola lettura<br/>  | Recupera un puntatore [**all'interfaccia IMsRdpClientSecuredSettings.**](imsrdpclientsecuredsettings-interface.md) Questa interfaccia può essere usata per impostare le impostazioni protette per il controllo client.<br/>   |
| [**Impostazioni protette3**](imsrdpclient7-securedsettings3.md)<br/>                | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia IMsRdpClientSecuredSettings2.**](imsrdpclientsecuredsettings2.md)<br/>                                                                           |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Sola lettura<br/>  | Recupera ciò che è stato passato tramite uno script [**all'interfaccia IMsRdpClientTransportSettings.**](imsrdpclienttransportsettings.md)<br/>                                                             |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Sola lettura<br/>  | Recupera [**l'interfaccia IMsRdpClientTransportSettings2.**](imsrdpclienttransportsettings2.md)<br/>                                                                                               |
| [**Impostazioni di trasporto3**](imsrdpclient7-transportsettings3.md)<br/>            | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia IMsRdpClientTransportSettings3.**](imsrdpclienttransportsettings3.md)<br/>                                                                       |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Sola lettura<br/>  | Recupera un oggetto che supporta [**l'interfaccia IMsRdpClientTransportSettings4.**](imsrdpclienttransportsettings4.md)<br/>                                                                       |



 

## <a name="remarks"></a>Commenti

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                                                                                              |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                                                                                                           |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 è definito come C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting è definito come A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> |
| IID<br/>                      | IID \_ IMsRdpClient10 è definito come 7ED92C39-EB38-4927-A70A-708AC5A59321<br/>                                                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

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

[Connessione Web Desktop remoto di riferimento](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

