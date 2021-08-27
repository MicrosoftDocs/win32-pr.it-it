---
description: Ora di arresto. Per impostazione predefinita, il valore è impostato su un numero molto grande. La classe derivata può reimpostare il valore nel costruttore o quando il filtro viene inizializzato.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: Membro CSourceSeeking::m_rtStop (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4408fddf42070012aa6e1eb3a0268e8e449b571828c0904524f3cc8d27df3bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103001"
---
# <a name="csourceseekingm_rtstop-member"></a>Membro CSourceSeeking::m \_ rtStop

Ora di arresto. Per impostazione predefinita, il valore è impostato su un numero molto grande. La classe derivata può reimpostare il valore nel costruttore o quando il filtro viene inizializzato.

## <a name="syntax"></a>Sintassi


```C++
CRefTime m_rtStop;
```



## <a name="remarks"></a>Osservazioni

Mantenere la **sezione \_ critica m pLock** prima di accedere a questa variabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




