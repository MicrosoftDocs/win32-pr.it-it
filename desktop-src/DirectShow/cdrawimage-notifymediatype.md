---
description: Il metodo NotifyMediaType invia una notifica all'oggetto CDrawImage del tipo di supporto corrente.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Metodo CDrawImage. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331920"
---
# <a name="cdrawimagenotifymediatype-method"></a>CDrawImage. NotifyMediaType, metodo

Il `NotifyMediaType` metodo notifica all'oggetto **CDrawImage** del tipo di supporto corrente.

## <a name="syntax"></a>Sintassi


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaType* 
</dt> <dd>

Puntatore a un oggetto [**CMediaType**](cmediatype.md) o **null** per cancellare il tipo di supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il filtro proprietario deve chiamare questo metodo ogni volta che viene modificato il tipo di supporto. Questa situazione si verifica in genere quando il pin si connette per la prima volta e dopo una modifica del formato dinamico.

L'oggetto **CDrawImage** archivia il puntatore *pMediaType* nella variabile **membro \_ pMediaType m** . Se pertanto il chiamante deve rilasciare l'oggetto **CMediaType** , deve aggiornare l'oggetto **CDrawImage** chiamando nuovamente questo metodo con un nuovo puntatore o con un valore **null** . In caso contrario, può verificarsi un errore quando l'oggetto **CDrawImage** tenta di fare riferimento al puntatore precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




