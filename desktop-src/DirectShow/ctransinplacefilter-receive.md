---
description: Il metodo Receive riceve un campione di supporti, lo elabora e lo recapita al filtro downstream.
ms.assetid: 87126353-b73a-45f5-a8e7-b719efdf9d76
title: Metodo CTransInPlaceFilter.Receive (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 390d0243631e4ac31da779ca01197500f1d3df18127a3b86f0cf1ea834283f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053461"
---
# <a name="ctransinplacefilterreceive-method"></a>Metodo CTransInPlaceFilter.Receive

Il `Receive` metodo riceve un campione di supporti, lo elabora e lo recapita al filtro downstream.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSample* 
</dt> <dd>

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) nell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                 |
|----------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione riuscita<br/>          |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl> | Errore imprevisto<br/> |



 

## <a name="remarks"></a>Commenti

Il pin di input del filtro chiama questo metodo quando riceve un esempio. Il filtro chiama il [**metodo Transform,**](ctransinplacefilter-transform.md) che deve essere implementato dalla classe derivata. Il **metodo Transform** elabora i dati. Se il filtro usa un solo allocatore, passa *pSample* direttamente al **metodo Transform.** In caso contrario, copia *pSample e* passa la copia.

Se il **metodo Transform** restituisce S \_ FALSE, il metodo elimina `Receive` l'esempio. Nel primo esempio eliminato, il filtro invia un evento [**EC \_ QUALITY \_ CHANGE**](ec-quality-change.md) al gestore del grafico dei filtri. In caso contrario, se **il metodo Transform** restituisce S \_ OK, il filtro restituisce l'esempio di output. A tale scopo, chiama il [**metodo IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input downstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




