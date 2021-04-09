---
description: Libera una chiave, un hash o un oggetto provider.
ms.assetid: 73fa0a08-4654-4515-bdb2-9951936b689a
title: Funzione SslFreeObject (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeObject
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e7d10059942080e7794da7e6b87613189dcf9844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880853"
---
# <a name="sslfreeobject-function"></a>SslFreeObject (funzione)

La funzione **SslFreeObject** libera una chiave, un hash o un oggetto provider.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslFreeObject(
  _In_ NCRYPT_HANDLE hObject,
  _In_ DWORD         dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hObject* \[ in\]
</dt> <dd>

Handle dell'oggetto da liberare.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt> </dl>    | Handle interno non valido.<br/>  |
| <dl> <dt>**Stato \_ di 0xC0000008L \_ handle non valido**</dt> <dt></dt> </dl> | Handle fornito non valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




