---
description: Crea una chiave effimera da usare durante l'autenticazione che si verifica durante l'handshake Secure Sockets Layer protocol (SSL).
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Funzione SslCreateEphemeralKey (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: a6a54de2865df805af51b054c22d455d52914a5b00514767d432ceda28c16a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907098"
---
# <a name="sslcreateephemeralkey-function"></a>Funzione SslCreateEphemeralKey

La **funzione SslCreateEphemeralKey** crea una chiave effimera da usare durante l'autenticazione che si verifica durante l'handshake del protocollo [*Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*phEphemeralKey* \[ Cambio\]
</dt> <dd>

Handle della chiave effimera.

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

Uno dei valori [**di CNG SSL Provider Key Type Identifier.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) Impostare questo parametro su zero per i tipi di chiave che non sono ECC [*(elliptic curve cryptography).*](/windows/desktop/SecGloss/e-gly)

</dd> <dt>

*dwKeyBitLen* \[ Pollici\]
</dt> <dd>

Lunghezza, espressa in bit, della chiave.

</dd> <dt>

*pbParams* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer che contiene i parametri per la chiave da creare. Se non viene usata una suite di crittografia [*DHE (Diffie-Hellman) (effimeral) key-exchange algorithm*](/windows/desktop/SecGloss/d-gly) (DHE), impostare il *parametro pbParams* su **NULL** e il parametro *cbParams* su zero.

</dd> <dt>

*cbParams* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, dei dati nel buffer *pbParams.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insufficiente per allocare il buffer.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | *L'handle hSslProvider* non è valido.<br/>              |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | Uno dei parametri forniti non è valido.<br/>         |



 

## <a name="remarks"></a>Commenti

Quando si usa una suite di crittografia DHE, l'implementazione SSL interna passa i parametri *p* e *g* del server alla funzione **SslCreateEphemeralKey** nei *parametri pbParams* *e cbParams.*

Il formato dei dati nel buffer *pbParams* è lo stesso usato quando si imposta la proprietà [**\_ BCRYPT DH \_ PARAMETERS**](cng-property-identifiers.md) e inizia con una struttura [**BCRYPT \_ DH \_ PARAMETER \_ HEADER.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

