---
description: Il metodo SetDrawContext imposta i contesti di dispositivo usati per il disegno.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Metodo CDrawImage. SetDrawContext (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326826"
---
# <a name="cdrawimagesetdrawcontext-method"></a>CDrawImage. SetDrawContext, metodo

Il `SetDrawContext` metodo imposta i contesti di dispositivo usati per il disegno.

## <a name="syntax"></a>Sintassi


```C++
void SetDrawContext();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo recupera i contesti di dispositivo della finestra e memoria dall'oggetto [**CBaseWindow**](cbasewindow.md) proprietario. Chiamare questo metodo dopo l'inizializzazione della finestra, ma prima di iniziare il disegno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




