---
description: Puntatore a un oggetto sezione critica.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'Membro CSourceSeeking:: m_pLock (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329488"
---
# <a name="csourceseekingm_plock-member"></a>Membro pLock di CSourceSeeking:: m \_

Puntatore a un oggetto sezione critica. La `CSourceSeeking` classe usa questa sezione critica per sincronizzare l'accesso all'ora di inizio e di fine, alla durata e alle variabili di frequenza. Questa variabile viene inizializzata nel metodo del costruttore. vedere [**CSourceSeeking:: CSourceSeeking**](csourceseeking-csourceseeking.md).

## <a name="syntax"></a>Sintassi


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




