---
title: Interfaccia IMsRdpWorkspace
description: Espone metodi che gestiscono le credenziali e le connessioni Connessione RemoteApp e desktop.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpWorkspace Servizi Desktop remoto
- Interfaccia IMsRdpWorkspace Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba55a02c5d984bc87aa05caffd42b3a3b965c43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963842"
---
# <a name="imsrdpworkspace-interface"></a>Interfaccia IMsRdpWorkspace

Espone metodi che gestiscono le credenziali e le connessioni Connessione RemoteApp e desktop. Questa interfaccia viene implementata dal controllo Servizi Desktop remoto Accesso Web. Questo controllo è un wrapper per il client di Connessione Desktop remoto (MsTscAx.dll) e il proxy di runtime di connessioni RemoteApp e desktop (Tswbprxy.exe).

## <a name="members"></a>Membri

L'interfaccia **IMsRdpWorkspace** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsRdpWorkspace** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMsRdpWorkspace** dispone di questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))             | Elimina le credenziali utente associate all'ID di connessione specificato.<br/>                                                                                  |
| [**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))                       | Disconnette tutte le connessioni esistenti associate all'ID di connessione specificato ed Elimina le credenziali utente corrispondenti dall'archivio delle credenziali.<br/> |
| [**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85)) | Determina se esistono credenziali utente per l'ID di connessione specificato.<br/>                                                                                 |
| [**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))                   | Determina se Single Sign-on (SSO) è abilitato per Connessione RemoteApp e desktop.<br/>                                                                   |
| [**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))                               | Contrassegna l'autenticazione delle credenziali utente per l'ID connessione e successivamente Visualizza la notifica di connessione nell'area di notifica della barra delle applicazioni. <br/>     |
| [**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))                                 | Associa le credenziali utente e i certificati con un ID connessione.<br/>                                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace è definito come 145D0621-04CF-4FC2-A766-A81A9069CDF8<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

