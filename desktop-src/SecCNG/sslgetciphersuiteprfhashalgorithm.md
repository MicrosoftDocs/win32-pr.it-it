---
description: "Restituisce l'identificatore di algoritmo CNG (Cryptography API: Next Generation) dell'algoritmo hash usato per la funzione pseudo-casuale TLS (Transport Layer Security Protocol) per il protocollo di input, la suite di crittografia e il tipo di chiave."
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: Funzione SslGetCipherSuitePRFHashAlgorithm (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: f328f5e4746d3a66f614e8ccbbfe66bbf3475b7f7a1a98a8a68c11df96412bf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906163"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a>Funzione SslGetCipherSuitePRFHashAlgorithm

La funzione **SslGetCipherSuitePRFHashAlgorithm** restituisce l'identificatore dell'algoritmo CNG (Cryptography API: Next Generation) dell'algoritmo [*hash*](/windows/desktop/SecGloss/h-gly) usato per la funzione [*pseudo-casuale*](/windows/desktop/SecGloss/p-gly) [*TLS (Transport Layer Security Protocol)*](/windows/desktop/SecGloss/t-gly) per il protocollo di input, il pacchetto di crittografia e il tipo di chiave.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle [*dell'istanza del*](/windows/desktop/SecGloss/s-gly) provider Secure Sockets Layer protocollo SSL (Secure Sockets Layer Protocol).

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

Uno dei valori [**dell'identificatore del tipo di chiave del provider SSL CNG.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) Per i tipi di chiave che non sono ecc [*(elliptic curve cryptography),*](/windows/desktop/SecGloss/e-gly) impostare questo parametro su zero.

</dd> <dt>

*szPRFHash* \[ Cambio\]
</dt> <dd>

Uno degli identificatori [**di algoritmo CNG per**](cng-algorithm-identifiers.md) l'hash che verrà usato per la PRF TLS.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per un uso futuro e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati, i seguenti.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | Il *parametro hSslProvider* contiene un puntatore non valido.<br/>                |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON**</dt> <dt>VALIDO 0x80090027L</dt> </dl> | Il *parametro szPRFHash* è impostato su **NULL.**<br/>                                     |
| <dl> <dt>**NTE \_ NON \_ SUPPORTATO**</dt> <dt>0x80090029L</dt> </dl>     | La funzione selezionata non è supportata nella versione specificata dell'interfaccia.<br/> |
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | Il *parametro dwFlags* deve essere impostato su zero.<br/>                                      |



 

## <a name="remarks"></a>Commenti

Questa **funzione SslGetCipherSuitePRFHashAlgorithm** viene chiamata per le conversazioni TLS 1.2 o successive per eseguire query sull'algoritmo hash che verrà usato nella PRF TLS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

