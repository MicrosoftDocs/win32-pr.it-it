---
description: Crea una chiave temporanea da usare durante l'autenticazione che si verifica durante l'handshake SSL (Secure Sockets Layer Protocol).
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: Funzione SslCreateEphemeralKey (Sslprovider. h)
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
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310763"
---
# <a name="sslcreateephemeralkey-function"></a>SslCreateEphemeralKey (funzione)

La funzione **SslCreateEphemeralKey** crea una chiave temporanea da usare durante l'autenticazione che si verifica durante l'handshake SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider del protocollo SSL.

</dd> <dt>

*phEphemeralKey* \[ out\]
</dt> <dd>

Handle della chiave temporanea.

</dd> <dt>

*dwProtocol* \[ in\]
</dt> <dd>

Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ in\]
</dt> <dd>

Uno dei valori dell' [**identificatore del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwKeyType* \[ in\]
</dt> <dd>

Uno dei valori dell' [**identificatore del tipo di chiave del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) . Impostare questo parametro su zero per i tipi di chiave che non sono la [*crittografia a curva ellittica*](/windows/desktop/SecGloss/e-gly) (ecc).

</dd> <dt>

*dwKeyBitLen* \[ in\]
</dt> <dd>

Lunghezza, espressa in bit, della chiave.

</dd> <dt>

*pbParams* \[ in\]
</dt> <dd>

Puntatore a un buffer che contiene i parametri per la chiave che deve essere creata. Se non si usa un pacchetto di crittografia dhe ( [*Diffie-Hellman (effimero)*](/windows/desktop/SecGloss/d-gly) , impostare il parametro *pbParams* su **null** e il parametro *cbParams* su zero.

</dd> <dt>

*cbParams* \[ in\]
</dt> <dd>

Lunghezza, in byte, dei dati nel buffer di *pbParams* .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria </dl>         | La memoria disponibile non è sufficiente per allocare il buffer.<br/> |
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Handle *hSslProvider* non valido.<br/>              |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Uno dei parametri specificati non è valido.<br/>         |



 

## <a name="remarks"></a>Commenti

Quando si usa un pacchetto di crittografia DHE, l'implementazione SSL interna passa i parametri *p* e *g* del server alla funzione **SslCreateEphemeralKey** nei parametri *pbParams* e *cbParams* .

Il formato dei dati nel buffer *pbParams* è identico a quello usato quando si imposta la proprietà [**BCRYPT \_ DH \_ Parameters**](cng-property-identifiers.md) e inizia con una struttura di [**intestazione di \_ \_ parametro BCRYPT \_ DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

