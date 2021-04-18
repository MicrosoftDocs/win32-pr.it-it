---
description: Metodo del costruttore. Il costruttore blocca l'oggetto sezione critico specificato.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Costruttore CAutoLock. CAutoLock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock.CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fed29011d4fe581ed146f64800351a3f1053d957
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327977"
---
# <a name="cautolockcautolock-constructor"></a>Costruttore CAutoLock. CAutoLock

Metodo del costruttore. Il costruttore blocca l'oggetto sezione critico specificato.

## <a name="syntax"></a>Sintassi


```C++
CAutoLock(
   CCritSec *plock
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Plock* 
</dt> <dd>

Puntatore a un oggetto [**CCritSec**](ccritsec.md) che contiene un oggetto sezione critica.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAutoLock**](cautolock.md)
</dt> </dl>

 

 




