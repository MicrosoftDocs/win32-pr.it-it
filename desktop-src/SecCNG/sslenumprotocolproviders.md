---
description: Restituisce una matrice di provider Secure Sockets Layer protocol (SSL) installati.
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: Funzione SslEnumProtocolProviders (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c0e20bd98f8f3e76d4185cf2a3aa52985d73f66ff1ea61ed50bf67552330290d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906683"
---
# <a name="sslenumprotocolproviders-function"></a>Funzione SslEnumProtocolProviders

La **funzione SslEnumProtocolProviders** restituisce una matrice [*di provider Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) installati.

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdwProviderCount* \[ Cambio\]
</dt> <dd>

Puntatore a un **valore DWORD** per ricevere il numero di provider di protocolli restituiti.

</dd> <dt>

*ppProviderList* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer che riceve la matrice di [**strutture NCryptProviderName.**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername)

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per usi futuri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati, i seguenti.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | Il *parametro dwFlags* non è zero.<br/>                              |
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Memoria insufficiente per allocare i buffer necessari.<br/>     |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON**</dt> <dt>VALIDO 0x80090027L</dt> </dl> | Il *parametro pdwProviderCount* o *ppProviderList* è **NULL.**<br/> |



 

## <a name="remarks"></a>Commenti

Dopo aver terminato di usare la matrice di [**strutture NCryptProviderName,**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) chiamare la [**funzione SslFreeBuffer**](sslfreebuffer.md) per liberare la matrice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

