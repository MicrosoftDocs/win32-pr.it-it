---
description: Chiamato da un'intersezione shader per segnalare un'intersezione del raggio.
ms.assetid: ''
title: ReportHit (funzione)
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305193"
---
# <a name="reporthit-function"></a>ReportHit (funzione)

Chiamato da un'intersezione [shader](intersection-shader.md) per segnalare un'intersezione del raggio.

## <a name="syntax"></a>Sintassi
Questa definizione di funzione intrinseca è equivalente al modello di funzione seguente:

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a>Parametri

`THit`

Valore float che specifica la distanza parametrica dell'intersezione.

`HitKind`

Unsigned Integer che identifica il tipo di hit che si è verificato.  Si tratta di un valore specificato dall'utente compreso nell'intervallo 0-127.  Il valore può essere letto da [tutti](any-hit-shader.md) gli hit shader hit o [Closer](closest-hit-shader.md) con la funzione intrinseca **HitKind** .

`Attributes`

Struttura della struttura dell' [**attributo di intersezione**](intersection-attributes.md) definita dall'utente che specifica gli attributi di intersezione.  

## <a name="return-value"></a>Valore restituito

**bool** True se il hit è stato accettato.  Un hit viene rifiutato se l'oggetto *SETI* non è compreso nell'intervallo corrente dei raggi o se qualsiasi hit shader chiama [**IgnoreHit**](ignorehit-function.md).  L'intervallo di raggi corrente è definito da **RayTMin** e **RayTCurrent**.

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Intersezione shader**](intersection-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




