---
description: 'Metodo CBaseOutputPin.EndOfStream: il metodo EndOfStream notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il metodo IPin::EndOfStream.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Metodo CBaseOutputPin.EndOfStream (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5f293b8026456618ad1196c491bce58cf481f07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096149"
---
# <a name="cbaseoutputpinendofstream-method"></a>Metodo CBaseOutputPin.EndOfStream

Il `EndOfStream` metodo notifica al pin che non sono previsti dati aggiuntivi. Questo metodo implementa il [**metodo IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndOfStream();
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
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




