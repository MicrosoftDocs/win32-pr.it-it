---
title: dcl_uav_structured (sm5 - asm)
description: Dichiarare una visualizzazione di accesso non ordinato per l'uso da parte di uno shader. | dcl_uav_structured (sm5 - asm)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b398dc8b59db6d8fc3a64effdf3cd93b56664881c4c7024a185ad6a212b9fb4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726799"
---
# <a name="dcl_uav_structured-sm5---asm"></a>dcl \_ uav \_ structured (sm5 - asm)

Dichiarare una visualizzazione di accesso non ordinato per l'uso da parte di uno shader.



| dcl \_ uav \_ structured \[ \_ glc \] dstUAV, structByteStride |
|--------------------------------------------------------|



 



| Elemento                                                                                                                                   | Descrizione                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                                         | \[\]nell'UAV.<br/>                            |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[in \] Dimensioni della struttura in byte.<br/> |



 

## <a name="remarks"></a>Commenti

*dstUAV* è un registro u dichiarato come riferimento a un oggetto UnorderedAccessView di un buffer strutturato con lo stride specificato che deve essere associato allo \# slot UAV \# nell'API.

Il contenuto della struttura non ha alcun tipo. Le operazioni eseguite sulla memoria possono interpretare implicitamente i dati come con un tipo .

*structByteStride* è la dimensione della struttura in byte nel buffer dichiarato. Il valore deve essere maggiore di zero. *structByteStride* è di tipo uint e deve essere un multiplo di 4.

Le istruzioni che fanno riferimento a un u strutturato accettano un indirizzo 2D, in cui il primo componente seleziona lo struct e il secondo componente seleziona l'offset all'interno \# \[ dello \] \[ struct, in byte \] allineati.

Il \_ flag glc significa "coerente a livello globale". L'assenza di glc significa che l'UAV viene dichiarato solo come "coerente con il gruppo" nel compute shader o "coerente localmente" in una singola chiamata \_ pixel shader chiamata.

Il \_ flag opc è il contatore di mantenimento dell'ordine. Indica che se un UAV è associato a uno slot (u ), deve \# essere stato creato con il flag \# COUNTER. Ciò significa che [le operazioni imm \_ atomic \_ alloc](imm-atomic-alloc--sm5---asm-.md) o [imm atomic \_ \_ consume](imm-atomic-consume--sm5---asm-.md) nello shader modificano un contatore i cui valori possono essere usati nello shader come riferimento permanente a una posizione nell'UAV. Non è possibile riordinare i dati dopo la fine dello shader.

L'assenza del flag opc significa che se lo shader usa \_ [istruzioni imm \_ atomic \_ alloc](imm-atomic-alloc--sm5---asm-.md) o [imm atomic \_ \_ consume](imm-atomic-consume--sm5---asm-.md) e un UAV è associato allo slot (u), deve essere stato creato con il flag APPEND, che fornisce un contatore che non garantisce che l'ordine sia mantenuto dopo la chiamata \# dello shader.

Se il flag opc è assente e lo shader non contiene istruzioni \_ [imm \_ atomic \_ alloc](imm-atomic-alloc--sm5---asm-.md) o [imm \_ atomic \_ consume,](imm-atomic-consume--sm5---asm-.md) è consentito creare un UAV associato allo slot (u) con il flag COUNTER (il contatore non verrà usato da questo shader), nessun flag (nessun contatore), ma non con il \# flag APPEND.

> [!Note]  
> cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supporta **dcl \_ tgsm \_ strutturato,** ma non [dcl \_ tgsm \_ raw.](dcl-tgsm-raw--sm5---asm-.md)

 

Questa istruzione si applica alle fasi di shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché gli UAV sono disponibili in tutte le fasi dello shader per Direct3D 11.1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11.1, disponibile a partire da Windows 8.



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



 

> [!Note]  
> Questa istruzione è supportata nei file cs \_ 4 \_ 0 e cs \_ 4 \_ 1.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





