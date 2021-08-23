---
description: Verifica che il processo chiamante abbia accesso in lettura/scrittura a un blocco di memoria. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: Macro ValidateReadWritePtr (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadWritePtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: ec4d1c0440d0747024efadaa441ca062da512283f5a01f29be12b19c0f7c0567
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755661"
---
# <a name="validatereadwriteptr-macro"></a>Macro ValidateReadWritePtr

Verifica che il processo chiamante abbia accesso in lettura/scrittura a un blocco di memoria. In caso contrario, la macro chiama la macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Questa macro è deprecata. In Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcun'operazione.

 

## <a name="syntax"></a>Sintassi


```C++
void ValidateReadWritePtr(
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

 

 




