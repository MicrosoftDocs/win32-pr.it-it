---
description: 'WorldToObject3x4: matrice per la trasformazione dallo spazio globale allo spazio oggetto.'
ms.assetid: ''
title: WorldToObject3x4
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WorldToObject3x4
api_type:
- NA
ms.openlocfilehash: cc7bf7dc2f06102b9b23eafd45655f12816c8359
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105240"
---
# <a name="worldtoobject3x4"></a>WorldToObject3x4

Matrice per la trasformazione da spazio del mondo a spazio oggetto. Lo spazio oggetto si riferisce allo spazio della struttura di accelerazione di livello inferiore corrente.

## <a name="syntax"></a>Sintassi

```
void WorldToObject3x4();

```




## <a name="remarks"></a>Osservazioni

La matrice è una trasposizione **della matrice WorldToObject4x3.**

Questa funzione può essere chiamata dai tipi di shader raytracing seguenti:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Hit Shader più vicino**](closest-hit-shader.md)
* [**Shader di intersezione**](intersection-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Direct3D 12 Raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




