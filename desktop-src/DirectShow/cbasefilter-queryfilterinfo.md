---
description: Il metodo QueryFilterInfo recupera informazioni sul filtro. Questo metodo implementa il metodo IBaseFilter::QueryFilterInfo.
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: Metodo CBaseFilter.QueryFilterInfo (Amfilter.h)
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
ms.openlocfilehash: 31eb135a29a6e8e1c4f27c28d24b5cbf50eba3bb87b99ba9a1d3a5868c2fbc49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341741"
---
# <a name="cbasefilterqueryfilterinfo-method"></a>Metodo CBaseFilter.QueryFilterInfo

Il `QueryFilterInfo` metodo recupera informazioni sul filtro. Questo metodo implementa il [**metodo IBaseFilter::QueryFilterInfo.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo)

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

Puntatore a una [**struttura FILTER \_ INFO.**](/windows/win32/api/strmif/ns-strmif-filter_info)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o E \_ POINTER.

## <a name="remarks"></a>Commenti

Questo metodo copia il nome del filtro dalla variabile membro [**CBaseFilter::m \_ pName**](cbasefilter-m-pname.md) nel membro **achName** della struttura FILTER \_ INFO. Se **m \_ pName** è **NULL,** il metodo imposta **achName** su L' \\ 0'.

Il metodo imposta il **membro pGraph** della struttura FILTER INFO uguale alla variabile membro \_ [**CBaseFilter::m \_ pGraph**](cbasefilter-m-pgraph.md) e incrementa il conteggio dei riferimenti. Il chiamante deve rilasciare l'interfaccia .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




