---
description: 'ObjectToWorld4x3: matrice per la trasformazione dallo spazio oggetto allo spazio globale.'
ms.assetid: ''
title: ObjectToWorld4x3
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObjectToWorld4x3
api_type:
- NA
ms.openlocfilehash: 22ad7bfafae89e33001d1d72878bc268ebfbd44649176b118a447fa16cf97d76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608271"
---
# <a name="objecttoworld4x3"></a>ObjectToWorld4x3

Matrice per la trasformazione da spazio oggetto a spazio del mondo. Lo spazio oggetto si riferisce allo spazio della struttura di accelerazione di livello inferiore corrente.

## <a name="syntax"></a>Sintassi

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a>Osservazioni

La matrice è una trasposizione della **matrice ObjectToWorld3x4.**

Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Hit Shader più vicino**](closest-hit-shader.md)
* [**Shader di intersezione**](intersection-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Direct3D 12 Raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




