---
description: Metodo del costruttore.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Costruttore CEnumPins. CEnumPins (Amfilter. h)
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
ms.openlocfilehash: 536782de6992acfc1613d5866f13af658fba6e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329840"
---
# <a name="cenumpinscenumpins-constructor"></a>Costruttore CEnumPins. CEnumPins

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

Puntatore al filtro sul quale enumerare i pin.

</dd> <dt>

*pEnumPins* 
</dt> <dd>

Puntatore all'interfaccia [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) di un enumeratore da clonare o **null**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se *pEnumPins* è **null**, questo metodo inizializza l'enumeratore all'inizio della sequenza di enumerazione. In caso contrario, duplica lo stato interno dell'enumeratore specificato da *pEnumPins*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




