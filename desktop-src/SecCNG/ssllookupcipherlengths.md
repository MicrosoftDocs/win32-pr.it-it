---
description: Restituisce una \_ \_ \_ struttura di lunghezze di crittografia SSL NCRYPT che contiene le lunghezze dell'intestazione e del trailer del protocollo di input, del pacchetto di crittografia e del tipo di chiave.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: Funzione SslLookupCipherLengths (Sslprovider. h)
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
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967133"
---
# <a name="ssllookupcipherlengths-function"></a>SslLookupCipherLengths (funzione)

La funzione **SslLookupCipherLengths** restituisce una struttura di [**\_ \_ \_ lunghezza di crittografia SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) che contiene le lunghezze dell'intestazione e del trailer del protocollo di input, del pacchetto di crittografia e del tipo di chiave.

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

*pCipherLengths* \[ out\]
</dt> <dd>

Puntatore a un buffer per ricevere la struttura [**delle \_ \_ \_ lunghezze di crittografia SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) .

</dd> <dt>

*cbCipherLengths* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer a cui punta il parametro *pCipherLengths* .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per utilizzi futuri e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Il parametro *hSslProvider* contiene un puntatore non valido.<br/>                                                      |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Il parametro *pCipherLengths* è impostato su **null** o la lunghezza del buffer specificata da *cbCipherLengths* è troppo corta.<br/> |
| <dl> <dt>**Nte \_ \_Flag non validi**</dt> <dt>0x80090009L</dt> </dl>         | Il parametro *dwFlags* deve essere impostato su zero.<br/>                                                                            |



 

## <a name="remarks"></a>Commenti

La funzione **SslLookupCipherLengths** viene chiamata per le conversazioni [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1,1 o versioni successive per eseguire una query sulle lunghezze dell'intestazione e del trailer per il protocollo richiesto, il pacchetto di crittografia e il tipo di chiave.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

