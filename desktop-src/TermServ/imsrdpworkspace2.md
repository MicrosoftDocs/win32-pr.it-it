---
title: Interfaccia IMsRdpWorkspace2
description: Espone un metodo che associa Connessione RemoteApp e desktop credenziali a una connessione.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpWorkspace Servizi Desktop remoto
- Interfaccia IMsRdpWorkspace Servizi Desktop remoto , descritta
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
ms.openlocfilehash: 38b869d3ffc83d9a4b8f3d51df0b7b14658ec3f1c561797a62dee3a574bf2803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125521"
---
# <a name="imsrdpworkspace2-interface"></a>Interfaccia IMsRdpWorkspace2

Espone un metodo che associa Connessione RemoteApp e desktop credenziali a una connessione. Questa interfaccia viene implementata dal controllo Servizi Desktop remoto Accesso Web. Questo controllo è un wrapper per il client Connessione Desktop remoto (MsTscAx.dll) e il proxy di runtime di Connessioni RemoteApp e Desktop (Tswbprxy.exe).

## <a name="members"></a>Membri

**L'interfaccia IMsRdpWorkspace** eredita da [**IMsRdpWorkspace**](imsrdpworkspace.md). **IMsRdpWorkspace2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IMsRdpWorkspace** include questi metodi.



| Metodo                                                        | Descrizione                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85)) | Associa le credenziali utente e i certificati a un ID connessione. <br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                          |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IMsRdpWorkspace2 IID è definito come \_ 145D0622-04CF-4FC3-A776-A82A9169CDF8<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

