---
title: sqrt
description: Restituisce la radice quadrata del valore a virgola mobile specificato, per componente.
ms.assetid: e8debc60-1441-4974-9ab3-6d1c2217caaf
keywords:
- Sqrt HLSL
topic_type:
- apiref
api_name:
- sqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6550906c50c44dba5ab28b6327c86a6bb94560e7ad3d9921b6e9d37eb35236de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725841"
---
# <a name="sqrt"></a>sqrt

Restituisce la radice quadrata del valore a virgola mobile specificato, per componente.



| *ret* sqrt(*x*) |
|-----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Valore a virgola mobile specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Radice quadrata del *parametro x,* per componente.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                 |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sì (solo vs \_ \_ 1 1) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

