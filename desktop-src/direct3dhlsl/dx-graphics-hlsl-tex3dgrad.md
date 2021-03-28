---
title: tex3Dgrad
description: Esegue il campionamento di una trama 3D utilizzando una sfumatura per selezionare il livello MIP. | tex3Dgrad
ms.assetid: 230c42cc-31b7-4f57-ade4-14f069094d46
keywords:
- HLSL tex3Dgrad
topic_type:
- apiref
api_name:
- tex3Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cd8188b7f39cc2b79eb2e961857732cd8dae9f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981570"
---
# <a name="tex3dgrad"></a>tex3Dgrad

Esegue il campionamento di una trama 3D utilizzando una sfumatura per selezionare il livello MIP.



| RET tex3Dgrad (s, t, DDX, ddy) |
|-------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                         | Descrizione                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/>       | \[nello \] stato del campionatore.<br/>                                         |
| <span id="t"></span><span id="T"></span>*t*<br/>       | \[nella \] coordinata di trama.<br/>                                    |
| <span id="ddx"></span><span id="DDX"></span>*DDX*<br/> | \[\]frequenza di modifica della geometria della superficie nella direzione x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[\]frequenza di modifica della geometria della superficie nella direzione y.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore dei dati della trama.

## <a name="type-description"></a>Descrizione del tipo



| Nome | Ingresso/Uscita | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in ingresso     | [**oggetto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| u    | in ingresso     | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| DDX  | in ingresso     | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| ddy  | in ingresso     | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| RET  | in uscita    | [**vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato                |
|-----------------------------------------------------------|--------------------------|
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | Sì (solo pixel shader)  |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Sì (solo pixel shader) |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Sì (solo pixel shader) |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no                       |



 

1.  Il riordino significativo del codice viene eseguito per spostare i calcoli delle sfumature all'esterno del controllo di flusso.
2.  Se il limite di D3DPSHADERCAPS2 \_ 0 è impostato su \_ D3DD3DPSHADERCAPS2 0 \_ GRADIENTINSTRUCTIONS, il compilatore esegue il mapping di questa funzione a texldd.

## <a name="remarks"></a>Commenti

Quando il controllo di flusso è presente in uno shader, il risultato di un calcolo della sfumatura richiesto all'interno di un percorso di branch specificato è ambiguo quando i pixel adiacenti possono passare a percorsi di controllo di flusso separati. Pertanto, viene considerato non valido utilizzare qualsiasi operazione di pixel shader che richiede un calcolo di sfumatura in una posizione all'interno di un costrutto di controllo di flusso che può variare tra i pixel per una determinata primitiva che viene rasterizzata. Se uno dei lati di un'istruzione **if** con l'attributo Branch usa una funzione gradiente, è possibile che venga generato un errore del compilatore. Vedere l' [istruzione if (DirectX HLSL)](dx-graphics-hlsl-if.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

