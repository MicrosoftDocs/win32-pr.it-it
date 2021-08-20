---
description: Il metodo SetMediaType viene chiamato quando il tipo di supporto è impostato su uno dei pin del filtro.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Metodo CTransformFilter.SetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc9331a532f6748de4e03c6972fdd555e4d5e11516d946bbd131da9acab364c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584941"
---
# <a name="ctransformfiltersetmediatype-method"></a>Metodo CTransformFilter.SetMediaType

Il metodo viene chiamato quando il tipo di supporto è impostato su uno dei pin `SetMediaType` del filtro.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*direction* 
</dt> <dd>

Membro del [**tipo enumerato PIN \_ DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) che specifica un segnaposto per il filtro (input o output).

</dd> <dt>

*Pmt* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che specifica il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

I [**metodi CTransformInputPin::SetMediaType**](ctransforminputpin-setmediatype.md) e [**CTransformOutputPin::SetMediaType**](ctransformoutputpin-setmediatype.md) chiamano questo metodo quando viene impostato il tipo di supporto di un pin. Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




