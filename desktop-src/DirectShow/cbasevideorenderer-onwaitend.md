---
description: Il metodo OnWaitEnd viene chiamato al termine di un tempo di attesa.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Metodo CBaseVideoRenderer.OnWaitEnd (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b130bf38833951cad4f82fd559c0299d2aea86854ca0ab5545f3f2794ab9b4b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432471"
---
# <a name="cbasevideorendereronwaitend-method"></a>Metodo CBaseVideoRenderer.OnWaitEnd

Il metodo OnWaitEnd viene chiamato al termine di un tempo di attesa.

## <a name="syntax"></a>Sintassi


```C++
void OnWaitEnd();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro esegue solo la registrazione delle prestazioni. Viene chiamato quando il thread viene svegliato dall'attesa nella finestra o quando è necessario eseguire il rendering dell'esempio successivo. Potrebbe infine essere usato per raccogliere informazioni che controllano la sincronizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseVideoRenderer**](cbasevideorenderer.md)
</dt> </dl>

 

 




