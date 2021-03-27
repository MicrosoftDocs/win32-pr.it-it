---
title: atan2 (Corecrt \_ Math. h)
description: Restituisce l'arcotangente di due valori (x, y).
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- HLSL atan2
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fbc6574d0fc0d53a165ae7da87c2627a295be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235008"
---
# <a name="atan2"></a>atan2

Restituisce l'arcotangente di due valori (x, y).



| atan2 *ret* (*y*, *x*) |
|-----------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                    |
|--------------------------------------------------------|--------------------------------|
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[nel \] valore y.<br/> |
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nel \] valore x.<br/> |



 

## <a name="return-value"></a>Valore restituito

Arcotangente di (y, x).

## <a name="remarks"></a>Commenti

I segni dei parametri *x* e *y* vengono utilizzati per determinare il quadrante dei valori restituiti nell'intervallo compreso tra-π e π. La funzione intrinseca HLSL **Atan2** è ben definita per ogni punto diverso dall'origine, anche se *y* è uguale a 0 e *x* non è uguale a 0.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *x* |
| *x*   | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *RET* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *x* |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati | sì       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

