---
description: Il metodo BeginFlush avvia un'operazione di scaricamento. Implementa il metodo IPin::BeginFlush.
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Metodo CBaseOutputPin.BeginFlush (Amfilter.h)
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
ms.openlocfilehash: 5dd12216fb040601d73eb566d47ec5c8c3ceeec685bd8f7abc6877756f94c6a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640011"
---
# <a name="cbaseoutputpinbeginflush-method"></a>Metodo CBaseOutputPin.BeginFlush

Il `BeginFlush` metodo avvia un'operazione di scaricamento. Implementa il [**metodo IPin::BeginFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce E \_ UNEXPECTED.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato solo sui pin di input, quindi **l'implementazione di CBaseOutputPin** restituisce E \_ UNEXPECTED.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




