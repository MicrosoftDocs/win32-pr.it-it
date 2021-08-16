---
description: Il metodo get \_ Duration recupera la durata del flusso. Questo metodo implementa il metodo IMediaPosition::get \_ Duration.
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: CPosPassThru.get_Duration metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e39dadd5a652b7b88321f21f1d5312c1ac44a1f1f23e7be75f9aab3460938aed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915481"
---
# <a name="cpospassthruget_duration-method"></a>Metodo CPosPassThru.get \_ Duration

Il `get_Duration` metodo recupera la durata del flusso. Questo metodo implementa il [**metodo IMediaPosition::get \_ Duration.**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration)

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*plength* 
</dt> <dd>

Puntatore a una variabile che riceve la lunghezza totale del flusso, in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il **valore HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




