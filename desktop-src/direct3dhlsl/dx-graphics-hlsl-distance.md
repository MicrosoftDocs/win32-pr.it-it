---
title: distance
description: Restituisce una distanza scalare tra due vettori.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- distance HLSL
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f51c5e9865b9dfc1c5a941beb43010dc8fad64e2d8ac8763998c22cb3e0dfbd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726541"
---
# <a name="distance"></a>distance

Restituisce una distanza scalare tra due vettori.



| *ret* distance(*x*, *y*) |
|--------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Primo vettore a virgola mobile da confrontare.<br/>  |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Secondo vettore a virgola mobile da confrontare.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore scalare a virgola mobile che rappresenta la distanza tra il *parametro x* e il *parametro y.*

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |
| *Ret* | [**Scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì       |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

