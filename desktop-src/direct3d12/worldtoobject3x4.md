---
description: Matrice per la trasformazione da spazio globale a oggetto-spazio.
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
ms.openlocfilehash: 6274b1d4d18aff0464d933c20f7b8052f3389e5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305310"
---
# <a name="worldtoobject3x4"></a>WorldToObject3x4

Matrice per la trasformazione da spazio globale a oggetto-spazio. Oggetto-spazio si riferisce allo spazio della struttura di accelerazione di livello inferiore corrente.

## <a name="syntax"></a>Sintassi

```
void WorldToObject3x4();

```




## <a name="remarks"></a>Osservazioni

La matrice è una trasposizione della matrice **WorldToObject4x3** .

Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Intersezione shader**](intersection-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




