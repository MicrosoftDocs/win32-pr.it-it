---
title: texCUBEgrad
description: Campiota una trama del cubo usando una sfumatura per selezionare il livello mip. | texCUBEgrad
ms.assetid: ebc5e38a-e314-43b0-9a00-7e4147e24bf0
keywords:
- texCUBEgrad HLSL
topic_type:
- apiref
api_name:
- texCUBEgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 831cfafcdc970a785bb702cabeac5b7ef881526421ef5ada9cb05cd1b407ce6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119885"
---
# <a name="texcubegrad"></a>texCUBEgrad

Campiota una trama del cubo usando una sfumatura per selezionare il livello mip.



| ret texCUBEgrad(s, t, ddx, ddy) |
|---------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                         | Descrizione                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/>       | \[nello \] stato del campionatore.<br/>                                         |
| <span id="t"></span><span id="T"></span>*T*<br/>       | \[in \] Coordinata trama.<br/>                                    |
| <span id="ddx"></span><span id="DDX"></span>*Ddx*<br/> | \[in \] Frequenza di modifica della geometria della superficie nella direzione x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[in \] Frequenza di modifica della geometria della superficie nella direzione y.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore dei dati di trama.

## <a name="type-description"></a>Descrizione del tipo



| Nome | Ingresso/Uscita | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Oggetto**](dx-graphics-hlsl-intrinsic-functions.md) | [samplerCUBE](dx-graphics-hlsl-sampler.md)                    | 1    |
| t    | in     | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ddx  | in     | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| ddy  | in     | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ret  | in uscita    | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato                |
|-----------------------------------------------------------|--------------------------|
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì (solo pixel shader)  |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sì (solo pixel shader) |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sì (solo pixel shader) |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no                       |



 

1.  Il riordinamento significativo del codice viene eseguito per spostare i calcoli delle sfumature al di fuori del controllo di flusso.
2.  Se il limite D3DPSHADERCAPS2 0 è impostato con \_ D3DD3DPSHADERCAPS2 0 GRADIENTINSTRUCTIONS, il compilatore esegue il mapping di questa funzione a \_ \_ texldd.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

