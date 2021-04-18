---
description: Il metodo GetTargetRect Recupera il rettangolo di destinazione corrente.
ms.assetid: b6542b06-af36-4666-b6fa-d9fa3c6c7044
title: Metodo CDrawImage. GetTargetRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 547dd12117cec95ad1cb0159667a8dd72a95a6e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327208"
---
# <a name="cdrawimagegettargetrect-method"></a>CDrawImage. GetTargetRect, metodo

Il `GetTargetRect` metodo recupera il rettangolo di destinazione corrente.

## <a name="syntax"></a>Sintassi


```C++
void GetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTargetRect* 
</dt> <dd>

Puntatore a una struttura **Rect** che riceve il rettangolo di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




