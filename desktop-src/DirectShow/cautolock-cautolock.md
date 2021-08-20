---
description: Metodo del costruttore. Il costruttore blocca l'oggetto sezione critica specificato.
ms.assetid: 5a0d74f9-bb99-4922-9a92-2e7c1863421f
title: Costruttore CAutoLock.CAutoLock (Wxutil.h)
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
ms.openlocfilehash: 11267b444df319e339bcf13b30f200868a0f62d67712ed147513c2f8bc7d000c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017569"
---
# <a name="cautolockcautolock-constructor"></a>Costruttore CAutoLock.CAutoLock

Metodo del costruttore. Il costruttore blocca l'oggetto sezione critica specificato.

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

Puntatore a [**un oggetto CCritSec,**](ccritsec.md) che contiene un oggetto sezione critica.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CAutoLock**](cautolock.md)
</dt> </dl>

 

 




