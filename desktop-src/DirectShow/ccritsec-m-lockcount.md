---
description: Numero di blocchi in attesa su questo oggetto.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'Membro CCritSec:: m_lockCount (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88098a8ded025a899e2092a96308bd6c54750758
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329861"
---
# <a name="ccritsecm_lockcount-member"></a>Membro lockCount di CCritSec:: m \_

Numero di blocchi in attesa su questo oggetto.

## <a name="syntax"></a>Sintassi


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a>Osservazioni

Questa variabile membro viene definita solo nella versione di debug della classe di base. Il membro viene usato dalle funzioni di [debug della sezione critica](critical-section-debugging-functions.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

 




