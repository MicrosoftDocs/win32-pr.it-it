---
description: Apre un handle per il provider Secure Sockets Layer protocol (SSL) specificato.
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: Funzione SslOpenProvider (Sslprovider.h)
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
ms.openlocfilehash: 2bd24183fd96fd177e5ec958d84e7c4751af4226bb3d76de8bea2dba4b170b4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905640"
---
# <a name="sslopenprovider-function"></a>Funzione SslOpenProvider

La **funzione SslOpenProvider** apre un handle per il provider [*di protocollo SECURE SOCKETS LAYER*](/windows/desktop/SecGloss/s-gly) (SSL) specificato.

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

*phSslProvider* \[ Cambio\]
</dt> <dd>

Indirizzo di un **handle PROV NCRYPT \_ \_** in cui scrivere l'handle del provider.

Al termine dell'uso dell'handle, è necessario liberarlo chiamando la [**funzione SslFreeObject.**](sslfreeobject.md)

</dd> <dt>

*pszProviderName* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode che contiene il nome del provider. Se il valore di questo parametro è **NULL,** viene restituito un handle per **MS \_ SCHANNEL \_ PROVIDER.**

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro è riservato per un uso futuro e deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ NON VALIDO**</dt> <dt>0x80090026L</dt> </dl>    | Uno degli handle forniti non è valido.<br/>                      |
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | Il *parametro phSslProvider* *o ppProviderList* è **NULL.**<br/> |
| <dl> <dt>**STATO \_ NO \_ MEMORY**</dt> <dt>0xC0000017L</dt> </dl>      | Memoria insufficiente per allocare i buffer necessari.<br/>  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

