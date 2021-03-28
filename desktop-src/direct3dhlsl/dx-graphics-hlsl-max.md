---
title: max
description: Seleziona maggiore di x e y.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- numero massimo di HLSL
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a40ccb32bb2c2fcd7ca7342b9d7d4d143688102
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399464"
---
# <a name="max"></a>max

Seleziona maggiore di x e y.



| RET Max (x, y) |
|---------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nel \] valore di input x.<br/> |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[nel \] valore di input y.<br/> |



 

## <a name="return-value"></a>Valore restituito

Il parametro *x* o *y* , a seconda del valore più grande.


## <a name="remarks"></a>Commenti

I denormalizzati vengono gestiti come indicato di seguito:

| src1 src0-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | src1          | +inf | -inf |
| F           | src0 | src0 o src1  | +inf | src0 |
| +inf        | +inf | +inf          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F indica un numero reale finito.


## <a name="type-description"></a>Descrizione del tipo

| Nome | Ingresso/Uscita      | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Dimensione                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in ingresso          | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| y    | in ingresso          | uguale all'input x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | le stesse dimensioni di input x |
| RET  | tipo restituito | uguale all'input x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | le stesse dimensioni di input x |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati | sì                         |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Sì (vs \_ 1 \_ e PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**Specifica funzionale DirectX**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
