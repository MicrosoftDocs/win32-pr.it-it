---
description: Verifica la firma specificata usando l'hash fornito e la chiave pubblica.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: Funzione SslVerifySignature (Sslprovider.h)
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
ms.openlocfilehash: b020f41822185dfc9e4e2513fc9e299bc35d9bbb258aaeddf6f1e1e8ea7b8cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905660"
---
# <a name="sslverifysignature-function"></a>Funzione SslVerifySignature

La **funzione SslVerifySignature** verifica la firma specificata usando l'hash fornito e la [*chiave pubblica*](/windows/desktop/SecGloss/p-gly). [](/windows/desktop/SecGloss/h-gly)

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

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle per [*l'istanza Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) protocol (SSL).

</dd> <dt>

*hPublicKey* \[ Pollici\]
</dt> <dd>

Handle per la chiave pubblica.

</dd> <dt>

*pbHashValue* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer contenente l'hash da utilizzare per verificare la firma.

</dd> <dt>

*cbHashValue* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer *pbHashValue.*

</dd> <dt>

*pbSignature* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer contenente la firma da verificare.

</dd> <dt>

*cbSignature* \[ Pollici\]
</dt> <dd>

Dimensione, in byte, del buffer *pbSignature.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl> | Uno degli handle forniti non è valido.<br/> |



 

## <a name="remarks"></a>Commenti

La **funzione SslVerifySignature** non è attualmente chiamata da Windows. Questa funzione è una parte obbligatoria dell'interfaccia del provider SSL e deve essere implementata completamente per garantire la compatibilità con l'inoltro.

Le implementazioni correnti del lato server della connessione [*TLS (Transport Layer Security Protocol)*](/windows/desktop/SecGloss/t-gly) chiamano la funzione [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) durante l'autenticazione client per elaborare il messaggio di verifica del certificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

