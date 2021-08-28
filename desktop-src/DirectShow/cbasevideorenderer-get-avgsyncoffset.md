---
description: Il metodo get AvgSyncOffset recupera la media del tempo in millisecondi tra la scadenza di ogni frame e il momento in cui è stato effettivamente eseguito il rendering per tutti i fotogrammi dall'avvio \_ dello streaming.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: CBaseVideoRenderer.get_AvgSyncOffset metodo (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4550445d0a2596edcb9d76b88b371eb060257b29730a386c4f9444dae2624b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526501"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a>Metodo CBaseVideoRenderer.get \_ AvgSyncOffset

Il metodo recupera la media del tempo in millisecondi tra la scadenza di ogni frame e il momento in cui è stato effettivamente eseguito il rendering per tutti i fotogrammi dall'avvio `get_AvgSyncOffset` dello streaming.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*piAvg* 
</dt> <dd>

Puntatore alla media del tempo come descritto in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IQualProp::get \_ AvgSyncOffset.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




