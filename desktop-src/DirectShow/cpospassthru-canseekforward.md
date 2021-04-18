---
description: 'Il metodo CanSeekForward determina se il flusso può essere cercato in futuro. Questo metodo implementa il metodo IMediaPosition:: CanSeekForward.'
ms.assetid: ccb2db8d-b52e-4e3d-b49b-9689197a974a
title: Metodo CPosPassThru. CanSeekForward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekForward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 701bfdff1d3a3a37dc0e3935aa82bfca2e01cfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329519"
---
# <a name="cpospassthrucanseekforward-method"></a>CPosPassThru. CanSeekForward, metodo

Il `CanSeekForward` metodo determina se il flusso può essere cercato in futuro. Questo metodo implementa il metodo [**IMediaPosition:: CanSeekForward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekforward) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT CanSeekForward(
   LONG *pCanSeekForward
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCanSeekForward* 
</dt> <dd>

Puntatore a una variabile che riceve il valore OATRUE se il filtro può cercare in futuro oppure OAFALSE in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore **HRESULT** dal pin connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




