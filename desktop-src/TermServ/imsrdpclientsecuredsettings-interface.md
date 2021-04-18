---
title: Interfaccia IMsRdpClientSecuredSettings
description: Include metodi per recuperare e impostare le proprietà del controllo ActiveX Desktop remoto che sono limitate a zone di sicurezza URL di Internet Explorer specifiche. | Interfaccia IMsRdpClientSecuredSettings
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 396e6b58b2be0122076b5529b910423377417fa6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321561"
---
# <a name="imsrdpclientsecuredsettings-interface"></a>Interfaccia IMsRdpClientSecuredSettings

Include metodi per recuperare e impostare le proprietà del controllo ActiveX Desktop remoto che sono limitate a zone di sicurezza URL di Internet Explorer specifiche.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClientSecuredSettings** eredita da [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md). **IMsRdpClientSecuredSettings** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClientSecuredSettings** ha queste proprietà.



| Proprietà                                                                                   | Tipo di accesso           | Descrizione                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | Lettura/Scrittura<br/> | Impostazioni del reindirizzamento audio.<br/>    |
| [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | Lettura/Scrittura<br/> | Impostazioni di Reindirizzamento da tastiera.<br/> |



 

## <a name="remarks"></a>Commenti

Non è possibile impostare queste proprietà quando il controllo è connesso.

Per ulteriori informazioni sui metodi di questa interfaccia, vedere la pagina [relativa a come fornire la sicurezza del client RDP](providing-for-rdp-client-security.md) .

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                       |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                 |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings è definito come 605befcf-39c1-45cc-A811-068fb7be346d<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





