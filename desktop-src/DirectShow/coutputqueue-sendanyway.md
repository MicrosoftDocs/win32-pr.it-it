---
description: Il metodo SendAnyway recapita tutti gli esempi in sospeso.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Metodo COutputQueue. SendAnyway (Outputq. h)
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
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324671"
---
# <a name="coutputqueuesendanyway-method"></a>COutputQueue. SendAnyway, metodo

Il `SendAnyway` Metodo recapita tutti gli esempi in sospeso.

## <a name="syntax"></a>Sintassi


```C++
void SendAnyway();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se la variabile membro [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) è **true**, l'oggetto riempie la matrice [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) prima di recapitare un batch di campioni. Chiamare questo metodo per recapitare un batch parziale. Ad esempio, il metodo [**COutputQueue:: EOS**](coutputqueue-eos.md) chiama `SendAnyway` per serializzare i messaggi di fine flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Outputq. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




