---
description: Il metodo Clone crea una copia dell'enumeratore con lo stesso stato di enumerazione. Questo metodo implementa il metodo IEnumPins::Clone.
ms.assetid: 6e44c970-b90a-4bdb-8c60-dd8f31516249
title: Metodo CEnumPins.Clone (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Clone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a0d14f0caf30f6037d53639ff54d2e21d6d0fb0eee5cfa493aba248e84d48e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688611"
---
# <a name="cenumpinsclone-method"></a>Metodo CEnumPins.Clone

Il `Clone` metodo crea una copia dell'enumeratore con lo stesso stato di enumerazione. Questo metodo implementa il [**metodo IEnumPins::Clone.**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-clone)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clone(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnum* 
</dt> <dd>

Indirizzo di una variabile che riceve un [**puntatore all'interfaccia IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) del nuovo enumeratore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Operazione completata.<br/>                                                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>              | Memoria insufficiente.<br/>                                                        |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>                  | Argomento del puntatore **NULL.**<br/>                                                  |
| <dl> <dt>**ENUMERAZIONE VFW \_ \_ NON \_ \_ \_ SINCRONIZZATA**</dt> </dl> | Lo stato del filtro è stato modificato ed è ora incoerente con l'enumeratore.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




