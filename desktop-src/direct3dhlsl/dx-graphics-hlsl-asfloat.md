---
title: asfloat
description: Interpreta il modello di bit di x come numero a virgola mobile.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- asfloat HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d85f6010a8c82f8ae66d5fa56a979a9e946316a5e2737fe2c7257570499055d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043849"
---
# <a name="asfloat"></a>asfloat

Interpreta il modello di bit di *x* come numero a virgola mobile.



| ret asfloat(*x*) |
|------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Valore di input.<br/> |



 

## <a name="return-value"></a>Valore restituito

Input interpretato come numero a virgola mobile.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                                                                                | stesse dimensioni dell'input *x* |



 

## <a name="function-overloads"></a>Overload di funzioni

<dl> 'float <x> asfloat(float <x> value); `  
` float <x> asfloat(int <x> value); `  
` float <x> asfloat(uint <x> value);'
</dl>

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Modelli shader modello 4](dx-graphics-hlsl-sm4.md) e versioni successive | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | no        |



 

## <a name="remarks"></a>Commenti

I compilatori meno recenti consentiva erroneamente , ma si noti che `asfloat(bool)` gli input bool non sono supportati.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

