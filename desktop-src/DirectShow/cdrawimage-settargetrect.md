---
description: Il metodo SetTargetRect imposta il rettangolo di destinazione.
ms.assetid: 033f8bae-e63d-4be0-8dd0-715cc1229392
title: Metodo CDrawImage. SetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4513b6aeda16d19476769290a6139f91b2fd1f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327206"
---
# <a name="cdrawimagesettargetrect-method"></a>CDrawImage. SetTargetRect, metodo

Il `SetTargetRect` metodo imposta il rettangolo di destinazione.

## <a name="syntax"></a>Sintassi


```C++
void SetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Puntatore a una struttura **Rect** che definisce il nuovo rettangolo di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il filtro proprietario deve chiamare questo metodo se il rettangolo di origine viene modificato; ad esempio, in risposta a una chiamata [**IBasicVideo:: SetDestinationPosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setdestinationposition) .

Prima di chiamare questo metodo, convalidare il rettangolo specificato in *pTargetRect*, relativo alla finestra del video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




