---
title: step
description: Confronta due valori, restituendo 0 o 1 in base al valore maggiore.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- passaggio HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c800e8d8c6f78386139f822f118163f3b431f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729527"
---
# <a name="step"></a>step

Confronta due valori, restituendo 0 o 1 in base al valore maggiore.



| passaggio *ret* (*y*, *x*) |
|----------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[nel \] primo valore a virgola mobile da confrontare.<br/>  |
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nel \] secondo valore a virgola mobile da confrontare.<br/> |



 

## <a name="return-value"></a>Valore restituito

1 se il parametro *x* è maggiore o uguale al parametro *y* ; in caso contrario, 0.

## <a name="remarks"></a>Commenti

Questa funzione utilizza la formula seguente: (*x*  >=  *y*)? 1:0. La funzione restituisce 0 o 1 a seconda che il parametro *x* sia maggiore o uguale al parametro *y* . Per calcolare un'interpolazione uniforme tra 0 e 1, usare la funzione intrinseca [**SmoothStep**](dx-graphics-hlsl-smoothstep.md) HLSL.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *x*   | uguale all'input *y*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *y* |
| *RET* | uguale all'input *y*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *y* |



 

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

 

