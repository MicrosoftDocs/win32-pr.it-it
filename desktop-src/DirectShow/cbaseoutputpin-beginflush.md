---
description: "Il Metodo BeginFlush avvia un'operazione di svuotamento. Implementa il metodo IPin:: BeginFlush."
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Metodo CBaseOutputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0216f74094d0c024d9b354dc594ff8d65315efbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329555"
---
# <a name="cbaseoutputpinbeginflush-method"></a>CBaseOutputPin. BeginFlush, metodo

Il `BeginFlush` metodo inizia un'operazione di svuotamento. Implementa il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce E \_ imprevisto.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato solo sui pin di input, pertanto l'implementazione di **CBaseOutputPin** restituisce E \_ imprevisto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




