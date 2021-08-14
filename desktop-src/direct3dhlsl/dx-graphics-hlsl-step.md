---
title: step
description: Confronta due valori, restituisce 0 o 1 in base al valore maggiore.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- passaggio HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27fe6985a4dfb4e77f1052b421a6c46c617395f46b4484f046b33919a935613f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276511"
---
# <a name="step"></a>step

Confronta due valori, restituisce 0 o 1 in base al valore maggiore.



| *ret* step(*y*, *x*) |
|----------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Primo valore a virgola mobile da confrontare.<br/>  |
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Il secondo valore a virgola mobile da confrontare.<br/> |



 

## <a name="return-value"></a>Valore restituito

1 se il *parametro x* è maggiore o uguale al *parametro y;* in caso contrario, 0.

## <a name="remarks"></a>Commenti

Questa funzione usa la formula seguente: (*x*  >=  *y*) ? 1 : 0. La funzione restituisce 0 o 1 a seconda che il *parametro x* sia maggiore del *parametro y.* Per calcolare un'interpolazione uniforme tra 0 e 1, usare la funzione intrinseca [**smoothstep**](dx-graphics-hlsl-smoothstep.md) HLSL.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *x*   | uguale all'input *y*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *y* |
| *Ret* | uguale all'input *y*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *y* |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                         |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sì (vs \_ 1 \_ 1 e ps \_ 1 \_ 4) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

