---
title: Interfaccia IMsRdpWorkspace2
description: Espone un metodo che associa Connessione RemoteApp e desktop credenziali a una connessione.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
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
ms.openlocfilehash: 3d6b5ff193eec393b67029d355a0f0c1bc67c0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048291"
---
# <a name="imsrdpworkspace2-interface"></a>Interfaccia IMsRdpWorkspace2

Espone un metodo che associa Connessione RemoteApp e desktop credenziali a una connessione. Questa interfaccia viene implementata dal controllo Servizi Desktop remoto Accesso Web. Questo controllo è un wrapper per il client di Connessione Desktop remoto (MsTscAx.dll) e il proxy di runtime di connessioni RemoteApp e desktop (Tswbprxy.exe).

## <a name="members"></a>Membri

L'interfaccia **IMsRdpWorkspace** eredita da [**IMsRdpWorkspace**](imsrdpworkspace.md). **IMsRdpWorkspace2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMsRdpWorkspace** dispone di questi metodi.



| Metodo                                                        | Descrizione                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85)) | Associa le credenziali utente e i certificati con un ID connessione. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                          |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace2 è definito come 145D0622-04CF-4fc3-A776-A82A9169CDF8<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

