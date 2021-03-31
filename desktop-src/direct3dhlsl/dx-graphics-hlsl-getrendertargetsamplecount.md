---
title: GetRenderTargetSampleCount
description: Ottiene il numero di campioni per una destinazione di rendering.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- HLSL GetRenderTargetSampleCount
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96c159a2ed63684b4bad2cbc6fa789c2dbd76edf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471998"
---
# <a name="getrendertargetsamplecount"></a>GetRenderTargetSampleCount

Ottiene il numero di campioni per una destinazione di rendering.



| *Uint* GetRenderTargetSampleCount() |
|-------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                 | Descrizione |
|--------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>Nessuno<br/> |             |



 

## <a name="return-value"></a>Valore restituito

Numero di campioni.

## <a name="remarks"></a>Commenti

Usare questa funzione e [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) per trovare il numero e la posizione dei percorsi di campionamento per una destinazione di rendering.

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

 

 





