---
title: samplepos (sm4.1 - asm)
description: Esegue una query sulla posizione di un esempio in una determinata visualizzazione delle risorse shader o nel rasterizzatore.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2457ca682adacf5daa274b3efbe6c76eb37523df4267cdb20131576815c2b6f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510165"
---
# <a name="samplepos-sm41---asm"></a>samplepos (sm4.1 - asm)

Esegue una query sulla posizione di un esempio in una determinata visualizzazione delle risorse shader o nel rasterizzatore.



| samplepos dest \[ .mask \] , srcResource \[ .swizzle \] , sampleIndex (operando scalare) |
|--------------------------------------------------------------------------------|



 



| Elemento                                                                                                               | Descrizione                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Indirizzo dei risultati dell'operazione.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[nella \] risorsa shader.<br/>                         |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*sampleIndex*<br/> | \[in \] Indice dell'esempio.<br/>                     |



 

## <a name="remarks"></a>Commenti

Questa istruzione restituisce la posizione di esempio 2D di *sampleIndex* per la risorsa specificata. È valido solo per le risorse che possono essere caricate usando [**ld2dms,**](ld2dms--sm4-1---asm-.md) a meno che il rasterizzatore non sia *specificato come srcResource*.

*srcResource* può essere un registro t \# (una visualizzazione di risorse shader) o un registro di rasterizzazione.

L'istruzione calcola il vettore a virgola mobile (Xposition, Yposition, 0, 0).

Lo swizzle in *srcResource* consente di eseguire lo swizzle arbitrario dei valori restituiti prima che siano scritti nella destinazione. La posizione del campione è relativa al centro del pixel, in base al sistema di coordinate pixel.

Se *sampleIndex* non rientra nei limiti, viene restituito un vettore zero. Se non è presente alcuna risorsa associata a uno slot specificato, viene restituito 0.

**samplepos può** essere usato per elementi come le operazioni di risoluzione personalizzate nel codice dello shader.

Questa istruzione si applica alle fasi di shader seguenti:



| Vertex shader | Geometry shader | Pixel shader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | sì       |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 4 (HLSL DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





