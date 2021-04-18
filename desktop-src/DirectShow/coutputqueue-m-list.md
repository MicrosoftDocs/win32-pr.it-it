---
description: Coda di esempio multimediale.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'Membro COutputQueue:: m_List (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328254"
---
# <a name="coutputqueuem_list-member"></a>Membro elenco COutputQueue:: m \_

Coda di esempio multimediale.

## <a name="syntax"></a>Sintassi


```C++
CSampleList *m_List;
```



## <a name="remarks"></a>Osservazioni

Questa variabile membro è un puntatore a un oggetto [**CGenericList**](cgenericlist.md) che include puntatori [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Il tipo **CSampleList** è definito come segue:

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




