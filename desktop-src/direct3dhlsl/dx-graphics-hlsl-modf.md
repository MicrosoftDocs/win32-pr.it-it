---
title: modf (Corecrt \_ math.h)
description: Suddivide il valore x in parti frazionarie e intere, ognuna delle quali ha lo stesso segno di x.
ms.assetid: 0cac1cf3-f0da-4b0a-ba30-4af5d65b04b2
keywords:
- modf HLSL
topic_type:
- apiref
api_name:
- modf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c09af44cb95f35854d4366c05d238423fcecaff7c9a10c3c55fadf6b51dd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513812"
---
# <a name="modf"></a>modf

Suddivide il valore x in parti frazionarie e intere, ognuna delle quali ha lo stesso segno di x.



| ret modf(x, out ip) |
|---------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                      | Descrizione                                    |
|-----------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/>    | \[in \] Valore di input x.<br/>           |
| <span id="ip"></span><span id="IP"></span>*Ip*<br/> | \[out \] La parte intera di *x*.<br/> |



 

## <a name="return-value"></a>Valore restituito

Parte frazionaria con segno di x.

## <a name="type-description"></a>Descrizione del tipo



| Nome | Ingresso/Uscita | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md)                 | Dimensione                         |
|------|--------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in     | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| Ip   | in uscita    | uguale all'input x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | stesse dimensioni dell'input x |
| Ret  | in uscita    | uguale all'input x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | stesse dimensioni dell'input x |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                 |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sì (solo vs \_ \_ 1 1) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

