---
description: "Il metodo QueryInternalConnections recupera i pin connessi internamente a questo pin (all'interno del filtro). Questo metodo implementa il metodo IPin:: QueryInternalConnections."
ms.assetid: 08344fc5-38b2-4dbe-8ef9-30d2fcd64187
title: Metodo CBasePin. QueryInternalConnections (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryInternalConnections
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99a636295fc87347a1735ab028b6de342e887d55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328261"
---
# <a name="cbasepinqueryinternalconnections-method"></a>CBasePin. QueryInternalConnections, metodo

Il `QueryInternalConnections` metodo recupera i pin connessi internamente a questo pin (all'interno del filtro). Questo metodo implementa il metodo [**Ipin:: QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryInternalConnections(
   IPin  *apPin,
   ULONG *nPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*apPin* 
</dt> <dd>

Indirizzo di una matrice di puntatori [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .

</dd> <dt>

*nPin* 
</dt> <dd>

In input, specifica la dimensione della matrice. Quando il metodo restituisce, il valore viene impostato sul numero di puntatori restituiti nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                         |
|-------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Dimensioni della matrice insufficienti.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>      | Esito positivo.<br/>                 |
| <dl> <dt>**E \_ non riescono**</dt> </dl>    | Esito negativo.<br/>                 |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Non implementato.<br/>         |



 

## <a name="remarks"></a>Commenti

In alcuni filtri i pin di input corrispondono a specifici pin di output. Per ogni pin, questo metodo riempie una matrice con puntatori ai pin corrispondenti. Se ogni pin di input fornisce dati per ogni pin di output, restituire E \_ NOTIMPL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




