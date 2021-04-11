---
description: Apre un handle per una chiave privata.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Funzione SslOpenPrivateKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128803"
---
# <a name="sslopenprivatekey-function"></a>SslOpenPrivateKey (funzione)

La funzione **SslOpenPrivateKey** apre un handle per una [*chiave privata*](/windows/desktop/SecGloss/p-gly).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ in\]
</dt> <dd>

Handle per l'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

</dd> <dt>

*phPrivateKey* \[ out\]
</dt> <dd>

Indirizzo di un buffer in cui scrivere l'handle per la chiave privata.

Al termine dell'uso della chiave, è necessario liberare *phPrivateKey* chiamando la funzione [**SslFreeObject**](sslfreeobject.md) .

</dd> <dt>

*pCertContext* \[ in\]
</dt> <dd>

Indirizzo del certificato da cui ottenere la chiave privata.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria </dl>         | La memoria disponibile non è sufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Handle *hSslProvider* non valido.<br/>                       |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Il parametro *phPrivateKey* o *pCertContext* è **null**.<br/>   |



 

## <a name="remarks"></a>Commenti

La chiave privata ottenuta è parte di una [*coppia di chiavi pubblica/privata*](/windows/desktop/SecGloss/p-gly) all'interno di un [*certificato*](/windows/desktop/SecGloss/c-gly). Questa funzione estrae semplicemente la chiave privata dal certificato specificato dal parametro *pCertContext* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

