---
description: Il \_ metodo Get DevSyncOffset recupera la deviazione standard del tempo in millisecondi tra il momento in cui ogni frame era dovuto e il rendering effettivamente eseguito, per tutti i frame dall'avvio dello streaming.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: Metodo CBaseVideoRenderer.get_DevSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326424"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a>Metodo CBaseVideoRenderer. Get \_ DevSyncOffset

Il `get_DevSyncOffset` metodo recupera la deviazione standard dell'intervallo di tempo in millisecondi tra il momento in cui ogni frame è dovuto e il momento in cui è stato eseguito il rendering, per tutti i frame dall'avvio del flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*piDev* 
</dt> <dd>

Puntatore alla deviazione standard dell'ora descritta in precedenza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IQualProp:: Get \_ DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




