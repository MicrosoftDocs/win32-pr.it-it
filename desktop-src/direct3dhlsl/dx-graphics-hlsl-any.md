---
title: any
description: Determina se i componenti del valore specificato sono diversi da zero.
ms.assetid: 69a30478-662a-47de-babc-3cc67f89809c
keywords:
- qualsiasi HLSL
topic_type:
- apiref
api_name:
- any
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 785e284b356acfa95615ac806b0433eb39ad737db5a6cca85365ecd0b48d27db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118091228"
---
# <a name="any"></a>any

Determina se i componenti del valore specificato sono diversi da zero.



| *ret* any(*x*) |
|----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Il valore specificato.<br/> |



 

## <a name="return-value"></a>Valore restituito

**True** se i componenti del *parametro x* sono diversi da zero. in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Questa funzione è simile a tutte [**le funzioni**](dx-graphics-hlsl-all.md) intrinseche HLSL. La **funzione any** determina se i componenti del valore specificato sono diversi da zero, mentre la funzione **all** determina se tutti i componenti del valore specificato sono diversi da zero.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Dimensione |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | any  |
| *Ret* | [**Scalare**](dx-graphics-hlsl-intrinsic-functions.md)                            | [**Bool**](/windows/desktop/WinProg/windows-data-types)                                                                                 | 1    |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato             |
|------------------------------------------------------------------------------------|-----------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                   |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 e ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

