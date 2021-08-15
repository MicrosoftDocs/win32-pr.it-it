---
title: asuint
description: Interpreta il modello di bit di x come intero senza segno.
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- Asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ac8be8a81cca5c0ed7377475f2e3688a8c0c90c33fddcaab8c4de0f15f174eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514774"
---
# <a name="asuint"></a>asuint

Interpreta il modello di bit di *x* come intero senza segno.



| ret asuint(*x*) |
|-----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Valore di input.<br/> |



 

## <a name="return-value"></a>Valore restituito

Input interpretato come intero senza segno.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *Ret* | uguale all'input *x*                                                                                              | [**uint**](/windows/desktop/WinProg/windows-data-types)                                         | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Modello shader 4 e](dx-graphics-hlsl-sm4.md) modelli di shader superiori | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)           | no        |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

