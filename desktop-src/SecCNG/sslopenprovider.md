---
description: Apre un handle per il provider del protocollo SSL (Secure Sockets Layer Protocol) specificato.
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: Funzione SslOpenProvider (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226011"
---
# <a name="sslopenprovider-function"></a>SslOpenProvider (funzione)

La funzione **SslOpenProvider** apre un handle per il provider del protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) specificato.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*phSslProvider* \[ out\]
</dt> <dd>

Indirizzo di un **handle NCRYPT \_ prov \_** in cui scrivere l'handle del provider.

Al termine dell'utilizzo dell'handle, è necessario liberarlo chiamando la funzione [**SslFreeObject**](sslfreeobject.md) .

</dd> <dt>

*pszProviderName* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode che contiene il nome del provider. Se il valore di questo parametro è **null**, viene restituito un handle per il **\_ \_ provider MS Schannel** .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per utilizzi futuri e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Uno degli handle forniti non è valido.<br/>                      |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Il parametro *phSslProvider* o *ppProviderList* è **null**.<br/> |
| <dl> <dt>**Stato \_ di Nessun \_**</dt> <dt>0xC0000017L</dt> di memoria </dl>      | La memoria disponibile non è sufficiente per allocare i buffer necessari.<br/>  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

