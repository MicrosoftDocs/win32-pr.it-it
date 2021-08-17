---
title: lerp
description: Esegue un'interpolazione lineare.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- lerp HLSL
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6981ef4134bbce17cbc7fa1e17de4d55de198572716ac39cbdd44b5e552e7f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791637"
---
# <a name="lerp"></a>lerp

Esegue un'interpolazione lineare.



| *ret* lerp(*x*, *y*, *s*) |
|---------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Primo valore a virgola mobile.<br/>                                                     |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Il secondo valore a virgola mobile.<br/>                                                    |
| <span id="s"></span><span id="S"></span>*s*<br/> | \[in \] Valore che interpola in modo lineare tra il *parametro x* e il parametro *y.*<br/> |



 

## <a name="return-value"></a>Valore restituito

Risultato dell'interpolazione lineare.

## <a name="type-description"></a>Descrizione del tipo



| Nome  | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**scalare,**](dx-graphics-hlsl-intrinsic-functions.md) **vettore** o **matrice** | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |
| *s*   | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |
| *Ret* | uguale all'input *x*                                                                                              | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | stesse dimensioni dell'input *x* |



 

## <a name="remarks"></a>Commenti

L'interpolazione lineare si basa sulla formula seguente: x (1-s) + y s che può essere scritta in modo equivalente come \* \* x + s(y-x).

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                                       | Supportato                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelli shader superiori | sì                         |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)                          | sì (vs \_ 1 \_ 1 e ps \_ 1 \_ 1) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

