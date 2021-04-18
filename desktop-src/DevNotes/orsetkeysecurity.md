---
description: Imposta la sicurezza di una chiave del registro di sistema aperta in un hive del registro di sistema offline.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: Funzione ORSetKeySecurity (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324443"
---
# <a name="orsetkeysecurity-function"></a>ORSetKeySecurity (funzione)

Imposta la sicurezza di una chiave del registro di sistema aperta in un hive del registro di sistema offline.

## <a name="syntax"></a>Sintassi


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
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

Flag di bit che indicano il tipo di informazioni di sicurezza da impostare. Questo parametro può essere una combinazione dei flag di bit per le [ \_ informazioni di sicurezza](../secauthz/security-information.md) .

</dd> <dt>

*pSecurityDescriptor* \[ in\]
</dt> <dd>

Puntatore a una struttura [di \_ descrittori di sicurezza](/windows/win32/api/winnt/ns-winnt-security_descriptor) che specifica gli attributi di sicurezza da impostare per la chiave specificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, la funzione restituisce ERROR \_ Success.

Se la funzione ha esito negativo, restituisce un codice di errore diverso da zero definito in Winerror. h. [](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|---------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | Windows offline Registry Library versione 1,0 o successiva<br/>                      |
| Intestazione<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORGetKeySecurity**](orgetkeysecurity.md)
</dt> <dt>

[descrittore di sicurezza \_](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[informazioni di sicurezza \_](../secauthz/security-information.md)
</dt> </dl>

 

 
