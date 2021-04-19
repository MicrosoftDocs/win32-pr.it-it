---
description: Verifica che il processo chiamante disponga dell'accesso in lettura/scrittura a un blocco di memoria. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: 215f6db9-67b6-47e1-bee1-dc37082ae2b8
title: Macro ValidateReadWritePtr (Wxdebug. h)
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
ms.openlocfilehash: b551f3c72a2480ea1f160b2b384fe87dbede51f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333292"
---
# <a name="validatereadwriteptr-macro"></a>ValidateReadWritePtr (macro)

Verifica che il processo chiamante disponga dell'accesso in lettura/scrittura a un blocco di memoria. In caso contrario, la macro chiama la macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Questa macro è deprecata. Nella Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcuna operazione.

 

## <a name="syntax"></a>Sintassi


```C++
void ValidateReadWritePtr(
   const void *p,
         UINT cb
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*p* 
</dt> <dd>

Puntatore a un blocco di memoria.

</dd> <dt>

*CB* 
</dt> <dd>

Dimensioni in byte del blocco di memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa macro viene ignorata a meno che non venga definito DEBUG, \_ debug o VFWROBUST quando viene incluso il file di intestazione della classe base DirectShow. Questa macro può avere un costo significativo per le prestazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di convalida del puntatore](pointer-validation-macros.md)
</dt> </dl>

 

 




