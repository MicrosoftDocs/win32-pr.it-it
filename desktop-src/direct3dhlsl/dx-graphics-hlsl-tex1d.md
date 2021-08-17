---
title: tex1D (informazioni di riferimento su HLSL)
description: Campionamento di una trama 1D.
ms.assetid: 587be0fd-af12-4bf0-862b-84988435e90e
keywords:
- tex1D HLSL
topic_type:
- apiref
api_name:
- tex1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fd7c8b02d9bbd904ae9205201203bbfdb06ad48d749048be7bc81cbfa83caca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725689"
---
# <a name="tex1d-hlsl-reference"></a>tex1D (informazioni di riferimento su HLSL)

Campionamento di una trama 1D.



| ret tex1D(s, t) |
|-----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[nello \] stato del campionatore.<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[in \] Coordinata trama.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore dei dati di trama.

## <a name="type-description"></a>Descrizione del tipo



| Nome | Ingresso/Uscita | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Oggetto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler1D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Scalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| Ret  | in uscita    | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì (pixel shader solo), ma è necessario usare l'opzione di compilazione [legacy](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) durante la compilazione. |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sì (solo pixel shader)                                                                                                           |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sì (solo pixel shader)                                                                                                           |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | sì (solo pixel shader)                                                                                                           |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

