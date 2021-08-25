---
description: Il metodo DisplayTypeInfo visualizza informazioni sul tipo di supporto durante il debug.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Metodo CBasePin.DisplayTypeInfo (Amfilter.h)
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
ms.openlocfilehash: 10b4535950a46fa55aba0ea7d808a075186f074cc829be0d3225dc887512ad47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916451"
---
# <a name="cbasepindisplaytypeinfo-method"></a>Metodo CBasePin.DisplayTypeInfo

Il metodo `DisplayTypeInfo` visualizza informazioni sul tipo di supporto durante il debug.

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

*Pmt* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Nelle build di debug questo metodo chiama la [**funzione DbgLog**](dbglog.md) per visualizzare il tipo di supporto specificato. Nelle build di vendita al dettaglio, questo metodo non esegue alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




