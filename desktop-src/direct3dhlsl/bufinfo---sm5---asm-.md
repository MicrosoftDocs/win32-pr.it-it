---
title: bufinfo (sm5 - asm)
description: Eseguire una query sul conteggio degli elementi in un buffer (ma non sul buffer costante).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a107896973e7457b4bf596843ec77934d95675d50a146190a7f9f40e1c2ce3c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287584"
---
# <a name="bufinfo-sm5---asm"></a>bufinfo (sm5 - asm)

Eseguire una query sul conteggio degli elementi in un buffer (ma non sul buffer costante).



| bufinfo dest \[ .mask \] , srcResource |
|------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Indirizzo dei risultati.<br/>                                         |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] Buffer, diverso da una costante Buffer, in una SRV (t \# ) o UAV (u \# ).<br/> |



 

## <a name="remarks"></a>Commenti

Tutti i componenti in *dest* ricevono il numero intero di elementi nella visualizzazione delle risorse shader del buffer. Il numero di elementi dipende dai parametri di visualizzazione, ad esempio il formato di memoria.

Per un buffer tipidato SRV o UAV, il valore restituito è il numero di elementi nella visualizzazione (dove un elemento è un'unità del formato tipiato).

Per un buffer non elaborato SRV o UAV, il valore restituito è il numero di byte nella visualizzazione.

Per un buffer strutturato SRV o UAV, il valore restituito è il numero di strutture nella vista.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa istruzione è supportata nei modelli di shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





