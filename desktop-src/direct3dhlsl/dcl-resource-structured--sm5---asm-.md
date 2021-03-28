---
title: struttura dcl_resource (SM5-ASM)
description: Dichiarare un input di risorsa shader e assegnarlo a un registro segnaposto t \-a per la risorsa. | struttura dcl_resource (SM5-ASM)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234685"
---
# <a name="dcl_resource-structured-sm5---asm"></a>\_struttura della risorsa DCL (SM5-ASM)

Dichiarare un input di risorsa dello shader e assegnarlo a un \# Registro di segnaposto t-a per la risorsa.



| \_ \_ dstSRV strutturato delle risorse DCL, structByteStride |
|----------------------------------------------------|



 



| Elemento                                                                                                                                   | Descrizione                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/>                                         | \[in \] un \# Registro t dichiarato come riferimento a un ShaderResourceView di un buffer strutturato con lo stride specificato che deve essere associato allo slot SRV \# nell'API. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[in \] un uint che specifica la dimensione della struttura in byte nel buffer dichiarato. Il valore deve essere maggiore di zero.<br/>                                   |



 

## <a name="remarks"></a>Commenti

Il contenuto della struttura non è di tipo; le operazioni eseguite sulla memoria possono interpretare in modo implicito i dati come aventi un tipo.

Le istruzioni che fanno riferimento a un'istruzione t strutturata \# accettano un indirizzo 2D, dove il primo componente sceglie lo \[ struct \] e il secondo componente sceglie \[ offset all'interno dello struct, più di 32 bit \] .

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione.

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

 

 





