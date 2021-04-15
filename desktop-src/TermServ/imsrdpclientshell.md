---
title: Interfaccia IMsRdpClientShell
description: Impostazioni client di Connessione Desktop remoto (RDC) utilizzate per avviare il client da Desktop remoto Accesso Web (Accesso Web Desktop remoto) o da altri portali Web.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpClientShell Servizi Desktop remoto
- Interfaccia IMsRdpClientShell Servizi Desktop remoto, descritta
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
ms.openlocfilehash: b529ed1819864e5fc6106472b33ddd00312560c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477758"
---
# <a name="imsrdpclientshell-interface"></a>Interfaccia IMsRdpClientShell

Impostazioni client di Connessione Desktop remoto (RDC) utilizzate per avviare il client da Desktop remoto Accesso Web (Accesso Web Desktop remoto) o da altri portali Web.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpClientShell** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsRdpClientShell** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IMsRdpClientShell** dispone di questi metodi.



| Metodo                                                     | Descrizione                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| [**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85)) | Recupera una singola proprietà RDP.<br/>                  |
| [**Launch**](imsrdpclientshell-launch.md)                 | Avvia il contenuto del file remoto dal portale Web.<br/> |
| [**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85)) | Imposta una singola proprietà RDP.<br/>                       |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpClientShell** ha queste proprietà.



| Proprietà                                                                                              | Tipo di accesso           | Descrizione                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**IsRemoteProgramClientInstalled**](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | Sola lettura<br/>  | Recupera un valore che indica se il client di Connessione Desktop remoto (RDC) supporta la funzionalità RemoteApp.<br/> |
| [**PublicMode**](imsrdpclientshell-publicmode.md)<br/>                                         | Lettura/Scrittura<br/> | Recupera un valore che indica se è attivata la modalità pubblica.<br/>                                                      |
| [**RdpFileContents**](imsrdpclientshell-rdpfilecontents.md)<br/>                               | Lettura/Scrittura<br/> | Versione del flusso del file di configurazione RDP.<br/>                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell è definito come d012ae6d-c19a-4bfe-B367-201f8911f134<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

