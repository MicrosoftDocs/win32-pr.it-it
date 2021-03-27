---
title: texCUBE (riferimento HLSL)
description: Esegue il campionamento di una trama del cubo.
ms.assetid: 77943eb9-86e8-4ae4-8975-8f925e084ce4
keywords:
- HLSL texCUBE
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 524ed44028372eeabf176c30da8b3a31a8ee7988
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046876"
---
# <a name="texcube-hlsl-reference"></a>texCUBE (riferimento HLSL)

Esegue il campionamento di una trama del cubo.



| texCUBE RET (s, t) |
|-------------------|



 

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
| s    | in ingresso     | [**oggetto**](dx-graphics-hlsl-intrinsic-functions.md) | [samplerCUBE](dx-graphics-hlsl-sampler.md)                    | 1    |
| u    | in ingresso     | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| RET  | in uscita    | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato               |
|-----------------------------------------------------------|-------------------------|
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | Sì (solo pixel shader) |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Sì (solo pixel shader) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Sì (solo pixel shader) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Sì (solo pixel shader) |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

