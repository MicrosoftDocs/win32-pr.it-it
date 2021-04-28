---
description: 'Costruttore CBaseList.CBaseList : metodo costruttore.'
ms.assetid: 2982f53a-c222-4a9d-812a-42897ca4cb5c
title: Costruttore CBaseList.CBaseList (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66aad24fe2d5176c684d4d78be27833e3be2f909
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096328"
---
# <a name="cbaselistcbaselist-constructor"></a>Costruttore CBaseList.CBaseList

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CBaseList(
   TCHAR *pName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore al nome dell'elenco.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per migliorare l'efficienza, `CBaseList` la classe gestisce una cache di nodi elenco. Questa versione del costruttore usa una dimensione della cache predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (include Streams.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseList**](cbaselist.md)
</dt> </dl>

 

 




