---
description: "Restituisce l'identificatore dell'algoritmo CNG (Cryptography API: Next Generation) dell'algoritmo hash utilizzato per Transport Layer Security la funzione pseudo-casuale (PRF) del protocollo di crittografia per il protocollo di input, il pacchetto di crittografia e il tipo di chiave."
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: Funzione SslGetCipherSuitePRFHashAlgorithm (Sslprovider. h)
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
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319911"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a>SslGetCipherSuitePRFHashAlgorithm (funzione)

La funzione **SslGetCipherSuitePRFHashAlgorithm** restituisce l'identificatore dell'algoritmo CNG (Cryptography API: Next Generation) dell' [*algoritmo di hash*](/windows/desktop/SecGloss/h-gly) utilizzato per Transport Layer Security la [*funzione pseudo-casuale*](/windows/desktop/SecGloss/p-gly) (PRF) del [*protocollo*](/windows/desktop/SecGloss/t-gly) di input (PRF) per il protocollo di input, il pacchetto di crittografia e il tipo di chiave.

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

*hSslProvider* \[ in\]
</dt> <dd>

Handle dell'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

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

Uno dei valori dell' [**identificatore del tipo di chiave del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) . Per i tipi di chiave che non sono la [*crittografia a curva ellittica*](/windows/desktop/SecGloss/e-gly) (ecc), impostare questo parametro su zero.

</dd> <dt>

*szPRFHash* \[ out\]
</dt> <dd>

Uno degli [**identificatori dell'algoritmo CNG**](cng-algorithm-identifiers.md) per l'hash che verrà usato per la PRF TLS.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per utilizzi futuri e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Il parametro *hSslProvider* contiene un puntatore non valido.<br/>                |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Il parametro *szPRFHash* è impostato su **null**.<br/>                                     |
| <dl> <dt>**Nte \_ 0x80090029L non \_ supportato**</dt> <dt></dt> </dl>     | La funzione selezionata non è supportata nella versione specificata dell'interfaccia.<br/> |
| <dl> <dt>**Nte \_ \_Flag non validi**</dt> <dt>0x80090009L</dt> </dl>         | Il parametro *dwFlags* deve essere impostato su zero.<br/>                                      |



 

## <a name="remarks"></a>Commenti

Questa funzione **SslGetCipherSuitePRFHashAlgorithm** viene chiamata per le conversazioni TLS 1,2 o successive per eseguire una query sull'algoritmo di hash che verrà usato in TLS PRF.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

