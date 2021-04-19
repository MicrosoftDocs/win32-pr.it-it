---
description: Puntatore a una \_ struttura di filtro AMOVIESETUP.
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: 'Membro CFactoryTemplate:: m_pAMovieSetup_Filter (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAMovieSetup_Filter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 087612acf99a41966ccd98d3b41d2b83255a86f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329816"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a>\_Membro del filtro pAMovieSetup di CFactoryTemplate:: m \_

Puntatore a una struttura di [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .

## <a name="syntax"></a>Sintassi


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a>Osservazioni

Usare questa struttura per applicare un filtro a una registrazione automatica. Se il componente non è un filtro, questa variabile membro può essere **null**. Per altre informazioni, vedere How to register DirectShow Filters.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




