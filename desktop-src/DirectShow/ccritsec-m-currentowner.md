---
description: Identificatore del thread proprietario.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Membro CCritSec:: m_currentOwner (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332585"
---
# <a name="ccritsecm_currentowner-member"></a>Membro currentOwner di CCritSec:: m \_

Identificatore del thread proprietario.

## <a name="syntax"></a>Sintassi


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a>Osservazioni

Questa variabile membro viene definita solo nella versione di debug della classe di base. Il membro viene usato dalle [funzioni di debug della sezione critica](critical-section-debugging-functions.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

 




