---
description: Il metodo SetSourceRect imposta il rettangolo di origine.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Metodo CDrawImage. SetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325194"
---
# <a name="cdrawimagesetsourcerect-method"></a>CDrawImage. SetSourceRect, metodo

Il `SetSourceRect` metodo imposta il rettangolo di origine.

## <a name="syntax"></a>Sintassi


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Puntatore a una struttura **Rect** che definisce il nuovo rettangolo di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il filtro proprietario deve chiamare questo metodo se il rettangolo di origine viene modificato; ad esempio, in risposta a una chiamata [**IBasicVideo:: SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) .

Verificare il rettangolo specificato in *pSourceRect* prima di chiamare questo metodo, per assicurarsi che non si estenda oltre le dimensioni del video nativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




