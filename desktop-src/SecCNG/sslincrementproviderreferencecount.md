---
description: Incrementa il conteggio dei riferimenti a un'istanza Secure Sockets Layer protocol (SSL).
ms.assetid: 67e7b8b4-b073-4936-b1e0-3fc7c1c011a2
title: Funzione SslIncrementProviderReferenceCount (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslIncrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: a177d4142d304834aea773e56a09703bc4d56e6b479a2f005f00e3b692980c72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906001"
---
# <a name="sslincrementproviderreferencecount-function"></a>Funzione SslIncrementProviderReferenceCount

La **funzione SslIncrementProviderReferenceCount** incrementa il conteggio dei riferimenti a [*un'istanza*](/windows/desktop/SecGloss/s-gly) del provider SSL (Secure Sockets Layer Protocol).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslIncrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSslProvider* \[ Pollici\]
</dt> <dd>

Handle per l'istanza del provider del protocollo SSL.

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



 

