---
description: Verifica che il processo chiamante disponga dell'accesso in lettura a una stringa di caratteri wide. In caso contrario, la macro chiama la macro DbgBreak.
ms.assetid: 526e8027-31e5-428d-856d-9fc6698693c3
title: Macro ValidateStringPtrW (Wxdebug. h)
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
ms.openlocfilehash: 1ece2caa0f2263c038121cd1ffd031cbe42d336a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333289"
---
# <a name="validatestringptrw-macro"></a>ValidateStringPtrW (macro)

Verifica che il processo chiamante disponga dell'accesso in lettura a una stringa di caratteri wide. In caso contrario, la macro chiama la macro [**DbgBreak**](dbgbreak.md) .

> [!Note]  
> Questa macro è deprecata. Nella Windows SDK per Windows Vista (e versioni successive) questa macro non esegue alcuna operazione.

 

## <a name="syntax"></a>Sintassi


```C++
void ValidateStringPtrW(
   LPCWSTR p
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*p* 
</dt> <dd>

Puntatore a una stringa di caratteri wide con terminazione NULL.

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

 

 




