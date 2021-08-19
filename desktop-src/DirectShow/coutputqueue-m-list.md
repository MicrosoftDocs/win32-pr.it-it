---
description: Coda di esempio multimediale.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: Membro COutputQueue::m_List (Outputq.h)
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
ms.openlocfilehash: 3e261116961f23c845ec2e27c6f20748b2c50cd9c036d9bc7d42bfe24b9b4fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087071"
---
# <a name="coutputqueuem_list-member"></a>Membro COutputQueue::m \_ List

Coda di esempio multimediale.

## <a name="syntax"></a>Sintassi


```C++
CSampleList *m_List;
```



## <a name="remarks"></a>Osservazioni

Questa variabile membro è un puntatore a un [**oggetto CGenericList**](cgenericlist.md) che contiene [**puntatori IMediaSample.**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Il **tipo CSampleList** viene definito come segue:

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




