---
title: sqrt
description: Restituisce la radice quadrata del valore a virgola mobile specificato, per componente.
ms.assetid: e8debc60-1441-4974-9ab3-6d1c2217caaf
keywords:
- HLSL sqrt
topic_type:
- apiref
api_name:
- sqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff3c872dac6da28a1ec92993e387bd23daec7f86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399056"
---
# <a name="sqrt"></a>sqrt

Restituisce la radice quadrata del valore a virgola mobile specificato, per componente.



| sqrt *ret* (*x*) |
|-----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nel \] valore a virgola mobile specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Radice quadrata del parametro *x* , per componente.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *RET* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *x* |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati | sì                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Sì ( \_ solo vs 1 \_ 1) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

