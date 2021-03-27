---
title: dcl_resource RAW (SM5-ASM)
description: Dichiarare un input di risorsa shader e assegnarlo a un registro segnaposto t \-a per la risorsa. | dcl_resource RAW (SM5-ASM)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234748"
---
# <a name="dcl_resource-raw-sm5---asm"></a>\_risorsa DCL RAW (SM5-ASM)

Dichiarare un input di risorsa dello shader e assegnarlo a un \# Registro di segnaposto t-a per la risorsa.



| \_dstSRV RAW delle risorse DCL \_ |
|---------------------------|



 



| Elemento                                                                                           | Descrizione                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/> | \[in \] un \# Registro t dichiarato come riferimento a un ShaderResourceView di un buffer non elaborato.<br/> |



 

## <a name="remarks"></a>Commenti

Il contenuto della struttura non è di tipo; le operazioni eseguite sulla memoria possono interpretare in modo implicito i dati come aventi un tipo.

Le istruzioni che fanno riferimento a una t non elaborata \# accettano un indirizzo 1D, un valore senza segno a 32 bit che specifica l'offset dei byte a una posizione allineata a 32 bit nel buffer. L'indirizzo deve essere un multiplo di 4 (byte).

Le visualizzazioni vincolate a t \# dichiarate come RAW devono avere un valore RAW specificato durante la creazione; in caso contrario, il comportamento quando si accede da uno shader non è definito.

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

 

 





