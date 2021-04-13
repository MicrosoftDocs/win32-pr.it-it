---
title: Metodo SendMessage della classe Win32_VirtualDesktopSession
description: Inviare un messaggio all'utente tramite la sessione desktop virtuale.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SendMessage
- Servizi Desktop remoto del metodo SendMessage, classe Win32_VirtualDesktopSession
- Classe Win32_VirtualDesktopSession Servizi Desktop remoto, metodo SendMessage
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400581"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a>Metodo SendMessage della \_ classe VirtualDesktopSession Win32

Inviare un messaggio all'utente tramite la sessione desktop virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Titolo* \[ in\]
</dt> <dd>

Titolo del dei.

</dd> <dt>

*Messaggio* \[ di in\]
</dt> <dd>

Contenuto del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualDesktopSession Win32**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





