---
description: 'Metodo CBasePin.Active: il metodo Active notifica al pin che il filtro è ora attivo.'
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Metodo CBasePin.Active (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1d651c58693789945af34d266aa8541679d1226d655530b90c542c8b0fc88b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872541"
---
# <a name="cbasepinactive-method"></a>Metodo CBasePin.Active

Il `Active` metodo notifica al pin che il filtro è ora attivo.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Quando il filtro passa da arrestato a sospeso, la [**classe CBaseFilter**](cbasefilter.md) chiama questo metodo su tutti i pin connessi del filtro.

Questo metodo non esegue alcuna operazione nella classe di base. Le classi derivate possono eseguire l'override di questo metodo. Ad esempio, un pin potrebbe eseguire il commit degli allocatori o ottenere risorse hardware.

Lo stato interno del gestore del grafico filtri non viene aggiornato fino a quando non viene restituita questa funzione membro, quindi non testare lo stato da questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




