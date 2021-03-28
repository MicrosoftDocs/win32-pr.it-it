---
title: trasposizione
description: Traspone la matrice di input specificata.
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- Trasponi HLSL
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44f129a87edaff260de87136954be7598ee3acb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399135"
---
# <a name="transpose"></a>trasposizione

Traspone la matrice di input specificata.



| RET Transpose (*x*) |
|--------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                             |
|--------------------------------------------------------|-----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nella \] matrice specificata.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore trasposto dal parametro *x* .

## <a name="remarks"></a>Commenti

Se le dimensioni della matrice di origine sono  *colonne* di righe, la matrice risultante è costituita da *righe* di *colonne* .

## <a name="type-description"></a>Descrizione del tipo



| Nome | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Dimensione                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| *x*  | [**matrice**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | any                                                                                    |
| RET  | [**matrice**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | righe = lo stesso numero di colonne dell'input *x*, colonne = lo stesso numero di righe dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader più elevati | sì       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

