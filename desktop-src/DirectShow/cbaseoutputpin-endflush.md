---
description: "Metodo CBaseOutputPin.EndFlush: il metodo EndFlush termina un'operazione di scaricamento. Questo metodo implementa il metodo IPin::EndFlush."
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: Metodo CBaseOutputPin.EndFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a85df585a570d7b35a0ac052c922b23dcb605cf4869b3a44cab880f9b6bef21d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910481"
---
# <a name="cbaseoutputpinendflush-method"></a>Metodo CBaseOutputPin.EndFlush

Il `EndFlush` metodo termina un'operazione di scaricamento. Questo metodo implementa il [**metodo IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce E \_ UNEXPECTED.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato solo sui pin di input, quindi l'implementazione **di CBaseOutputPin** restituisce E \_ UNEXPECTED.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




