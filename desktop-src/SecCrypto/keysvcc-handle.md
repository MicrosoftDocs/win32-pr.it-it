---
description: Il tipo di dati KEYSVCC \_ HANDLE definisce un handle del servizio chiavi. Un handle \_ HANDLE KEYSVCC viene usato dalle funzioni RKeyOpenKeyService e RKeyCloseKeyService.
ms.assetid: d0fd5184-5c8e-4f96-9ff1-8abd6f718d05
title: KEYSVCC_HANDLE (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32e34285c6291cb7cb87aeb9095e5261b43999b0eefa82e33704719e7673f1b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515951"
---
# <a name="keysvcc_handle"></a>KEYSVCC \_ HANDLE

Il **tipo di dati KEYSVCC \_ HANDLE** definisce un handle del servizio chiavi. Un handle **\_ HANDLE KEYSVCC** viene usato dalle [**funzioni RKeyOpenKeyService**](rkeyopenkeyservice.md) [**e RKeyCloseKeyService.**](rkeyclosekeyservice.md)


```C++
typedef void* KEYSVCC_HANDLE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 




