---
description: Chiamato da uno shader di intersezione per segnalare un'intersezione di raggi.
ms.assetid: ''
title: Funzione ReportHit
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
ms.openlocfilehash: 8714cabc02f70ca12bcc78493de3a61482ba5aed5490087d309f6ec091cecf75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528109"
---
# <a name="reporthit-function"></a>Funzione ReportHit

Chiamato da uno [shader di intersezione per](intersection-shader.md) segnalare un'intersezione di raggi.

## <a name="syntax"></a>Sintassi
Questa definizione di funzione intrinseca equivale al modello di funzione seguente:

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a>Parametri

`THit`

Valore float che specifica la distanza parametrica dell'intersezione.

`HitKind`

Intero senza segno che identifica il tipo di hit che si è verificato.  Si tratta di un valore specificato dall'utente nell'intervallo da 0 a 127.  Il valore può essere letto da [qualsiasi hit](any-hit-shader.md) shader o [hit](closest-hit-shader.md) shader più vicino con la funzione **intrinseca HitKind.**

`Attributes`

Struttura dell'attributo di intersezione definito [**dall'utente che**](intersection-attributes.md) specifica gli attributi di intersezione.  

## <a name="return-value"></a>Valore restituito

**bool** True se l'hit è stato accettato.  Un hit viene rifiutato se *THit* non rientra nell'intervallo di raggi corrente o se qualsiasi hit shader [**chiama IgnoreHit.**](ignorehit-function.md)  L'intervallo di raggi corrente è definito **da RayTMin** e **RayTCurrent.**

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:

* [**Intersection Shader**](intersection-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su HLSL per Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




