---
description: Controlla se un puntatore è NULL. Se il puntatore è NULL, la funzione o il metodo in cui viene visualizzata la macro restituisce il valore specificato.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Macro CheckPointer (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: ef1fa2370def45321958862ebaf3ded341b13f45ddae1ecafdc4a17e937aca08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999291"
---
# <a name="checkpointer-macro"></a>Macro CheckPointer

Controlla se un puntatore è **NULL.** Se il puntatore è **NULL,** la funzione o il metodo in cui viene visualizzata la macro restituisce il valore specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*P* 
</dt> <dd>

Puntatore da controllare.

</dd> <dt>

*Ret* 
</dt> <dd>

Valore restituito dalla funzione o dal metodo se *p* è **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione circostante restituisce *ret* se *p* è **NULL.** In caso contrario, la macro non causa la restituzione della funzione circostante.

## <a name="examples"></a>Esempio


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wxdebug.h (includere Flussi.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di convalida dei puntatori](pointer-validation-macros.md)
</dt> </dl>

 

 




