---
description: Il metodo Copy copia un esempio di supporto.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: Metodo CTransInPlaceFilter.Copy (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10a7a2927789ffe49d37912862580222f0ed06d9648b6312cbb044e357d6e61c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053521"
---
# <a name="ctransinplacefiltercopy-method"></a>Metodo CTransInPlaceFilter.Copy

Il `Copy` metodo copia un campione di supporti.

## <a name="syntax"></a>Sintassi


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSource* 
</dt> <dd>

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore **all'interfaccia IMediaSample** nel nuovo esempio.

## <a name="remarks"></a>Commenti

Questo metodo recupera un buffer vuoto dall'allocatore downstream. Copia tutte le proprietà di esempio da *pSource* nel nuovo esempio, insieme ai dati effettivi nell'esempio. Se il filtro usa due allocatori, chiama questo metodo per copiare i dati tra buffer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




