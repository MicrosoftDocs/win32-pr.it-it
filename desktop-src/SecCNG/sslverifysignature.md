---
description: Verifica la firma specificata usando l'hash fornito e la chiave pubblica.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: Funzione SslVerifySignature (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cb2a50a7f16062f271a89b6061e3f2fa2dd16685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878966"
---
# <a name="sslverifysignature-function"></a>SslVerifySignature (funzione)

La funzione **SslVerifySignature** verifica la firma specificata usando l' [*hash*](/windows/desktop/SecGloss/h-gly) fornito e la [*chiave pubblica*](/windows/desktop/SecGloss/p-gly).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ in\]
</dt> <dd>

Handle per l'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

</dd> <dt>

*hPublicKey* \[ in\]
</dt> <dd>

Handle per la chiave pubblica.

</dd> <dt>

*pbHashValue* \[ in\]
</dt> <dd>

Puntatore a un buffer contenente l'hash da usare per verificare la firma.

</dd> <dt>

*cbHashValue* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer *pbHashValue* .

</dd> <dt>

*pbSignature* \[ in\]
</dt> <dd>

Puntatore a un buffer contenente la firma da verificare.

</dd> <dt>

*cbSignature* \[ in\]
</dt> <dd>

Dimensione, in byte, del buffer *pbSignature* .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl> | Uno degli handle forniti non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

La funzione **SslVerifySignature** non è attualmente chiamata da Windows. Questa funzione è una parte obbligatoria dell'interfaccia del provider SSL e deve essere implementata completamente per garantire la compatibilità con le edizioni.

Le implementazioni correnti del lato server della connessione TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) chiamano la funzione [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) durante l'autenticazione del client per elaborare il messaggio di verifica del certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

