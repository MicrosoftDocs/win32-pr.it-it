---
description: Restituisce il valore passato come parametro HitKind a ReportHit.
ms.assetid: ''
title: HitKind
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HitKind
api_type:
- NA
ms.openlocfilehash: 81638996dbf69097154a2f1c235f6ab26c28dc8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304999"
---
# <a name="hitkind"></a>HitKind

Restituisce il valore passato come parametro **HitKind** a [**ReportHit**](reporthit-function.md).

## <a name="syntax"></a>Sintassi

```
uint HitKind();

```



## <a name="remarks"></a>Osservazioni

Se l'intersezione è stata segnalata dall'intersezione di un triangolo a funzione fissa, **HitKind** sarà uno dei front-end del **\_ triangolo di tipo \_ \_ \_ hit** (254) o il retro del **triangolo di \_ tipo \_ \_ \_ hit** (255).

Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Intersezione shader**](intersection-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




