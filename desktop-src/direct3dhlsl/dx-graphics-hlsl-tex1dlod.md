---
title: tex1Dlod
description: Campiona una trama 1D con mipmap. Il mipmap LOD è specificato in t.w.
ms.assetid: f1700ee6-2f79-4b8b-ad34-30561f319356
keywords:
- HLSL tex1Dlod
topic_type:
- apiref
api_name:
- tex1Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca6379448290d027bba8a8b62f80cac39c84f25
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729159"
---
# <a name="tex1dlod"></a>tex1Dlod

Campiona una trama 1D con mipmap. Il mipmap LOD è specificato in t.w.



| tex1Dlod RET (s, t) |
|--------------------|



 

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
| s    | in ingresso     | [**oggetto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler1D](dx-graphics-hlsl-sampler.md)                      | 1    |
| u    | in ingresso     | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| RET  | in uscita    | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato               |
|-----------------------------------------------------------|-------------------------|
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | Sì (solo pixel shader) |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Sì (solo pixel shader) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no                      |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no                      |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

