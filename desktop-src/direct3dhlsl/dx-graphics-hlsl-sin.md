---
title: sin
description: Restituisce il seno del valore specificato.
ms.assetid: e1c3ead8-73dd-4798-8553-1a42dbaefe8e
keywords:
- sin HLSL
topic_type:
- apiref
api_name:
- sin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67c07adcbdfdfc0f2021355cf0a1e43b32ff23d5d3cb1343e189f328229a2efd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950291"
---
# <a name="sin"></a>sin

Restituisce il seno del valore specificato.



| *ret* sin(*x*) |
|----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Valore specificato, espresso in radianti.<br/> |



 

## <a name="return-value"></a>Valore restituito

Seno del *parametro x.*

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                 |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | sì (solo \_ vs 1 \_ 1) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

