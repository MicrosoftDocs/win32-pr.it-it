---
description: Usato in un qualsiasi hit shader per confermare l'hit corrente e quindi arrestare la ricerca di altri riscontri per il raggio.
ms.assetid: ''
title: AcceptHitAndEndSearch (funzione)
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- AcceptHitAndEndSearch
api_type:
- NA
ms.openlocfilehash: 25bbac15a26beb535a91155cdd4c411c3c669e0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304925"
---
# <a name="accepthitandendsearch-function"></a>AcceptHitAndEndSearch (funzione)

Usato in un [qualsiasi hit shader](any-hit-shader.md) per confermare l'hit corrente e quindi arrestare la ricerca di altri riscontri per il raggio. Se è in esecuzione un'intersezione dello shader, l'esecuzione viene arrestata.  L'esecuzione passa all' [hit shader più vicino](closest-hit-shader.md), se abilitato, con il riscontro più vicino registrato fino a questo punto.

## <a name="syntax"></a>Sintassi

```
void AcceptHitAndEndSearch();
```




## <a name="return-value"></a>Valore restituito

**void**

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Richiamabile shader**](callable-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Lo shader manca**](miss-shader.md)
* [**Shader di generazione del Ray**](ray-generation-shader.md)



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




