---
description: Recupera le informazioni sul pacchetto di crittografia per un protocollo, un pacchetto di crittografia e un tipo di chiave specificati.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: Funzione SslLookupCipherSuiteInfo (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherSuiteInfo
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7aff6c9e08351ce771669535a98ec817bfc4aaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885661"
---
# <a name="ssllookupciphersuiteinfo-function"></a>SslLookupCipherSuiteInfo (funzione)

La funzione **SslLookupCipherSuiteInfo** recupera le informazioni sul pacchetto di crittografia per un protocollo specificato, un pacchetto di crittografia e un set di tipi di chiave.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslLookupCipherSuiteInfo(
  _In_  NCRYPT_PROV_HANDLE      hSslProvider,
  _In_  DWORD                   dwProtocol,
  _In_  DWORD                   dwCipherSuite,
  _In_  DWORD                   dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_SUITE *pCipherSuite,
  _In_  DWORD                   dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ in\]
</dt> <dd>

Handle per l'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

</dd> <dt>

*dwProtocol* \[ in\]
</dt> <dd>

Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ in\]
</dt> <dd>

Uno dei valori degli [**identificatori del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*dwKeyType* \[ in\]
</dt> <dd>

Uno dei valori [**identificatori del tipo di chiave del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .

</dd> <dt>

*pCipherSuite* \[ out\]
</dt> <dd>

Indirizzo di un buffer che contiene una struttura [**del \_ \_ \_ pacchetto di crittografia SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) in cui scrivere le informazioni sul pacchetto di crittografia.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl> | Handle *hSslProvider* non valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

