---
title: Interfaccia IRemoteDesktopClientEvents
description: Fornisce metodi che ricevono informazioni dal server correlate agli eventi di controllo client.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048367"
---
# <a name="iremotedesktopclientevents-interface"></a>Interfaccia IRemoteDesktopClientEvents

Fornisce metodi che ricevono informazioni dal server correlate agli eventi di controllo client. Gli eventi includono la connessione e la disconnessione, le richieste in modalità schermo intero, l'accesso riuscito e le condizioni di errore.

## <a name="members"></a>Membri

L'interfaccia **IRemoteDesktopClientEvents** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRemoteDesktopClientEvents** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IRemoteDesktopClientEvents** dispone di questi metodi.



| Metodo                                                                                      | Descrizione                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Chiamato quando il controllo client riceve un messaggio amministrativo. <br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Chiamato quando il controllo client si è riconnesso automaticamente a una sessione remota. <br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Chiamato quando il controllo client tenta di ristabilire automaticamente una connessione a una sessione remota. <br/>                                                  |
| [**OnConnected**](iremotedesktopclientevents-onconnected.md)                               | Chiamato quando il controllo client si è connesso a una sessione remota.<br/>                                                                                        |
| [**Onconnecting**](iremotedesktopclientevents-onconnecting.md)                             | Chiamato quando il controllo client tenta di stabilire una connessione a una sessione remota. <br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Chiamato dopo che una finestra di dialogo visualizzata dal controllo client viene rilasciata. <br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Chiamato prima che il controllo visualizzi una finestra di dialogo. <br/>                                                                                                        |
| [**Disconnected**](iremotedesktopclientevents-ondisconnected.md)                         | Chiamato quando il controllo client è stato disconnesso da una sessione remota. <br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Chiamato quando vengono premuti combinazioni di tasti speciali nella sessione remota. <br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Chiamato quando il controllo client ha effettuato correttamente l'accesso a una sessione remota. <br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Chiamato quando lo stato della rete è stato modificato. <br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Chiamato quando viene modificata la dimensione del desktop remoto. <br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Chiamato quando il controllo client ha aggiornato il proprio stato. <br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Chiamato quando il cursore del puntatore tocco è stato spostato e la proprietà [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) è impostata su true. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                           |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                 |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| CLSID<br/>                    | CLSID \_ RemoteDesktopClient è definito come EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/>       |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento al controllo ActiveX Desktop remoto](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

