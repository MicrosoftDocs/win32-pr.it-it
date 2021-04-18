---
description: Il metodo AddBefore inserisce un elenco prima della posizione specificata.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Metodo CBaseList. AddBefore (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3c25b2dd545b3e6698404bf00f82d1086bfb81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328681"
---
# <a name="cbaselistaddbefore-method"></a>CBaseList. AddBefore, metodo

Il `AddBefore` metodo inserisce un elenco prima della posizione specificata.

## <a name="syntax"></a>Sintassi


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pos* 
</dt> <dd>

Posizione prima della quale inserire l'elenco.

</dd> <dt>

*pList* 
</dt> <dd>

Puntatore all'elenco da inserire.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Gli indicatori di posizione esistenti, incluso quello specificato nel parametro *pos* , rimangono validi. Se il metodo ha esito negativo, è possibile che alcuni elementi siano stati aggiunti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




