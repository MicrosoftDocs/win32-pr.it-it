---
title: fmod (Corecrt \_ math.h)
description: Restituisce il resto a virgola mobile di x/y.
ms.assetid: bb940548-c4c5-4109-a488-4ea7295c7213
keywords:
- fmod HLSL
topic_type:
- apiref
api_name:
- fmod
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e35f4de2c935f88c92aa1ebde2b4fcf9e8987c7f0824b38e260b727d9d34150
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789721"
---
# <a name="fmod"></a>fmod

Restituisce il resto a virgola mobile di x/y.



| *ret* fmod(*x*, *y*) |
|----------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                    |
|--------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Dividendo a virgola mobile.<br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Divisore a virgola mobile.<br/>  |



 

## <a name="return-value"></a>Valore restituito

Resto a virgola mobile del *parametro x* diviso per il *parametro y.*

## <a name="remarks"></a>Commenti

Il resto a virgola mobile viene calcolato in modo che x = i y + f, dove i è un numero intero, f ha lo stesso segno di x e il valore assoluto di f è minore del valore assoluto di \* y.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì       |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

