---
description: Il metodo SetSubtype specifica il sottotipo.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Metodo CMediaType. SetSubtype (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327204"
---
# <a name="cmediatypesetsubtype-method"></a>CMediaType. SetSubtype, metodo

Il `SetSubtype` metodo specifica il sottotipo.

## <a name="syntax"></a>Sintassi


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*psubtype* 
</dt> <dd>

Puntatore a un **GUID** che specifica il sottotipo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




