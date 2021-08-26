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
ms.openlocfilehash: 901b64099547060305bab6db43cbe75b3fdb8d9c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886267"
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

<dl> `float&lt;x&gt; asfloat(float&lt;x&gt; value);`  
`float&lt;x&gt; asfloat(int&lt;x&gt; value);`  
`float&lt;x&gt; asfloat(uint&lt;x&gt; value);`  
</dl>

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Modello shader 4](dx-graphics-hlsl-sm4.md) e modelli shader superiori | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | no        |



 

## <a name="remarks"></a>Commenti

I compilatori meno recenti consentiva erroneamente , ma si noti che `asfloat(bool)` gli input bool non sono supportati.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

