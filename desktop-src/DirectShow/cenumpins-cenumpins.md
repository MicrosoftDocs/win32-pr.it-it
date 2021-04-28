---
description: 'Costruttore CEnumPins.CEnumPins : metodo costruttore.'
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
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099229"
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

Puntatore al filtro in base al quale enumerare i pin.

</dd> <dt>

*pEnumPins* 
</dt> <dd>

Puntatore [**all'interfaccia IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) di un enumeratore da clonare oppure **NULL.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Se *pEnumPins* è **NULL,** questo metodo inizializza l'enumeratore all'inizio della sequenza di enumerazione. In caso contrario, duplica lo stato interno dell'enumeratore specificato da *pEnumPins*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CEnumPins**](cenumpins.md)
</dt> </dl>

 

 




