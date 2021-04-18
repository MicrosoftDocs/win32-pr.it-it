---
title: Interfaccia IMsTscSecuredSettings
description: Include metodi per recuperare e impostare le proprietà del controllo ActiveX Desktop remoto che sono limitate a zone di sicurezza URL di Internet Explorer specifiche. | Interfaccia IMsTscSecuredSettings
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsTscSecuredSettings Servizi Desktop remoto
- Interfaccia IMsTscSecuredSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321461"
---
# <a name="imstscsecuredsettings-interface"></a>Interfaccia IMsTscSecuredSettings

Include metodi per recuperare e impostare le proprietà del controllo ActiveX Desktop remoto che sono limitate a zone di sicurezza URL di Internet Explorer specifiche. Le proprietà includono quelle che specificano la modalità del controllo client (modalità schermo intero o modalità finestra) e il programma da avviare dopo la connessione al server di host sessione Desktop remoto (host sessione Desktop remoto). Questi metodi sono disponibili anche tramite l'interfaccia [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .

## <a name="members"></a>Membri

L'interfaccia **IMsTscSecuredSettings** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsTscSecuredSettings** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsTscSecuredSettings** ha queste proprietà.



| Proprietà                                                              | Tipo di accesso           | Descrizione                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [**FullScreen**](imstscsecuredsettings-fullscreen.md)<br/>     | Lettura/Scrittura<br/> | Stato a schermo intero del controllo client.<br/>                    |
| [**StartProgram**](imstscsecuredsettings-startprogram.md)<br/> | Lettura/Scrittura<br/> | Programma da avviare sul server remoto dopo la connessione.<br/> |
| [**WorkDir**](imstscsecuredsettings-workdir.md)<br/>           | Lettura/Scrittura<br/> | Directory di lavoro del programma di avvio.<br/>                     |



 

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sui metodi di questa interfaccia, vedere la pagina [relativa a come fornire la sicurezza del client RDP](providing-for-rdp-client-security.md) .

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

