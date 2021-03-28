---
title: dcl_input vGSInstanceID (SM5-ASM)
description: Abilita le istanze di Geometry shader.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335644"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a>\_vGSInstanceID di input DCL (SM5-ASM)

Abilita le istanze di Geometry shader.



| \_input DCL vGSInstanceID, instanceCount |
|-----------------------------------------|



 



| Elemento                                                                                                                       | Descrizione                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*<br/> | \[nell' \] ID istanza.<br/>    |
| <span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*<br/> | \[nel \] conteggio delle istanze.<br/> |



 

## <a name="remarks"></a>Commenti

Il parametro *instanceCount* della dichiarazione specifica il numero di istanze che il geometry shader deve eseguire per ogni primitiva di input. Il valore massimo per *instanceCount* è 32.

Il numero massimo di vertici dichiarati per l'output, tramite [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), viene applicato singolarmente a ogni istanza.

Il numero di istanze in questa dichiarazione, moltiplicato per il numero massimo di vertici per istanza tramite [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), deve essere <= 1024.

La quantità di dati che una data istanza geometry shader può emettere è 1024 scalari massimi, convalidata contando tutti i scalari dichiarati per l'input e moltiplicando il numero di vertici di output dichiarati.

L'uso delle istanze di Geometry shader aumenta in modo efficace la quantità totale di dati che possono essere emessi per primitive di input. 1024 scalars per una singola istanza restituisce fino a 1024 \* 32 scalari di dati di output in tutte le istanze di Geometry shader per una singola primitiva di input. Tuttavia, più istanze, minore è il numero di vertici che ogni istanza può emettere. Una singola istanza (nessuna istanza) può emettere 1024 vertici. Se si dichiara \* 32 istanze significa che ogni istanza può restituire solo i vertici 1024/32 = 32.

La dichiarazione di creazione di istanze di Geometry shader rende disponibile al programma un registro di input di tipo Integer a 32 bit autonomo, *vGSInstanceID*. Ogni istanza geometry shader è identificata dal valore contenuto in *vGSInstanceID* \[ 0, 1, 2... \] .

*vGSInstanceID* non fa parte della matrice di vertici di input geometry shader, ad esempio 3 vertici quando si inserisce un triangolo. Il registro *vGSInstanceID* si trova autonomamente, ad esempio vPrimitiveID.

Quando ogni istanza geometry shader termina, esiste una riduzione implicita nella topologia di output, quindi le istanze consecutive non dipendono l'una dall'altra.

Anche se l'hardware può eseguire ogni istanza geometry shader in parallelo, l'output di tutte le istanze alla fine viene serializzato come se tutte le chiamate geometry shader dell'istanza venissero eseguite in sequenza in un'iterazione del ciclo *vGSInstanceID* da 0 a *instanceCount*-1, con tagli della topologia di output impliciti alla fine di ogni istanza.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





