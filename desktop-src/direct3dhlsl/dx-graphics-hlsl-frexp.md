---
title: frexp (Corecrt \_ Math. h)
description: Restituisce mantissa ed esponente del valore a virgola mobile specificato.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- HLSL frexp
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969348"
---
# <a name="frexp"></a>frexp

Restituisce mantissa ed esponente del valore a virgola mobile specificato.



| frexp *ret* (*x*, *Exp*) |
|-------------------------|



 

Il valore restituito è mantissa e il valore restituito dal parametro *Exp* è l'esponente.

## <a name="parameters"></a>Parametri



| Elemento                                                         | Descrizione                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/>       | \[nel \] valore a virgola mobile specificato. Se il parametro *x* è 0, questa funzione restituisce 0 sia per mantissa che per l'esponente.<br/> |
| <span id="exp"></span><span id="EXP"></span>*exp*<br/> | \[\]esponente restituito del parametro *x* .<br/>                                                                                   |



 

## <a name="return-value"></a>Valore restituito

Mantissa del parametro *x* .

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *exp* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *x* |
| *RET* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *x* |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelli shader più elevati | sì                 |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | Sì ( \_ solo PS 2 \_ x) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | no                  |



 

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

