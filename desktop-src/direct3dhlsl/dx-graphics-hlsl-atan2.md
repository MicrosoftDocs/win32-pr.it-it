---
title: atan2 (Corecrt \_ math.h)
description: Restituisce l'arcotangente di due valori (x,y).
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- atan2 HLSL
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2932f82cf6d9e8b2071446b63f84e60727aff2da2213461d3c1194b2811fe1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854971"
---
# <a name="atan2"></a>atan2

Restituisce l'arcotangente di due valori (x,y).



| *ret* atan2(*y*, *x*) |
|-----------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                    |
|--------------------------------------------------------|--------------------------------|
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Valore y.<br/> |
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Valore x.<br/> |



 

## <a name="return-value"></a>Valore restituito

Arcotangente di (y,x).

## <a name="remarks"></a>Commenti

I segni dei *parametri x* e *y* vengono usati per determinare il quadrante dei valori restituiti nell'intervallo di -π da π. La **funzione intrinseca atan2** HLSL è ben definita per ogni punto diverso dall'origine, anche se *y* è uguale a 0 e *x* non è uguale a 0.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì       |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

