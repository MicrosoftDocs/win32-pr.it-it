---
description: Restituisce una struttura CIPHER LENGTHS NCRYPT SSL che contiene le lunghezze di intestazione e trailer del protocollo di input, della suite di crittografia \_ e del tipo di \_ \_ chiave.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: Funzione SslLookupCipherLengths (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 3898b54946b9a1035ce8ec1fedabc218c750bff6579b39f195a1f60b378144f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905991"
---
# <a name="ssllookupcipherlengths-function"></a>Funzione SslLookupCipherLengths

La **funzione SslLookupCipherLengths** restituisce una struttura [**\_ \_ CIPHER \_ LENGTHS SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) che contiene le lunghezze di intestazione e trailer del protocollo di input, della suite di crittografia e del tipo di chiave.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle [*dell'istanza Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) protocol (SSL).

</dd> <dt>

*dwProtocol* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Protocol Identifier.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Cipher Suite Identifier.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*dwKeyType* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Key Type Identifier.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) Per i tipi di chiave che non sono crittografia [*a curva*](/windows/desktop/SecGloss/e-gly) ellittica (ECC), impostare questo parametro su zero.

</dd> <dt>

*pCipherLengths* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer per ricevere la [**struttura \_ \_ CIPHER \_ LENGTHS SSL NCRYPT.**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**)

</dd> <dt>

*cbCipherLengths* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, del buffer a cui punta il *parametro pCipherLengths.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per un uso futuro e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | Il *parametro hSslProvider* contiene un puntatore non valido.<br/>                                                      |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | Il *parametro pCipherLengths* è impostato su **NULL** o la lunghezza del buffer specificata da *cbCipherLengths* è troppo breve.<br/> |
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | Il *parametro dwFlags* deve essere impostato su zero.<br/>                                                                            |



 

## <a name="remarks"></a>Commenti

La funzione **SslLookupCipherLengths** viene chiamata per le conversazioni tls 1.1 o successive del protocollo [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) per eseguire query sulla lunghezza dell'intestazione e del trailer per il protocollo, la suite di crittografia e il tipo di chiave richiesti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

