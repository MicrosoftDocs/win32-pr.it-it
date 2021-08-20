---
title: isnan (Corecrt \_ math.h)
description: Determina se il valore specificato è NAN o QNAN.
ms.assetid: 09085634-e610-4793-848e-abda8241f1cc
keywords:
- isnan HLSL
topic_type:
- apiref
api_name:
- isnan
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5f60f04d577bcd2e2f8d13cf11e1c02237ae9ddfacd225dff3d0bfca4266c72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791940"
---
# <a name="isnan"></a>isnan

Determina se il valore specificato è NAN o QNAN.



| *ret* isnan(*x*) |
|------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Il valore specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

Restituisce un valore delle stesse dimensioni dell'input, con un valore impostato su **True** se il *parametro x* è NAN o QNAN. In caso contrario, **False.**

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any      |
| *Ret* | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Bool**](/windows/desktop/WinProg/windows-data-types)                         | come input |



 

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

 

