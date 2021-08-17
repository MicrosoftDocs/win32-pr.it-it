---
title: GetRenderTargetSampleCount
description: Ottiene il numero di campioni per una destinazione di rendering.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- GetRenderTargetSampleCount HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54414d7af326c1a069585f9d5deaa3e728d421a65490c5b9f5322b98e06f531e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120135"
---
# <a name="getrendertargetsamplecount"></a>GetRenderTargetSampleCount

Ottiene il numero di campioni per una destinazione di rendering.



| *UINT* GetRenderTargetSampleCount() |
|-------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                 | Descrizione |
|--------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>Nessuno<br/> |             |



 

## <a name="return-value"></a>Valore restituito

Numero di campioni.

## <a name="remarks"></a>Commenti

Usare questa funzione e [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) per trovare il numero e la posizione delle posizioni di campionamento per una destinazione di rendering.

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Modello shader 4 e](dx-graphics-hlsl-sm4.md) modelli di shader superiori | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)           | no        |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





