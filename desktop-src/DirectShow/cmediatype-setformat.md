---
description: Il metodo seformatt Inizializza il blocco di formato.
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: Metodo CMediaType. Formatter (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329532"
---
# <a name="cmediatypesetformat-method"></a>Metodo CMediaType. seformatt

Il `SetFormat` metodo inizializza il blocco di formato.

## <a name="syntax"></a>Sintassi


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFormat* 
</dt> <dd>

Puntatore a un blocco di memoria che contiene il blocco di formato.

</dd> <dt>

*length* 
</dt> <dd>

Lunghezza del blocco di formato, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se ha esito positivo o **false** se si è verificato un errore.

## <a name="remarks"></a>Commenti

Questo metodo alloca memoria per il blocco di formato e copia il buffer specificato da *pFormat* nel nuovo blocco di formato. Se il tipo di supporto contiene già un blocco di formato, viene rilasciato quello precedente. Il metodo imposta inoltre il membro **cbFormat** della struttura **del \_ \_ tipo di supporto am** .

Per impostare il tipo di formato, chiamare il metodo [**CMediaType:: SetFormatType**](cmediatype-setformattype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




