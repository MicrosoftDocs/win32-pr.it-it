---
description: Verifica se un puntatore è allineato a un limite specificato. In caso contrario, la macro richiama la macro ASSERT. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: Macro DbgAssertAligned (Wxdebug. h)
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
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332706"
---
# <a name="dbgassertaligned-macro"></a>DbgAssertAligned (macro)

Verifica se un puntatore è allineato a un limite specificato. In caso contrario, la macro richiama la macro [**Assert**](assert.md) . Ignorato nelle compilazioni al dettaglio.

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

*allineamento* 
</dt> <dd>

Allineamento obbligatorio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di asserzione e punti di interruzione](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




