---
title: pow
description: Restituisce il valore specificato elevato alla potenza specificata.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- pow HLSL
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9d26e150d611df12f2e042d2e20c06ab82172bbc3d2f241ee1ce3a4725f1193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120075"
---
# <a name="pow"></a>pow

Restituisce il valore specificato elevato alla potenza specificata.



| *ret* pow(*x*, *y*) |
|---------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Valore specificato.<br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Potenza specificata.<br/> |



 

## <a name="return-value"></a>Valore restituito

Parametro *x* elevato alla potenza del *parametro y.*

## <a name="remarks"></a>Commenti

La **funzione intrinseca** HLSL pow calcola *x*<sup>y</sup>.



| X      | Y      | Risultato                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| < 0 | any    | NAN                                                                         |
| > 0 | == 0   | 1                                                                           |
| == 0   | > 0 | 0                                                                           |
| == 0   | < 0 | Inf                                                                         |
| > 0 | < 0 | 1/X<sup>-Y</sup>                                                            |
| == 0   | == 0   | Dipende dal processore di grafica specifico<br/> 0, 1 o NA<br/> |



 

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                 |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | sì (solo \_ vs 1 \_ 1) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

