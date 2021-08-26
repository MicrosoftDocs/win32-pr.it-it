---
description: Numero massimo corrente di fotogrammi differenziali da eliminare.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: Membro CVideoTransformFilter::m_nWaitForKey (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83cb78b233385e502d6508212492c54865aca28990ae079e4bf588776bd83fe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998541"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a>Membro CVideoTransformFilter::m \_ nWaitForKey

Numero massimo corrente di fotogrammi differenziali da eliminare. Anche se questa variabile è maggiore di zero, il filtro elimina i fotogrammi fino a raggiungere un fotogramma chiave. Per ogni frame eliminato, il filtro decrementa questa variabile di uno, impedendo al filtro di eliminare un numero eccessivo di frame. Dopo 30 fotogrammi differenziali in una riga senza fotogrammi chiave, il filtro inizierà a distribuire nuovamente i fotogrammi.

## <a name="syntax"></a>Sintassi


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




