---
title: asin
description: Restituisce l'arcoseno del valore specificato.
ms.assetid: 49559cb2-3305-4c97-8071-1589bcca3a75
keywords:
- HLSL Asin
topic_type:
- apiref
api_name:
- asin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2f64865cb3172037f6630dc422a69aa4d135b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047300"
---
# <a name="asin"></a>asin

Restituisce l'arcoseno del valore specificato.



| asin *ret* (*x*) |
|-----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nel \] valore specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Arcoseno del parametro *x* .

## <a name="remarks"></a>Commenti

Ogni componente del parametro *x* deve essere compreso nell'intervallo tra-π/2 e π/2.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *RET* | uguale all'input *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | le stesse dimensioni di input *x* |



 

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

 

