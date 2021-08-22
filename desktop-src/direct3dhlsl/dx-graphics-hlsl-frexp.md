---
title: frexp (Corecrt \_ math.h)
description: Restituisce la mantissa e l'esponente del valore a virgola mobile specificato.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- frexp HLSL
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f77ab30f525c37fcb2243bb6f634722420836f3893a4550edbb6604c8769773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276621"
---
# <a name="frexp"></a>frexp

Restituisce la mantissa e l'esponente del valore a virgola mobile specificato.



| *ret* frexp(*x*, *exp*) |
|-------------------------|



 

Il valore restituito è la mantissa e il valore restituito dal *parametro exp* è l'esponente.

## <a name="parameters"></a>Parametri



| Elemento                                                         | Descrizione                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[in \] Valore a virgola mobile specificato. Se il *parametro x* è 0, questa funzione restituisce 0 sia per la mantissa che per l'esponente.<br/> |
| <span id="exp"></span><span id="EXP"></span>*Exp*<br/> | \[out \] Esponente restituito del *parametro x.*<br/>                                                                                   |



 

## <a name="return-value"></a>Valore restituito

Mantissa del *parametro x.*

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *exp* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato           |
|------------------------------------------------------------------------------------|---------------------|
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelli shader superiori | sì                 |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | yes (solo ps \_ 2 \_ x) |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | no                  |



 

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

