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
ms.openlocfilehash: c31bc829f8990517ddbea8be7c25eead413ab666
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120576"
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
| [Modello shader 4 e](dx-graphics-hlsl-sm4.md) modelli di shader superiori | yes       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | No        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | No        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md)           | No        |



 

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





