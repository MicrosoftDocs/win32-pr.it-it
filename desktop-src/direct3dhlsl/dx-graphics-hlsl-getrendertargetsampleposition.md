---
title: GetRenderTargetSamplePosition
description: Ottiene la posizione di campionamento (x, y) per un indice di esempio specificato.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- HLSL GetRenderTargetSamplePosition
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0cd944b175522ab7d722ae791f3548c6633b71
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103717776"
---
# <a name="getrendertargetsampleposition"></a>GetRenderTargetSamplePosition

Ottiene la posizione di campionamento (x, y) per un indice di esempio specificato.



|                                                                                  |
|----------------------------------------------------------------------------------|
| float<2> GetRenderTargetSamplePosition (in int<1> index<br/>); |



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                       | Descrizione                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Indice*<br/> | \[in \] un indice di esempio in base zero.<br/> |



 

## <a name="return-value"></a>Valore restituito

Posizione (x, y) dell'esempio specificato.

## <a name="remarks"></a>Commenti

Usare questa funzione e [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) per trovare il numero e la posizione dei percorsi di campionamento per una destinazione di rendering.

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | no        |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





