---
description: Imposta la parte FOURCC dell'oggetto FOURCCMap.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'Metodo FOURCCMap:: SetFOURCC (fourcc. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329956"
---
# <a name="fourccmapsetfourcc-method"></a>Metodo FOURCCMap:: SetFOURCC

Imposta la parte **fourcc** dell'oggetto [**FOURCCMap**](fourccmap.md) .

## <a name="syntax"></a>Sintassi


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pguid* 
</dt> <dd>

Puntatore alla parte dell'identificatore univoco globale (**GUID**) restituita dell'oggetto **FOURCCMap** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>FourCC. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe FOURCCMap**](fourccmap.md)
</dt> </dl>

 

 




