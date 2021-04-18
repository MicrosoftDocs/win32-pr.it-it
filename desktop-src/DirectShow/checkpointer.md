---
description: Verifica se un puntatore è NULL. Se il puntatore è NULL, la funzione o il metodo in cui viene visualizzata la macro restituisce il valore specificato.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Macro CheckPoint (Wxdebug. h)
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
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329781"
---
# <a name="checkpointer-macro"></a>CheckPoint (macro)

Verifica se un puntatore è **null**. Se il puntatore è **null**, la funzione o il metodo in cui viene visualizzata la macro restituisce il valore specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*p* 
</dt> <dd>

Puntatore da verificare.

</dd> <dt>

*RET* 
</dt> <dd>

Valore restituito dalla funzione o dal metodo se *p* è **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione circostante restituisce *ret* se *p* è **null**. In caso contrario, la macro non determina la restituzione della funzione circostante.

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
| Intestazione<br/> | <dl> <dt>Wxdebug. h (include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro di convalida del puntatore](pointer-validation-macros.md)
</dt> </dl>

 

 




