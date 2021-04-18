---
description: La \_ variabile membro bModifiesData m indica se il filtro modifica i dati di esempio ricevuti. Il valore viene impostato nel costruttore CTransInPlaceFilter, ma il valore predefinito è TRUE.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Membro CTransInPlaceFilter:: m_bModifiesData (Transip. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5bc0d630fd0eda6e9915f8c11f5b15d21b725ce8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328169"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a>Membro bModifiesData di CTransInPlaceFilter:: m \_

La `m_bModifiesData` variabile membro indica se il filtro modifica i dati di esempio ricevuti. Il valore viene impostato nel costruttore **CTransInPlaceFilter** , ma il valore predefinito è **true**.

## <a name="syntax"></a>Sintassi


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a>Osservazioni

Questa variabile influiscono sul modo in cui il filtro negozia l'allocatore. Se il valore è **true**, il filtro non può utilizzare un allocatore di sola lettura per entrambe le connessioni pin.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




