---
description: Il metodo ReallocFormatBuffer rialloca il blocco di formato in una nuova dimensione.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Metodo CMediaType. ReallocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325517"
---
# <a name="cmediatypereallocformatbuffer-method"></a>CMediaType. ReallocFormatBuffer, metodo

Il metodo rialloca `ReallocFormatBuffer` il blocco di formato in una nuova dimensione.

## <a name="syntax"></a>Sintassi


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*length* 
</dt> <dd>

Nuove dimensioni richieste per il blocco di formato, in byte. Deve essere maggiore di zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore al nuovo blocco in caso di esito positivo. In caso contrario, restituisce un puntatore al blocco di formato precedente o **null**.

## <a name="remarks"></a>Commenti

Questo metodo alloca un nuovo blocco di formato. Viene copiato il maggior volume possibile del blocco di formato esistente nel nuovo blocco di formato. Se il nuovo blocco è più piccolo del blocco esistente, il blocco di formato esistente viene troncato. Se il nuovo blocco è più grande, il contenuto dello spazio aggiuntivo non è definito. Non vengono impostate in modo esplicito su zero.

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

 

 




