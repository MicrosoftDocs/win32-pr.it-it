---
title: tex3D (riferimento HLSL)
description: Campiona una trama 3D.
ms.assetid: 713eec24-bdf5-456e-98da-30e2c9d7e808
keywords:
- HLSL tex3D
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3a071d00dedabdff02bae302c71aa8ecece4ba2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729519"
---
# <a name="tex3d-hlsl-reference"></a>tex3D (riferimento HLSL)

Campiona una trama 3D.



| tex3D RET (s, t) |
|-----------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[nello \] stato del campionatore.<br/>      |
| <span id="t"></span><span id="T"></span>*t*<br/> | \[nella \] coordinata di trama.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore dei dati della trama.

## <a name="type-description"></a>Descrizione del tipo



| Nome | Ingresso/Uscita | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in ingresso     | [**oggetto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| u    | in ingresso     | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| RET  | in uscita    | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | Sì (solo pixel shader), ma è necessario usare l' [opzione di compilazione legacy](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) durante la compilazione. |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Sì (solo pixel shader)                                                                                                           |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Sì (solo pixel shader)                                                                                                           |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Sì (solo pixel shader)                                                                                                           |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

