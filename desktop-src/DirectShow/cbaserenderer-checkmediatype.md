---
description: Il metodo CheckMediaType determina se il filtro accetta un tipo di supporto specifico.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Metodo CBaseRenderer.CheckMediaType (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8de57346138b4683f59cfa612f01fff1ef3d8fd9aceec9b34daee49bfa74ebbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157981"
---
# <a name="cbaserenderercheckmediatype-method"></a>Metodo CBaseRenderer.CheckMediaType

Il `CheckMediaType` metodo determina se il filtro accetta un tipo di supporto specifico.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntatore a un [**oggetto CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il tipo di supporto proposto è accettabile. In caso contrario, restituisce S \_ FALSE o un codice di errore.

## <a name="remarks"></a>Commenti

Il pin di input chiama questo metodo dal proprio [**metodo CBasePin::CheckMediaType.**](cbasepin-checkmediatype.md) La classe derivata deve implementare questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




