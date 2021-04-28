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
ms.openlocfilehash: 947676c25bd5cac50749c737afd7e4ff75426c0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107739"
---
# <a name="objecttoworld3x4"></a>ObjectToWorld3x4

Matrice per la trasformazione da spazio oggetto a spazio del mondo. Lo spazio oggetto si riferisce allo spazio della struttura di accelerazione di livello inferiore corrente.

## <a name="syntax"></a>Sintassi

```
void ObjectToWorld3x4();

```




## <a name="remarks"></a>Osservazioni

La matrice è una trasposizione **della matrice ObjectToWorld4x3.**

Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Hit Shader più vicino**](closest-hit-shader.md)
* [**Shader di intersezione**](intersection-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Direct3D 12 Raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




