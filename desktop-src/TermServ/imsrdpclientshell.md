---
title: Interfaccia IMsRdpClientShell
description: Connessione Desktop remoto (RDC) client usate per avviare il client da Desktop remoto Accesso Web (rd Accesso Web) o da altri portali Web.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientShell Servizi Desktop remoto
- Interfaccia IMsRdpClientShell Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8593a890097bbfaf6d9c9876bb56d92794ce204f38f349c72beb73b8d28403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621031"
---
# <a name="imsrdpclientshell-interface"></a>Interfaccia IMsRdpClientShell

Connessione Desktop remoto (RDC) client usate per avviare il client da Desktop remoto Accesso Web (rd Accesso Web) o da altri portali Web.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpClientShell** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsRdpClientShell** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IMsRdpClientShell.**



| Metodo                                                     | Descrizione                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| [**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85)) | Recupera una singola proprietà RDP.<br/>                  |
| [**Launch**](imsrdpclientshell-launch.md)                 | Avvia il contenuto di file remoti dal portale Web.<br/> |
| [**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85)) | Imposta una singola proprietà RDP.<br/>                       |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IMsRdpClientShell.**



| Proprietà                                                                                              | Tipo di accesso           | Descrizione                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**IsRemoteProgramClientInstalled**](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | Sola lettura<br/>  | Recupera se il client Connessione Desktop remoto (RDC) supporta la funzionalità RemoteApp.<br/> |
| [**PublicMode**](imsrdpclientshell-publicmode.md)<br/>                                         | Lettura/Scrittura<br/> | Recupera se la modalità pubblica è abilitata.<br/>                                                      |
| [**RdpFileContents**](imsrdpclientshell-rdpfilecontents.md)<br/>                               | Lettura/Scrittura<br/> | Versione di flusso del file di configurazione RDP.<br/>                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsRdpClientShell IID è definito come \_ d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Connessione Web Desktop remoto riferimento](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

