---
description: Verifica che il processo chiamante abbia accesso in lettura a una stringa ANSI. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: 44be67f8-9896-4360-82de-083a5f28a3d0
title: Macro ValidateStringPtrA (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateStringPtrA
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 26a0e000f5b2b8de645924300eb650a05a66a4b57c16c5eda3f124e7bc0903a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432101"
---
# <a name="validatestringptra-macro"></a>Macro ValidateStringPtrA

Verifica che il processo chiamante abbia accesso in lettura a una stringa ANSI. In caso contrario, la macro chiama la macro [**DbgBreak.**](dbgbreak.md)

> [!Note]  
> Questa macro è deprecata. In Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcun'operazione.

 

## <a name="syntax"></a>Sintassi


```C++
void ValidateStringPtrA(
   LPCSTR p
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*P* 
</dt> <dd>

Puntatore a una stringa ANSI con terminazione NULL.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa macro non restituisce un valore.

## <a name="remarks"></a>Commenti

Questa macro viene ignorata a meno che non venga definito DEBUG, DEBUG o VFWROBUST quando DirectShow file di intestazione della classe \_ base è incluso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di convalida dei puntatori](pointer-validation-macros.md)
</dt> </dl>

 

 




