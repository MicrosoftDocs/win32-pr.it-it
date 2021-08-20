---
description: Il metodo AllocFormatBuffer alloca memoria per il blocco di formato.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Metodo CMediaType.AllocFormatBuffer (Mtype.h)
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
ms.openlocfilehash: 2c53e739237f2d61a6c59c7fac96e1b97e6343fa6dd209bcf72700cefab7d599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073985"
---
# <a name="cmediatypeallocformatbuffer-method"></a>Metodo CMediaType.AllocFormatBuffer

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

Restituisce un puntatore al nuovo blocco in caso di esito positivo. In caso contrario, restituisce **NULL.**

## <a name="remarks"></a>Commenti

Se il metodo alloca correttamente un nuovo blocco di formato, libera il blocco di formato esistente. Se l'allocazione non riesce, il metodo lascia il blocco di formato esistente.

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

 

 




