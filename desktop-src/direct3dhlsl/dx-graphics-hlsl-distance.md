---
title: distance
description: Restituisce un valore scalare distanza tra due vettori.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- distanza HLSL
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338078"
---
# <a name="distance"></a>distance

Restituisce un valore scalare distanza tra due vettori.



| distanza *ret* (*x*, *y*) |
|--------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nel \] primo vettore a virgola mobile da confrontare.<br/>  |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[nel \] secondo vettore a virgola mobile da confrontare.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore scalare A virgola mobile che rappresenta la distanza tra il parametro *x* e il parametro *y* .

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *x* |
| *RET* | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati | sì       |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

