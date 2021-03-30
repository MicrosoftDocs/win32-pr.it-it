---
title: abs
description: Restituisce il valore assoluto del valore specificato.
ms.assetid: 8c4cfd8f-8aac-4db3-8247-ce2bbf501e80
keywords:
- HLSL ABS
topic_type:
- apiref
api_name:
- abs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1acd1903e1a65a38f5af7549ab52577bc6cba51c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976794"
---
# <a name="abs"></a>abs

Restituisce il valore assoluto del valore specificato.



| ABS RET (*x*) |
|--------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nel \] valore specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore assoluto del parametro *x* .

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *RET* | uguale all'input *x*                                                                                              | uguale all'input *x*                                                              | le stesse dimensioni di input *x* |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato             |
|------------------------------------------------------------------------------------|-----------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader più elevati | sì                   |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 e PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

