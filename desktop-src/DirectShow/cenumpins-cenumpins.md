---
description: 'Costruttore CEnumPins.CEnumPins : metodo del costruttore.'
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Costruttore CEnumPins.CEnumPins (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1972533b86215e34563b9b1aa8f1b8ac3c14450b804fdae01ed7c7eafa78def4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131241"
---
# <a name="cenumpinscenumpins-constructor"></a>Costruttore CEnumPins.CEnumPins

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFilter* 
</dt> <dd>

Puntatore al filtro in base al quale enumerare i segnaposto.

</dd> <dt>

*pEnumPins* 
</dt> <dd>

Puntatore [**all'interfaccia IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) di un enumeratore da clonare oppure **NULL.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Se *pEnumPins* è **NULL,** questo metodo inizializza l'enumeratore all'inizio della sequenza di enumerazione. In caso contrario, duplica lo stato interno dell'enumeratore specificato da *pEnumPins.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




