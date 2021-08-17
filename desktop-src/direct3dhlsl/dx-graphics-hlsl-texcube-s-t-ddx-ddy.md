---
title: 'texCUBE (informazioni di riferimento su HLSL): selezionare il livello mip'
description: Campita una trama del cubo usando una sfumatura per selezionare il livello mip. | texCUBE (informazioni di riferimento su HLSL)
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
keywords:
- texCUBE HLSL
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e236a17359f94adcb8b54d3af8b67df37b1fcb6aaf7e75e6f4dba298eaae7aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725659"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a>texCUBE (informazioni di riferimento su HLSL): selezionare il livello mip

Campita una trama del cubo usando una sfumatura per selezionare il livello mip.



| ret texCUBE(s, t, ddx, ddy) |
|-----------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                         | Descrizione                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/>       | \[nello \] stato del campionatore.<br/>                                         |
| <span id="t"></span><span id="T"></span>*T*<br/>       | \[in \] Coordinata trama.<br/>                                    |
| <span id="ddx"></span><span id="DDX"></span>*Ddx*<br/> | \[in \] Frequenza di modifica della geometria della superficie nella direzione x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[in \] Frequenza di modifica della geometria della superficie nella direzione y.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore dei dati della trama.

## <a name="type-description"></a>Descrizione del tipo



| Nome | Ingresso/Uscita | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Oggetto**](dx-graphics-hlsl-intrinsic-functions.md) | [samplerCUBE](dx-graphics-hlsl-sampler.md)                    | 1    |
| t    | in     | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ddx  | in     | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| ddy  | in     | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ret  | in uscita    | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato                |
|-----------------------------------------------------------|--------------------------|
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì (solo pixel shader)  |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | sì (solo pixel shader) |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | sì (solo pixel shader) |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no                       |



 

1.  Il riordinamento significativo del codice viene eseguito per spostare i calcoli delle sfumature all'esterno del controllo di flusso.
2.  Se il limite D3DPSHADERCAPS2 0 è impostato con \_ D3DD3DPSHADERCAPS2 0 GRADIENTINSTRUCTIONS, il compilatore esegue il mapping di questa funzione a \_ \_ texldd.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

