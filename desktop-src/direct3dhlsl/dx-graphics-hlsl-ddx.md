---
title: Ddx
description: Restituisce la derivata parziale del valore specificato rispetto alla coordinata x dello spazio dello schermo.
ms.assetid: a21c2d2a-7c62-4dc6-8521-273690be1104
keywords:
- ddx HLSL
topic_type:
- apiref
api_name:
- ddx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60f2376af13e291ff0c59966bd50261cf2fd29ceb10d8ea26f621e257956ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043819"
---
# <a name="ddx"></a>Ddx

Restituisce la derivata parziale del valore specificato rispetto alla coordinata x dello spazio dello schermo.



| *ret* ddx(*x*) |
|----------------|



 

Questa funzione calcola la derivata parziale rispetto alla coordinata x dello spazio dello schermo. Per calcolare la derivata parziale rispetto alla coordinata y dello spazio dello schermo, usare la [**funzione ddy.**](dx-graphics-hlsl-ddy.md)

Questa funzione è supportata solo nei pixel shader.

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Il valore specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Derivazione parziale del *parametro x.*

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                | Supportato                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| [Modelli shader modello 5](d3d11-graphics-reference-sm5.md) e versioni successive | sì                                       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                                  | sì                                       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)                   | sì                                       |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                   | sì in ps \_ 2 \_ x; non supportato in ps \_ 2 \_ 0. |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                   | no                                        |



 

Questa funzione è supportata nei tipi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

