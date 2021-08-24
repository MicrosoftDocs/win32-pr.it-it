---
description: Il metodo SendAnyway fornisce tutti gli esempi in sospeso.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Metodo COutputQueue.SendAnyway (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4aed3cdd37c50f20b48922c8c711266a111680506813ab4572800abbca971343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831761"
---
# <a name="coutputqueuesendanyway-method"></a>Metodo COutputQueue.SendAnyway

Il `SendAnyway` metodo fornisce tutti gli esempi in sospeso.

## <a name="syntax"></a>Sintassi


```C++
void SendAnyway();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la variabile membro [**COutputQueue::m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) è **TRUE,** l'oggetto riempie la matrice [**COutputQueue::m \_ ppSamples**](coutputqueue-m-ppsamples.md) prima di distribuire un batch di campioni. Chiamare questo metodo per recapitare un batch parziale. Ad esempio, il [**metodo COutputQueue::EOS**](coutputqueue-eos.md) chiama `SendAnyway` per serializzare i messaggi di fine flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




