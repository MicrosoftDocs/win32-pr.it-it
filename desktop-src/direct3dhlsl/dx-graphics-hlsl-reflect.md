---
title: riflettere
description: Restituisce un vettore di reflection utilizzando un raggio di evento imprevisto e una normale della superficie.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- riflette HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729927"
---
# <a name="reflect"></a>riflettere

Restituisce un vettore di reflection utilizzando un raggio di evento imprevisto e una normale della superficie.



| reflection *ret* (*i*, *n*) |
|-------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*i*<br/> | \[in \] un vettore di evento imprevisto a virgola mobile.<br/> |
| <span id="n"></span><span id="N"></span>*n*<br/> | \[in \] un vettore a virgola mobile normale.<br/>   |



 

## <a name="return-value"></a>Valore restituito

Vettore di Reflection A virgola mobile.

## <a name="remarks"></a>Commenti

Questa funzione calcola il vettore di Reflection usando la formula seguente: v = i-2 \* n \* dot (i n).

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*   | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *n*   | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *i* |
| *RET* | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *i* |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader più elevati | sì       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

