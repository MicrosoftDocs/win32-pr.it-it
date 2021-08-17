---
title: tex2Dgrad
description: Campiota una trama 2D usando una sfumatura per selezionare il livello mip. | tex2Dgrad
ms.assetid: a9ab7972-3480-4b37-aa10-c5cf811bdd0e
keywords:
- tex2Dgrad HLSL
topic_type:
- apiref
api_name:
- tex2Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 358690291cbb8cffbf6d60ef034b42d075902b923a3899824845e42bad999a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119915"
---
# <a name="tex2dgrad"></a>tex2Dgrad

Campiota una trama 2D usando una sfumatura per selezionare il livello mip.



| ret tex2Dgrad(s, t, ddx, ddy) |
|-------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                         | Descrizione                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/>       | \[nello \] stato del campionatore.<br/>                                         |
| <span id="t"></span><span id="T"></span>*T*<br/>       | \[in \] Coordinate della trama.<br/>                                   |
| <span id="ddx"></span><span id="DDX"></span>*Ddx*<br/> | \[in \] Frequenza di modifica della geometria della superficie nella direzione x.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[in \] Frequenza di modifica della geometria della superficie nella direzione y.<br/> |



 

## <a name="return-value"></a>Valore restituito

Valore dei dati di trama.

## <a name="type-description"></a>Descrizione del tipo



| Nome | Ingresso/Uscita | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Oggetto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| Ddx  | in     | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| ddy  | in     | [**Vettore**](dx-graphics-hlsl-intrinsic-functions.md) | [**Galleggiante**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
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

## <a name="remarks"></a>Commenti

Quando il controllo di flusso è presente in uno shader, il risultato di un calcolo della sfumatura richiesto all'interno di un determinato percorso di ramo è ambiguo quando i pixel adiacenti possono scendere in percorsi di controllo di flusso separati. Pertanto, è considerato non valido usare qualsiasi operazione di pixel shader che richiede un calcolo della sfumatura in una posizione all'interno di un costrutto di controllo di flusso che può variare in pixel per una determinata primitiva in fase di rasterizzato. Se su entrambi i lati di **un'istruzione if** con l'attributo branch viene utilizzata una funzione sfumatura, potrebbe essere generato un errore del compilatore. Vedere [l'istruzione if (DirectX HLSL)](dx-graphics-hlsl-if.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

