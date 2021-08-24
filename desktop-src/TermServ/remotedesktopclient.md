---
title: Classe RemoteDesktopClient
description: Implementa l'app microsoft Windows Store Desktop remoto controllo client versione 1.
ms.assetid: 0910883A-BD49-4908-8423-1FC280E0FE0C
ms.tgt_platform: multiple
keywords:
- Classe RemoteDesktopClient Servizi Desktop remoto
- Classe RemoteDesktopClient Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- RemoteDesktopClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad76c8c189854a28709765c5677d047590216ae8ab6271d44c595f7b24fdd88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865900"
---
# <a name="remotedesktopclient-class"></a>Classe RemoteDesktopClient

Implementa l'app di Microsoft Windows Store Desktop remoto controllo client - versione 1

Questa classe implementa le interfacce seguenti.

-   [**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
-   [**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)

**RemoteDesktopClient** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe RemoteDesktopClient** include questi metodi.



| Metodo                                                                                      | Descrizione                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent)                                     | Associa un gestore eventi a un evento .<br/>                                                                                                                  |
| [**Connettere**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect)                                             | Avvia una connessione usando le proprietà attualmente impostate nel controllo client del contenitore di app Remote Desktop Protocol (RDP).<br/>                         |
| [**DeleteSavedCredentials**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials)               | Elimina le credenziali salvate per il computer remoto specificato.<br/>                                                                                            |
| [**detachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent)                                     | Scollega un gestore eventi da un evento .<br/>                                                                                                                |
| [**Disconnetti**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect)                                       | Disconnette la connessione attiva.<br/>                                                                                                                      |
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Chiamato quando il controllo client riceve un messaggio amministrativo.<br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Chiamato quando il controllo client si è riconnesso automaticamente a una sessione remota.<br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Chiamato quando il controllo client tenta di ristabilire automaticamente una connessione a una sessione remota.<br/>                                                  |
| [**OnConnected**](iremotedesktopclientevents-onconnected.md)                               | Chiamato quando il controllo client si è connesso a una sessione remota.<br/>                                                                                       |
| [**OnConnecting**](iremotedesktopclientevents-onconnecting.md)                             | Chiamato quando il controllo client tenta di stabilire una connessione a una sessione remota.<br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Chiamato dopo la chiusura di una finestra di dialogo visualizzata dal controllo client.<br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Chiamato prima che il controllo visualizzi una finestra di dialogo.<br/>                                                                                                        |
| [**OnDisconnected**](iremotedesktopclientevents-ondisconnected.md)                         | Chiamato quando il controllo client è stato disconnesso da una sessione remota.<br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Chiamato quando vengono premute combinazioni di tasti speciali nella sessione remota.<br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Chiamato quando il controllo client ha eseguito correttamente l'accesso a una sessione remota.<br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Chiamato quando lo stato della rete viene modificato.<br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Chiamato quando le dimensioni del desktop remoto vengono modificate.<br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Chiamato quando il controllo client ha aggiornato il proprio stato.<br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Chiamato quando il cursore del puntatore a tocco viene spostato e la [**proprietà EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) è impostata su true.<br/> |
| [**Riconnetti**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect)                                         | Avvia una riconnessione automatica del controllo client del contenitore di app Remote Desktop Protocol (RDP) per adattare la sessione alla nuova larghezza e altezza.<br/>   |
| [**UpdateSessionDisplaySettings**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings)   | Aggiorna le impostazioni di larghezza e altezza per il controllo client del contenitore di app Remote Desktop Protocol (RDP).<br/>                                               |



 

### <a name="properties"></a>Proprietà

La **classe RemoteDesktopClient** ha queste proprietà.



| Proprietà                                                             | Tipo di accesso          | Descrizione                                                                                                                                                            |
|:---------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Azioni**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_actions)<br/>           | Sola lettura<br/> | Recupera l'oggetto actions per il client Remote Desktop Protocol contenitore di app (RDP).<br/>                                                                    |
| [**Impostazioni**](iremotedesktopclient-settings.md)<br/>         | Sola lettura<br/> | Recupera l'oggetto impostazioni per il client del contenitore di app Remote Desktop Protocol (RDP).<br/>                                                                   |
| [**TouchPointer**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_touchpointer)<br/> | Sola lettura<br/> | Contiene [**l'oggetto RemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer) per il client contenitore di app Remote Desktop Protocol (RDP).<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                     |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                           |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| CLSID<br/>                    | CLSID \_ RemoteDesktopClient è definito come EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Desktop remoto ActiveX classi di controllo](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

