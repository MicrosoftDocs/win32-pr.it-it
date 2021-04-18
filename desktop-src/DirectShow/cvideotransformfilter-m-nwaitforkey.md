---
description: Numero massimo corrente di fotogrammi Delta da eliminare.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Membro CVideoTransformFilter:: m_nWaitForKey (Vtrans. h)'
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
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324418"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a>Membro nWaitForKey di CVideoTransformFilter:: m \_

Numero massimo corrente di fotogrammi Delta da eliminare. Sebbene la variabile sia maggiore di zero, il filtro ridurrà i frame fino a raggiungere un fotogramma chiave. Per ogni frame eliminato, il filtro decrementa la variabile di uno, impedendo al filtro di eliminare un numero eccessivo di fotogrammi. Dopo 30 frame Delta in una riga senza fotogrammi chiave, il filtro inizierà a recapito i frame.

## <a name="syntax"></a>Sintassi


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




