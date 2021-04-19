---
description: 'Il metodo QueryFilterInfo recupera le informazioni sul filtro. Questo metodo implementa il metodo IBaseFilter:: QueryFilterInfo.'
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Metodo CBaseFilter. QueryFilterInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333492"
---
# <a name="cbasefilterqueryfilterinfo-method"></a>CBaseFilter. QueryFilterInfo, metodo

Il `QueryFilterInfo` metodo recupera le informazioni sul filtro. Questo metodo implementa il metodo [**IBaseFilter:: QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* 
</dt> <dd>

Puntatore a una struttura di [**\_ informazioni sul filtro**](/windows/win32/api/strmif/ns-strmif-filter_info) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un \_ puntatore S OK o e \_ .

## <a name="remarks"></a>Commenti

Questo metodo copia il nome del filtro dalla variabile membro [**CBaseFilter:: m \_ pname**](cbasefilter-m-pname.md) nel membro **achName** della struttura delle informazioni sul filtro \_ . Se **m \_ pname** è **null**, il metodo imposta **achName** su L' \\ 0'.

Il metodo imposta il membro **pGraph** della struttura di \_ informazioni sul filtro uguale alla variabile membro [**\_ pGraph di CBaseFilter:: m**](cbasefilter-m-pgraph.md) e incrementa il conteggio dei riferimenti. Il chiamante deve rilasciare l'interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




