---
description: Recupera le informazioni sulla suite di crittografia per un protocollo, una suite di crittografia e un set di tipi di chiave specificati.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: Funzione SslLookupCipherSuiteInfo (Sslprovider.h)
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
ms.openlocfilehash: bf56f199ae0d367517558a12a0e84bf8ce26e7bdf5f70625b878066152d0b696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905610"
---
# <a name="ssllookupciphersuiteinfo-function"></a>Funzione SslLookupCipherSuiteInfo

La **funzione SslLookupCipherSuiteInfo** recupera le informazioni sulla suite di crittografia per un protocollo, una suite di crittografia e un set di tipi di chiave specificati.

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

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle per [*l'istanza Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) protocol (SSL).

</dd> <dt>

*dwProtocol* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Protocol Identifier.**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx)

</dd> <dt>

*dwCipherSuite* \[ Pollici\]
</dt> <dd>

Uno dei valori [**di CNG SSL Provider Cipher Suite Identifiers.**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx)

</dd> <dt>

*dwKeyType* \[ Pollici\]
</dt> <dd>

Uno dei valori di identificatore del tipo di chiave del [**provider SSL CNG.**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx)

</dd> <dt>

*pCipherSuite* \[ Cambio\]
</dt> <dd>

Indirizzo di un buffer che contiene una struttura [**\_ \_ CIPHER \_ SUITE SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) in cui scrivere le informazioni sulla suite di crittografia.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                    | Descrizione                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl> | *L'handle hSslProvider* non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

