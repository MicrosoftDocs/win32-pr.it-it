---
description: Il metodo GetStdDev stima la deviazione standard in millisecondi tra il momento in cui ogni frame è dovuto e quando viene effettivamente eseguito il rendering, per le statistiche per fotogramma.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Metodo CBaseVideoRenderer. GetStdDev (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326413"
---
# <a name="cbasevideorenderergetstddev-method"></a>CBaseVideoRenderer. GetStdDev, metodo

Il `GetStdDev` Metodo stima la deviazione standard in millisecondi tra il momento in cui ogni frame è dovuto e quando viene effettivamente eseguito il rendering, per le statistiche per fotogramma.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nSamples* 
</dt> <dd>

Valore intero che contiene il numero di campioni video ricevuti dal renderer video.

</dd> <dt>

*piResult* 
</dt> <dd>

Puntatore a un valore integer che conterrà la deviazione standard.

</dd> <dt>

*llSumSq* 
</dt> <dd>

Valore che rappresenta la deviazione standard, in millisecondi, di tutti gli esempi video sottoposti a rendering. Più basso è il valore, più è coerente il rendering.

</dd> <dt>

*iTot* 
</dt> <dd>

Valore che rappresenta il valore medio, in millisecondi, tra l'ora timbrata e il tempo di rendering per tutti gli esempi video sottoposti a rendering.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce NOERROR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




