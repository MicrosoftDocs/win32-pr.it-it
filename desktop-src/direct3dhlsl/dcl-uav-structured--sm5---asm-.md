---
title: dcl_uav_structured (SM5-ASM)
description: Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'utilizzo da uno shader. | dcl_uav_structured (SM5-ASM)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234714"
---
# <a name="dcl_uav_structured-sm5---asm"></a>\_ \_ struttura di DCL UAV (SM5-ASM)

Dichiarare una visualizzazione di accesso non ordinata (UAV) per l'utilizzo da uno shader.



| DCL \_ UAV \_ strutturato \[ \_ GLC \] dstUAV, structByteStride |
|--------------------------------------------------------|



 



| Elemento                                                                                                                                   | Descrizione                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                                         | \[nel \] UAV.<br/>                            |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[nella \] dimensione della struttura in byte.<br/> |



 

## <a name="remarks"></a>Commenti

*dstUAV* è un \# registro u dichiarato come riferimento a un UnorderedAccessView di un buffer strutturato con lo stride specificato che deve essere associato allo slot UAV nell' \# API.

Il contenuto della struttura non è di tipo; le operazioni eseguite sulla memoria possono interpretare in modo implicito i dati come aventi un tipo.

*structByteStride* è la dimensione della struttura in byte nel buffer dichiarato. Il valore deve essere maggiore di zero. *structByteStride* è di tipo uint e deve essere un multiplo di 4.

Le istruzioni che fanno riferimento a un'u strutturata \# accettano un indirizzo 2D, in cui il primo componente sceglie \[ struct \] e il secondo componente sceglie \[ offset all'interno dello struct, in byte allineati \] .

Il \_ flag GLC significa "globalmente coerente". L'assenza di \_ GLC significa che il UAV viene dichiarato solo come "gruppo coerente" nel compute shader o "coerente localmente" in una singola chiamata di pixel shader.

Il \_ flag OPC è il contatore per la conservazione degli ordini. Indica che se un UAV è associato a uno slot \# (u \# ), è necessario che sia stato creato con il flag del contatore. Ciò significa che le operazioni [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) o [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) nello shader consentono di modificare un contatore i cui valori possono essere usati nello shader come riferimento permanente a una posizione nell'UAV. Non è possibile riordinare i dati dopo che lo shader è stato superato.

L'assenza del \_ flag OPC significa che se lo shader usa le istruzioni[IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) o [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) e un UAV è associato a slot \# (u), è necessario che sia stato creato con il flag Append, che fornisce un contatore che non garantisce che l'ordine venga mantenuto dopo la chiamata dello shader.

Se il \_ flag OPC è assente e lo shader non contiene le istruzioni [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) o [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) , è consentito creare un UAV associato a slot \# (u) con il flag del contatore (il contatore non verrà usato da questo shader), nessun flag (nessun contatore), ma non con il flag di Accodamento.

> [!Note]  
> cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano **DCL \_ TGSM \_ strutturate**, ma [non \_ TGSM DCL \_ RAW](dcl-tgsm-raw--sm5---asm-.md).

 

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.



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



 

> [!Note]  
> Questa istruzione è supportata in cs \_ 4 \_ 0 e cs \_ 4 \_ 1.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





