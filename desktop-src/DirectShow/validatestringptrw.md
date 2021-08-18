---
description: Verifica che il processo chiamante abbia accesso in lettura a una stringa di caratteri wide. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: 526e8027-31e5-428d-856d-9fc6698693c3
title: Macro ValidateStringPtrW (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrW
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 71567070618796ad564b7f7fb5e8d854f580d482e91d9f4fd7381a582e32495c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755671"
---
# <a name="validatestringptrw-macro"></a>Macro ValidateStringPtrW

Verifica che il processo chiamante abbia accesso in lettura a una stringa di caratteri wide. In caso contrario, la macro chiama la macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Questa macro è deprecata. In Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcun'operazione.

 

## <a name="syntax"></a>Sintassi


```C++
void ValidateStringPtrW(
   LPCWSTR p
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*P* 
</dt> <dd>

Puntatore a una stringa di caratteri wide con terminazione NULL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa macro viene ignorata a meno che non venga definito DEBUG, DEBUG o VFWROBUST quando viene DirectShow file di intestazione della \_ classe base. Questa macro può avere un costo significativo per le prestazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di convalida dei puntatori](pointer-validation-macros.md)
</dt> </dl>

 

 




