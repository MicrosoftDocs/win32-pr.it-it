---
title: ddy
description: Restituisce la derivazione parziale del valore specificato rispetto alla coordinata y dello spazio dello schermo.
ms.assetid: 1c88804f-a13f-4714-a3ef-466307afbc1b
keywords:
- HLSL ddy
topic_type:
- apiref
api_name:
- ddy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d27e48a6d9ae237e4e58d1fd30afbac3b2b40d3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399216"
---
# <a name="ddy"></a>ddy

Restituisce la derivazione parziale del valore specificato rispetto alla coordinata y dello spazio dello schermo.



| ddy *ret* (*x*) |
|----------------|



 

Questa funzione calcola la derivazione parziale per quanto riguarda la coordinata y dello spazio dello schermo. Per calcolare la derivazione parziale per quanto riguarda la coordinata x dello spazio dello schermo, utilizzare la funzione [**DDX**](dx-graphics-hlsl-ddx.md) .

Questa funzione è supportata solo in pixel shader.

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nel \] valore specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Derivato parziale del parametro *x* .

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *RET* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *x* |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e versioni successive shader Models | sì                                       |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                                  | sì                                       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)                   | sì                                       |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                   | Sì in PS \_ 2 \_ x; non supportato in PS \_ 2 \_ 0. |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                   | no                                        |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

