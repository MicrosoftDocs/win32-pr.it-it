---
title: dcl_stream (sm5 - asm)
description: Dichiarare un flusso di output geometry shader.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53b8226cc9a4d8d2bd980cd26371f9e7b46a5168ec61ff39e425f73a4d7193c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793042"
---
# <a name="dcl_stream-sm5---asm"></a>Flusso dcl \_ (sm5 - asm)

Dichiarare un flusso di output geometry shader.



| dcl \_ stream m\# |
|-----------------|



 



| Elemento                                                       | Descrizione                             |
|------------------------------------------------------------|-----------------------------------------|
| <span id="m_"></span><span id="M_"></span>*M\#*<br/> | \[in \] Stream 0..3 (m0.. m3).<br/> |



 

## <a name="remarks"></a>Commenti

Un flusso specificato può essere dichiarato una sola volta.

Se non viene dichiarato alcun flusso, si presuppone che le dichiarazioni di topologia di output e output siano per il flusso 0.

Il primo **flusso dcl \_ non** può essere visualizzato dopo alcuna **istruzione \_ dcl output** o **dcl \_ outputTopology.**

Qualsiasi **istruzione dcl \_ output o** **dcl \_ outputToplogic** dopo qualsiasi **istruzione dcl \_ stream** m definisce \# gli output per il flusso m \# .

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





