---
description: Il metodo AddPin aggiunge un nuovo pin di output al filtro.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: Metodo CSource.AddPin (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1c221d2fd032445587b52b0d0ae7f7744889254983fab82c7b282d06fee195e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953780"
---
# <a name="csourceaddpin-method"></a>Metodo CSource.AddPin

Il `AddPin` metodo aggiunge un nuovo pin di output al filtro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStream* 
</dt> <dd>

Puntatore [**all'oggetto CSourceStream**](csourcestream.md) che implementa il pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione riuscita<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente<br/> |



 

## <a name="remarks"></a>Commenti

Quando si crea un nuovo pin derivato da **CSourceStream,** il costruttore **CSourceStream** chiama automaticamente questo metodo per aggiungere il pin di output al filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Source.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSource**](csource.md)
</dt> </dl>

 

 




