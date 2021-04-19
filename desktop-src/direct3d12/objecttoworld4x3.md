---
description: Matrice per la trasformazione dallo spazio oggetto allo spazio globale.
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
ms.openlocfilehash: 613b4c403f235819845114e7019e07051a25ec80
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304704"
---
# <a name="objecttoworld4x3"></a>ObjectToWorld4x3

Matrice per la trasformazione dallo spazio oggetto allo spazio globale. Oggetto-spazio si riferisce allo spazio della struttura di accelerazione di livello inferiore corrente.

## <a name="syntax"></a>Sintassi

```
void ObjectToWorld4x3();

```




## <a name="remarks"></a>Osservazioni

La matrice è una trasposizione della matrice **ObjectToWorld3x4** .

Questa funzione può essere chiamata dai seguenti tipi di shader raytracing:

* [**Qualsiasi hit shader**](any-hit-shader.md)
* [**Hit shader più vicino**](closest-hit-shader.md)
* [**Intersezione shader**](intersection-shader.md)





## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Guida di riferimento a Direct3D 12 raytracing HLSL](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




