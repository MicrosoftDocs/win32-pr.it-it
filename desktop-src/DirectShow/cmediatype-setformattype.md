---
description: Il metodo SetFormatType specifica il tipo di formato.
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: Metodo CMediaType. SetFormatType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7843c5a9788545909ef4297accfa342c08b71e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330224"
---
# <a name="cmediatypesetformattype-method"></a>CMediaType. SetFormatType, metodo

Il metodo SetFormatType '' specifica il tipo di formato.

## <a name="syntax"></a>Sintassi


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pformattype* 
</dt> <dd>

Puntatore a un **GUID** che specifica il tipo di formato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo imposta il membro **formatType** . Il tipo di formato definisce il layout del blocco di formato. Se ad esempio il formato del tipo è \_ videoinfo, il blocco di formato deve contenere una struttura **VIDEOINFOHEADER** . Per impostare il blocco di formato, chiamare il metodo [**CMediaType:: Seformatt**](cmediatype-setformat.md) . Il chiamante è responsabile di assicurarsi che il blocco di formato corrisponda al tipo di formato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 


``
