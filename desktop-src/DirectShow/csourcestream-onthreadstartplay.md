---
description: Il metodo OnThreadStartPlay viene chiamato all'inizio del metodo CSourceStream::D oBufferProcessingLoop.
ms.assetid: 16d3b28f-bfae-49af-b8e4-8cc8cb15ecab
title: Metodo CSourceStream. OnThreadStartPlay (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadStartPlay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857f27ad39fb9169e1ef67253d5232c7cbc3dbb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330035"
---
# <a name="csourcestreamonthreadstartplay-method"></a>CSourceStream. OnThreadStartPlay, metodo

Il `OnThreadStartPlay` metodo viene chiamato all'inizio del metodo [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT OnThreadStartPlay();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo non esegue alcuna operazione nella classe di base. è disponibile per la classe derivata di cui eseguire l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source. h (Includi Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceStream**](csourcestream.md)
</dt> </dl>

 

 




