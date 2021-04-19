---
description: Chiamato da un qualsiasi hit shader per rifiutare l'hit e terminare lo shader.
ms.assetid: ''
title: IgnoreHit (funzione)
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnoreHit
api_type:
- NA
ms.openlocfilehash: 66d450ce5a03e07e779ca5131443cdf67398cf19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305194"
---
# <a name="ignorehit-function"></a>IgnoreHit (funzione)

Chiamato da un [qualsiasi hit shader](any-hit-shader.md) per rifiutare l'hit e terminare lo shader. La ricerca di hit prosegue senza eseguire il commit della distanza e degli attributi per l'hit corrente.  La chiamata [**ReportHit**](reporthit-function.md) nell' [intersezione shader](intersection-shader.md), se presente, restituirà false.  Tutte le modifiche apportate al payload del raggio fino a questo punto in qualsiasi hit shader vengono mantenute.

## <a name="syntax"></a>Sintassi

```
void IgnoreHit();

```


## <a name="return-value"></a>Valore restituito

**void**

## <a name="remarks"></a>Commenti

Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Qualsiasi hit shader**](any-hit-shader.md)




## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




