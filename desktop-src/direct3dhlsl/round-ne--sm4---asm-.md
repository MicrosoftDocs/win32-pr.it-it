---
title: round_ne (sm4 - asm)
description: Arrotondamento a virgola mobile a float integrale. | round_ne (sm4 - asm)
ms.assetid: 2D1A0786-F7DB-4D69-9F56-82ECD1EE7ABA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0efb2ff10b75e50ec05847dd25aa8448c760c7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993928"
---
# <a name="round_ne-sm4---asm"></a>round \_ ne (sm4 - asm)

Arrotondamento a virgola mobile a float integrale.



| round \_ ne \[ \_ sat \] dest \[ \] .mask, \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|------------------------------------------------------------------|



 



| Elemento                                                            | Descrizione                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Indirizzo dei risultati dell'operazione.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Componenti dell'operazione.<br/>             |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un round a virgola mobile per componente dei valori in *src0*, scrivendo valori a virgola mobile integrali *in dest*. **round \_ ne** arrotonda verso il valore pari più vicino.

La tabella seguente mostra i risultati ottenuti durante l'esecuzione dell'istruzione con diverse classi di numeri.

F indica un numero finito-reale.



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | -inf     | -F     | -0          | -0     | +0     | +0          | +F     | +inf     | NaN     |



 

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





