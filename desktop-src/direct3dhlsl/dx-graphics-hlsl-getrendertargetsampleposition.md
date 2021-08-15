---
title: GetRenderTargetSamplePosition
description: Ottiene la posizione di campionamento (x,y) per un determinato indice di campionamento.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- GetRenderTargetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a406fcbd023d0688baf51cabbfea53438f3d58a6fba4d1fc7d1bf8d33077262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514335"
---
# <a name="getrendertargetsampleposition"></a>GetRenderTargetSamplePosition

Ottiene la posizione di campionamento (x,y) per un determinato indice di campionamento.

float<2> GetRenderTargetSamplePosition( in int<1> Index<br/>);



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                       | Descrizione                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Indice*<br/> | \[in \] un indice di esempio in base zero.<br/> |



 

## <a name="return-value"></a>Valore restituito

Posizione (x,y) dell'esempio specificato.

## <a name="remarks"></a>Commenti

Usare questa funzione e [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) per individuare il numero e la posizione delle posizioni di campionamento per una destinazione di rendering.

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

 

 





