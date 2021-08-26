---
description: Il metodo CanSeekBackward determina se il flusso può essere cercato all'indietro. Questo metodo implementa il metodo IMediaPosition::CanSeekBackward.
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Metodo CPosPassThru.CanSeekBackward (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1d989acf074eb20e6ea3387c37129700320ce782e3c5d7c8bd4320641839ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108431"
---
# <a name="cpospassthrucanseekbackward-method"></a>Metodo CPosPassThru.CanSeekBackward

Il `CanSeekBackward` metodo determina se il flusso può essere cercato all'indietro. Questo metodo implementa il [**metodo IMediaPosition::CanSeekBackward.**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward)

## <a name="syntax"></a>Sintassi


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCanSeekBackward* 
</dt> <dd>

Puntatore a una variabile che riceve il valore OATRUE se il filtro può eseguire la ricerca all'indietro oppure OAFALSE in caso contrario.

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

 

 




