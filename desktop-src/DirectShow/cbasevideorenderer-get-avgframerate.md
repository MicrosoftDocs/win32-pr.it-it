---
description: Il \_ metodo Get AvgFrameRate calcola e recupera la frequenza dei fotogrammi media conseguita.
ms.assetid: f36fc020-8c1a-491f-9f55-18265fde8bf8
title: Metodo CBaseVideoRenderer.get_AvgFrameRate (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgFrameRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d8fff53f3d56676805eca9029670d51210ef2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331522"
---
# <a name="cbasevideorendererget_avgframerate-method"></a>Metodo CBaseVideoRenderer. Get \_ AvgFrameRate

Il `get_AvgFrameRate` metodo calcola e recupera la frequenza dei fotogrammi media conseguita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AvgFrameRate(
   int *piAvgFrameRate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*piAvgFrameRate* 
</dt> <dd>

Puntatore al numero di fotogrammi al secondo dall'inizio del flusso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IQualProp:: Get \_ AvgFrameRate**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgframerate) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




