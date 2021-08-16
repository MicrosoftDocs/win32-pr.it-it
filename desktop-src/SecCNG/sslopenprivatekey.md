---
description: Apre un handle per una chiave privata.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Funzione SslOpenPrivateKey (Sslprovider.h)
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
ms.openlocfilehash: bab1451ada84576ee33623dfdaa7d8dcad189e6d4ef8050b0b79fafaba11b49c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905650"
---
# <a name="sslopenprivatekey-function"></a>Funzione SslOpenPrivateKey

La **funzione SslOpenPrivateKey** apre un handle per una [*chiave privata.*](/windows/desktop/SecGloss/p-gly)

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

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle per [*l'istanza Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) protocol (SSL).

</dd> <dt>

*phPrivateKey* \[ Cambio\]
</dt> <dd>

Indirizzo di un buffer in cui scrivere l'handle nella chiave privata.

Al termine dell'uso della chiave, è necessario liberare *phPrivateKey* chiamando la [**funzione SslFreeObject.**](sslfreeobject.md)

</dd> <dt>

*pCertContext* \[ Pollici\]
</dt> <dd>

Indirizzo del certificato da cui ottenere la chiave privata.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | *L'handle hSslProvider* non è valido.<br/>                       |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | Il *parametro phPrivateKey* o *pCertContext* è **NULL.**<br/>   |



 

## <a name="remarks"></a>Commenti

La chiave privata ottenuta fa parte di una [*coppia di chiavi pubblica/privata*](/windows/desktop/SecGloss/p-gly) all'interno di un [*certificato*](/windows/desktop/SecGloss/c-gly). Questa funzione estrae semplicemente la chiave privata dal certificato specificato dal *parametro pCertContext.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

