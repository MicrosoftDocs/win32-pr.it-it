---
description: Verifica se un puntatore è allineato a un limite specificato. In caso contrario, questa macro richiama la macro ASSERT. Ignorato nelle build di vendita al dettaglio.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: Macro DbgAssertAligned (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 36b835ccd7fd82e226eb76dfb45ca4cfcd034a713da0d3639e91fba8aa7e4fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953350"
---
# <a name="dbgassertaligned-macro"></a>Macro DbgAssertAligned

Verifica se un puntatore è allineato a un limite specificato. In caso contrario, questa macro richiama la macro [**ASSERT.**](assert.md) Ignorato nelle build di vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ptr* 
</dt> <dd>

Variabile puntatore.

</dd> <dt>

*Allineamento* 
</dt> <dd>

Allineamento obbligatorio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di asserzione e punto di interruzione](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




