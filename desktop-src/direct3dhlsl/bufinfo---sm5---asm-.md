---
title: bufinfo (SM5-ASM)
description: Eseguire una query sul numero di elementi in un buffer (ma non sul buffer costante).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993077"
---
# <a name="bufinfo-sm5---asm"></a>bufinfo (SM5-ASM)

Eseguire una query sul numero di elementi in un buffer (ma non sul buffer costante).



| bufinfo dest \[ . mask \] , srcResource |
|------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[nell' \] indirizzo dei risultati.<br/>                                         |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[nel \] buffer, diverso da un buffer costante, in un SRV (t \# ) o in un UAV (u \# ).<br/> |



 

## <a name="remarks"></a>Commenti

Tutti i componenti in *dest* ricevono il numero intero di elementi nella visualizzazione delle risorse dello shader del buffer. Il numero di elementi dipende dai parametri di visualizzazione, ad esempio il formato della memoria.

Per un buffer tipizzato SRV o UAV, il valore restituito è il numero di elementi nella visualizzazione (in cui un elemento è un'unità del formato tipizzato).

Per un buffer non elaborato SRV o UAV, il valore restituito è il numero di byte nella visualizzazione.

Per un buffer strutturato SRV o UAV, il valore restituito è il numero di strutture nella visualizzazione.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





