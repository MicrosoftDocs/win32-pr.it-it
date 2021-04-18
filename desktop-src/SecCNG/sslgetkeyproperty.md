---
description: Recupera il valore di una proprietà denominata per un oggetto chiave del provider SSL (Secure Sockets Layer Protocol).
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Funzione SslGetKeyProperty (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316720"
---
# <a name="sslgetkeyproperty-function"></a>SslGetKeyProperty (funzione)

La funzione **SslGetKeyProperty** Recupera il valore di una proprietà denominata per un oggetto chiave del provider SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HKEY* \[ in\]
</dt> <dd>

Handle del provider SSL.

</dd> <dt>

*pszProperty* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che contiene il nome della proprietà da recuperare. Può essere uno degli [**identificatori di proprietà di archiviazione chiavi**](key-storage-property-identifiers.md) predefiniti o un identificatore di proprietà personalizzato.

</dd> <dt>

*ppbOutput* \[ out\]
</dt> <dd>

Puntatore a un buffer che riceve il valore della proprietà. Il chiamante della funzione deve liberare questo buffer chiamando la funzione [**SslFreeBuffer**](sslfreebuffer.md) .

</dd> <dt>

*pcbOutput* \[ out\]
</dt> <dd>

Dimensione, in byte, del buffer *pbOutput* .

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Uno degli handle forniti non è valido.<br/>    |
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Uno dei parametri specificati non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

