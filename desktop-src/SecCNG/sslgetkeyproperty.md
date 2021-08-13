---
description: Recupera il valore di una proprietà denominata per un oggetto chiave del provider SECURE SOCKETS LAYER Protocol (SSL).
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: Funzione SslGetKeyProperty (Sslprovider.h)
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
ms.openlocfilehash: b86f8a2e76573122bcfcf809d5301bc6bf70690467527f4dc69a5ec12419f56b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906119"
---
# <a name="sslgetkeyproperty-function"></a>Funzione SslGetKeyProperty

La **funzione SslGetKeyProperty** recupera il valore di una proprietà denominata per un oggetto chiave del provider [*Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) protocol (SSL).

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

*hKey* \[ Pollici\]
</dt> <dd>

Handle del provider SSL.

</dd> <dt>

*pszProperty* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null contenente il nome della proprietà da recuperare. Può trattarsi di uno degli identificatori di proprietà Archiviazione chiave [**predefiniti**](key-storage-property-identifiers.md) o di un identificatore di proprietà personalizzato.

</dd> <dt>

*ppbOutput* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve il valore della proprietà. Il chiamante della funzione deve liberare questo buffer chiamando la [**funzione SslFreeBuffer.**](sslfreebuffer.md)

</dd> <dt>

*pcbOutput* \[ Cambio\]
</dt> <dd>

Dimensione, in byte, del buffer *pbOutput.*

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | Uno degli handle forniti non è valido.<br/>    |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | Uno dei parametri forniti non è valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

