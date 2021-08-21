---
description: 'ObjectToWorld3x4: matrice per la trasformazione dallo spazio oggetti allo spazio globale.'
ms.assetid: ''
title: ObjectToWorld3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld3x4
api_type:
- NA
ms.openlocfilehash: d58737e50fb7d173c84c4b38f6b91b9b6bfbc9d3b5a88c498344dadd5e94e73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123750"
---
# <a name="objecttoworld3x4"></a>ObjectToWorld3x4

Matrice per la trasformazione dallo spazio oggetti allo spazio globale. Lo spazio oggetti si riferisce allo spazio della struttura di accelerazione di livello inferiore corrente.

## <a name="syntax"></a>Sintassi

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a>Osservazioni

La matrice è una trasposizione della **matrice ObjectToWorld4x3.**

Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Intersection Shader**](intersection-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su HLSL per Direct3D 12 Raytracing](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




