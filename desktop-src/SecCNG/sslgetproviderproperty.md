---
description: Recupera il valore di una proprietà del provider specificata.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Funzione SslGetProviderProperty (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bfe65fe4033397fd5885eceb3bf0d2ac9ce9aa9b487a84ab7611cb253d979220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906109"
---
# <a name="sslgetproviderproperty-function"></a>Funzione SslGetProviderProperty

La **funzione SslGetProviderProperty** recupera il valore di una proprietà del provider specificata.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle del provider [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) per il quale recuperare la proprietà.

</dd> <dt>

*pszProperty* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null contenente il nome della proprietà da recuperare.

</dd> <dt>

*ppbOutput* \[ Cambio\]
</dt> <dd>

Indirizzo di un buffer che riceve il valore della proprietà.

Il chiamante della funzione deve liberare questo buffer chiamando la [**funzione SslFreeBuffer.**](sslfreebuffer.md)

</dd> <dt>

*pcbOutput* \[ Cambio\]
</dt> <dd>

Dimensione, in byte, del buffer *pbOutput.*

</dd> <dt>

*ppEnumState* \[ in, out\]
</dt> <dd>

Indirizzo di un **puntatore VOID** che riceve informazioni sullo stato dell'enumerazione utilizzate nelle chiamate successive a questa funzione. Queste informazioni hanno significato solo per il provider SSL e sono opache per il chiamante. Il provider SSL usa queste informazioni per determinare l'elemento successivo nell'enumerazione . Se la variabile a cui punta questo parametro contiene **NULL,** l'enumerazione viene avviata dall'inizio.

Il chiamante della funzione deve liberare questa memoria chiamando la [**funzione SslFreeBuffer.**](sslfreebuffer.md)

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insufficiente per allocare i buffer necessari.<br/> |
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | *L'handle hSslProvider* non è valido.<br/>                       |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | Uno dei parametri forniti non è valido.<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

