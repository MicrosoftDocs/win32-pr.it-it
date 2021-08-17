---
title: max
description: Seleziona i valori maggiori di x e y.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- max HLSL
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e81eca4f5cabea57f36aa66b722fedb3e1176c3c189db9cdcfd610e4e26047c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791472"
---
# <a name="max"></a>max

Seleziona i valori maggiori di x e y.



| ret max(x, y) |
|---------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Valore di input x.<br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Valore di input y.<br/> |



 

## <a name="return-value"></a>Valore restituito

Parametro *x* *o y,* a seconda del valore più grande.


## <a name="remarks"></a>Commenti

I denormali vengono gestiti come segue:

| src0 src1-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | src1          | +inf | -inf |
| F           | src0 | src0 o src1  | +inf | src0 |
| +inf        | +inf | +inf          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F indica un numero finito reale.


## <a name="type-description"></a>Descrizione del tipo

| Nome | Ingresso/Uscita      | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Dimensione                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in          | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| y    | in          | uguale all'input x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | stesse dimensioni dell'input x |
| Ret  | tipo restituito | uguale all'input x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | stesse dimensioni dell'input x |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                         |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | sì (vs \_ 1 \_ 1 e ps \_ 1 \_ 4) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**Specifica funzionale di DirectX**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
