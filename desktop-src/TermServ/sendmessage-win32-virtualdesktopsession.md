---
title: Metodo SendMessage della classe Win32_VirtualDesktopSession
description: Inviare un messaggio all'utente tramite la sessione desktop virtuale.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- Metodo SendMessage Servizi Desktop remoto
- Metodo SendMessage Servizi Desktop remoto , Win32_VirtualDesktopSession classe
- Win32_VirtualDesktopSession classe Servizi Desktop remoto, metodo SendMessage
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
ms.openlocfilehash: a159d9c8b4e8c4b5086fff9c4fc6c67c0a6e33464eeefee77d15a620b157bd55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988151"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a>Metodo SendMessage della classe \_ VirtualDesktopSession Win32

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

*Titolo* \[ Pollici\]
</dt> <dd>

Titolo della confusione.

</dd> <dt>

*Messaggio* \[ Pollici\]
</dt> <dd>

Contenuto del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Root \\ CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ VirtualDesktopSession**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





