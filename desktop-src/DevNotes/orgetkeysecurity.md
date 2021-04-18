---
description: Recupera una copia del descrittore di sicurezza che protegge la chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: Funzione ORGetKeySecurity (offreg. h)
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
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330863"
---
# <a name="orgetkeysecurity-function"></a>ORGetKeySecurity (funzione)

Recupera una copia del descrittore di sicurezza che protegge la chiave del registro di sistema aperta specificata in un hive del registro di sistema offline.

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

*Gestisci* \[ in\]
</dt> <dd>

Handle per una chiave del registro di sistema aperta in un hive del registro di sistema offline.

</dd> <dt>

*SecurityInformation* \[ in\]
</dt> <dd>

Valore [delle \_ informazioni di sicurezza](../secauthz/security-information.md) che indica le informazioni di sicurezza richieste.

</dd> <dt>

*pSecurityDescriptor* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer che riceve una copia del descrittore di sicurezza richiesto. Questo parametro può essere **NULL**.

</dd> <dt>

*lpcbSecurityDescriptor* \[ in uscita\]
</dt> <dd>

Puntatore a una variabile che specifica la dimensione, in byte, del buffer a cui punta il parametro *pSecurityDescriptor* . Quando la funzione restituisce, la variabile contiene il numero di byte scritti nel buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce ERROR \_ Success.

Se la funzione ha esito negativo, restituisce un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

Se il buffer specificato dal parametro *pSecurityDescriptor* è troppo piccolo, la funzione restituisce l'errore \_ buffer insufficiente \_ e il parametro *lpcbSecurityDescriptor* contiene il numero di byte necessari per il descrittore di sicurezza richiesto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORSetKeySecurity**](orsetkeysecurity.md)
</dt> <dt>

[informazioni di sicurezza \_](../secauthz/security-information.md)
</dt> </dl>

 

 
