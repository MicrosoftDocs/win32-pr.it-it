---
title: Interfaccia IMsRdpClientSecuredSettings
description: Include metodi per recuperare e impostare le proprietà del controllo Desktop remoto ActiveX che sono limitate a specifiche aree Internet Explorer di sicurezza URL. | Interfaccia IMsRdpClientSecuredSettings
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a1b834d42c957998ad2a8eda5cd3790dd16f40dfd82a8e463bc34e510cd742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129791"
---
# <a name="imsrdpclientsecuredsettings-interface"></a>Interfaccia IMsRdpClientSecuredSettings

Include metodi per recuperare e impostare le proprietà del controllo Desktop remoto ActiveX che sono limitate a specifiche aree Internet Explorer di sicurezza URL.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClientSecuredSettings** eredita da [**IMsTscSecuredSettings.**](imstscsecuredsettings-interface.md) **IMsRdpClientSecuredSettings** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste **proprietà sono disponibili nell'interfaccia IMsRdpClientSecuredSettings.**



| Proprietà                                                                                   | Tipo di accesso           | Descrizione                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | Lettura/Scrittura<br/> | Impostazioni di reindirizzamento audio.<br/>    |
| [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | Lettura/Scrittura<br/> | Impostazioni di reindirizzamento della tastiera.<br/> |



 

## <a name="remarks"></a>Commenti

Queste proprietà non possono essere impostate quando il controllo è connesso.

Per altre informazioni sui metodi di questa interfaccia, vedere Fornire la sicurezza client [RDP.](providing-for-rdp-client-security.md)

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                       |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                 |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings è definito come 605befcf-39c1-45cc-a811-068fb7be346d<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> <dt>

[Connessione Web Desktop remoto di riferimento](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





