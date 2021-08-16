---
description: Verifica che il processo chiamante abbia accesso in scrittura a un blocco di memoria. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: efbb5ca6-0289-487d-b55a-f85b38d0515a
title: Macro ValidateWritePtr (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: f20739093692977b2560de465b916cac12aeb67e2dbf9a6b9488ef8cd61f544f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072125"
---
# <a name="validatewriteptr-macro"></a>Macro ValidateWritePtr

Verifica che il processo chiamante abbia accesso in scrittura a un blocco di memoria. In caso contrario, la macro chiama la macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Questa macro è deprecata. In Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcun'operazione.

 

## <a name="syntax"></a>Sintassi


```C++
void ValidateWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*P* 
</dt> <dd>

Puntatore a un blocco di memoria.

</dd> <dt>

*Cb* 
</dt> <dd>

Dimensioni del blocco di memoria, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa macro viene ignorata a meno che non venga definito DEBUG, DEBUG o VFWROBUST quando DirectShow file di intestazione della classe \_ base è incluso. Questa macro può avere un costo significativo in termini di prestazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di convalida dei puntatori](pointer-validation-macros.md)
</dt> </dl>

 

 




