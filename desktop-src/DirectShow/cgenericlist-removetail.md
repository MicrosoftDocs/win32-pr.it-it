---
description: Il metodo RemoveTail rimuove l'ultimo elemento nell'elenco.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Metodo CGenericList.RemoveTail (Wxlist.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed0b39d72eac68310dacdf2bfdc1d3c28bb35695b3d77230ba37f6fe81c417ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656156"
---
# <a name="cgenericlistremovetail-method"></a>Metodo CGenericList.RemoveTail

Il `RemoveTail` metodo rimuove l'ultimo elemento nell'elenco.

## <a name="syntax"></a>Sintassi


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a un oggetto di tipo **OBJECT** (tipo di modello) o **NULL** se l'elenco è vuoto.

## <a name="remarks"></a>Commenti

Questo metodo elimina il nodo elenco, ma non l'elemento contenuto nel nodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxlist.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CGenericList**](cgenericlist.md)
</dt> </dl>

 

 




