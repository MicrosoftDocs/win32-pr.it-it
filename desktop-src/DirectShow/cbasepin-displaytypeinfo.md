---
description: Il metodo DisplayTypeInfo Visualizza le informazioni sul tipo di supporto durante il debug.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Metodo CBasePin. DisplayTypeInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681e424505bb2ff840ac5beaa48431f17a5d177b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329539"
---
# <a name="cbasepindisplaytypeinfo-method"></a>CBasePin. DisplayTypeInfo, metodo

Il `DisplayTypeInfo` Metodo Visualizza le informazioni sul tipo di supporto durante il debug.

## <a name="syntax"></a>Sintassi


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin* 
</dt> <dd>

Ignorato.

</dd> <dt>

*PMT* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Nelle compilazioni di debug questo metodo chiama la funzione [**DbgLog**](dbglog.md) per visualizzare il tipo di supporto specificato. Nelle compilazioni finali, questo metodo non esegue alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




