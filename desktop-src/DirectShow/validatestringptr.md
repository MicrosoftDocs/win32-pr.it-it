---
description: Verifica che il processo chiamante abbia accesso in lettura a una stringa. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: 749a8c22-7a4a-49c2-a214-fc64dc5a0202
title: Macro ValidateStringPtr (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateReadPtr
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: e6b04b83f3bd3b938f7cc6cc488a931e34bcca6207770b44cbd3c77c01dc9624
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755691"
---
# <a name="validatestringptr-macro"></a>Macro ValidateStringPtr

Verifica che il processo chiamante abbia accesso in lettura a una stringa. In caso contrario, la macro chiama la macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Questa macro è deprecata. In Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcun'operazione.

 

## <a name="syntax"></a>Sintassi


```C++
void ValidateReadPtr(
   LPCTSTR p
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*P* 
</dt> <dd>

Puntatore a una stringa TCHAR con **terminazione NULL.**

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

 

 




