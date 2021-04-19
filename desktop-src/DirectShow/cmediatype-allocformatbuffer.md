---
description: Il metodo AllocFormatBuffer alloca memoria per il blocco di formato.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Metodo CMediaType. AllocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6a9314fd06734adcc367b7be34dc8d6d1b9d996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324021"
---
# <a name="cmediatypeallocformatbuffer-method"></a>CMediaType. AllocFormatBuffer, metodo

Il `AllocFormatBuffer` metodo alloca memoria per il blocco di formato.

## <a name="syntax"></a>Sintassi


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*length* 
</dt> <dd>

Dimensioni richieste per il blocco di formato, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore al nuovo blocco in caso di esito positivo. In caso contrario, restituisce **null**.

## <a name="remarks"></a>Commenti

Se il metodo esegue correttamente l'allocazione di un nuovo blocco di formato, libera il blocco di formato esistente. Se l'allocazione ha esito negativo, il metodo lascia il blocco di formato esistente.

Il metodo aggiorna i membri **cbFormat** e **pbFormat** della struttura **del \_ \_ tipo di supporto am** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




