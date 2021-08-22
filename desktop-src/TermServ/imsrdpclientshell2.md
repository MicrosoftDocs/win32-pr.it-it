---
title: Interfaccia IMsRdpClientShell2
description: Espone le proprietà che avviano il client Connessione Desktop remoto da Desktop remoto Accesso Web (Accesso Web Desktop remoto) o da altri portali Web.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientShell2 Servizi Desktop remoto
- Interfaccia IMsRdpClientShell2 Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e9a63e631ca88575f4b632def5e47b29b68da414d48af95d42e757dcb2da6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138654"
---
# <a name="imsrdpclientshell2-interface"></a>Interfaccia IMsRdpClientShell2

Espone le proprietà che avviano il client Connessione Desktop remoto da Desktop remoto Accesso Web (Accesso Web Desktop remoto) o da altri portali Web.

Questa interfaccia viene implementata dal controllo Servizi Desktop remoto Accesso Web, che è un wrapper per il client Connessione Desktop remoto (MsTscAx.dll) e il proxy di runtime di Connessioni RemoteApp e Desktop (Tswbprxy.exe).

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClientShell2** eredita da **IMsRdpClientShell.** **IMsRdpClientShell2** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IMsRdpClientShell2.**



| Proprietà                                                                               | Tipo di accesso          | Descrizione                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsRdpWorkspace**](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | Sola lettura<br/> | Recupera un puntatore [**all'interfaccia IMsRdpWorkspace,**](imsrdpworkspace.md) usata per gestire Connessione RemoteApp e desktop credenziali e connessioni.<br/> |
| [**SecuredSettingsEnabled**](imsrdpclientshell2-securedsettingsenabled.md)<br/> | Sola lettura<br/> | Recupera un valore che indica se la pagina Web corrente si trova in un'area di sicurezza Internet Explorer'URL attendibile.<br/>                                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

 





