---
description: Utilizzato per liberare la memoria allocata da una delle funzioni del provider di protocollo Secure Sockets Layer (SSL).
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: Funzione SslFreeBuffer (Sslprovider. h)
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
ms.openlocfilehash: bced83b52ddf37266f64ae0c2b8919902f30fff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058314"
---
# <a name="sslfreebuffer-function"></a>SslFreeBuffer (funzione)

La funzione **SslFreeBuffer** viene utilizzata per liberare la memoria allocata da una delle funzioni del provider di protocollo SSL ( [*Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Sintassi


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pvInput* \[ in\]
</dt> <dd>

Puntatore al buffer di memoria da liberare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce zero.

Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice/valore restituito                                                                                                                                                       | Descrizione                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt> </dl> | Il parametro *pdwProviderCount* o *ppProviderList* è **null**.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

