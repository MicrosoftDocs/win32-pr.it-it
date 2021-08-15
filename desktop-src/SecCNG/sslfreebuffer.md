---
description: Usato per liberare memoria allocata da una delle funzioni Secure Sockets Layer protocol (SSL).
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: Funzione SslFreeBuffer (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6121802b8815a2e13fab0f4336420b763fe931a6e022fcce73080adfb01197c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906480"
---
# <a name="sslfreebuffer-function"></a>Funzione SslFreeBuffer

La **funzione SslFreeBuffer** viene usata per liberare memoria allocata da una delle funzioni del provider [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pvInput* \[ Pollici\]
</dt> <dd>

Puntatore al buffer di memoria da liberare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ PARAMETRO \_ NON VALIDO**</dt> <dt>0x80090027L</dt> </dl> | Il *parametro pdwProviderCount* o *ppProviderList* è **NULL.**<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

