---
description: Recupera una copia del descrittore di sicurezza che protegge la chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: Funzione ORGetKeySecurity (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 786321db22c513e7698fcd1661d173ccb5fdf76f1b09d9dd3e739ddf3fb2ca47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984161"
---
# <a name="orgetkeysecurity-function"></a>Funzione ORGetKeySecurity

Recupera una copia del descrittore di sicurezza che protegge la chiave del Registro di sistema aperta specificata in un hive del Registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Handle* \[ Pollici\]
</dt> <dd>

Handle di una chiave del Registro di sistema aperta in un hive del Registro di sistema offline.

</dd> <dt>

*SecurityInformation* \[ Pollici\]
</dt> <dd>

Valore [SECURITY \_ INFORMATION](../secauthz/security-information.md) che indica le informazioni di sicurezza richieste.

</dd> <dt>

*pSecurityDescriptor* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve una copia del descrittore di sicurezza richiesto. Questo parametro può essere **NULL**.

</dd> <dt>

*lpcbSecurityDescriptor* \[ in, out\]
</dt> <dd>

Puntatore a una variabile che specifica le dimensioni, in byte, del buffer a cui punta il *parametro pSecurityDescriptor.* Quando la funzione viene restituita, la variabile contiene il numero di byte scritti nel buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce ERROR \_ SUCCESS.

Se la funzione ha esito negativo, restituisce un codice di errore diverso da zero definito in Winerror.h. È possibile usare la [funzione FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT \_ MESSAGE FROM SYSTEM per ottenere una \_ \_ descrizione generica dell'errore.

Se il buffer specificato dal *parametro pSecurityDescriptor* è troppo piccolo, la funzione restituisce ERROR INSUFFICIENT BUFFER e il parametro \_ \_ *lpcbSecurityDescriptor* contiene il numero di byte necessari per il descrittore di sicurezza richiesto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows Libreria del Registro di sistema offline versione 1.0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORSetKeySecurity**](orsetkeysecurity.md)
</dt> <dt>

[INFORMAZIONI SULLA \_ SICUREZZA](../secauthz/security-information.md)
</dt> </dl>

 

 
