---
description: Il metodo ReallocFormatBuffer rialloca il blocco di formato a una nuova dimensione.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Metodo CMediaType.ReallocFormatBuffer (Mtype.h)
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
ms.openlocfilehash: 7bd4d7bd27c3698f1e30c690f755f445ffaffeff37c88f27d0a5c8ba58cd2d32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768171"
---
# <a name="cmediatypereallocformatbuffer-method"></a>Metodo CMediaType.ReallocFormatBuffer

Il `ReallocFormatBuffer` metodo rialloca il blocco di formato a una nuova dimensione.

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

Restituisce un puntatore al nuovo blocco in caso di esito positivo. In caso contrario, restituisce un puntatore al blocco di formato precedente o **NULL.**

## <a name="remarks"></a>Commenti

Questo metodo alloca un nuovo blocco di formato. Copia il maggior numero possibile di blocchi di formato esistenti nel nuovo blocco di formato. Se il nuovo blocco è più piccolo del blocco esistente, il blocco di formato esistente viene troncato. Se il nuovo blocco è più grande, il contenuto dello spazio aggiuntivo non è definito. Non vengono impostate in modo esplicito su zero.

Il metodo aggiorna i **membri cbFormat** **e pbFormat** della **struttura AM MEDIA \_ \_ TYPE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaType**](cmediatype.md)
</dt> </dl>

 

 




