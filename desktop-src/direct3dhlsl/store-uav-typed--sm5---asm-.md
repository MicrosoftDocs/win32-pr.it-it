---
title: store_uav_typed (SM5-ASM)
description: Scrittura ad accesso casuale di un elemento in una visualizzazione di accesso non ordinato (UAV) tipizzata.
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046074"
---
# <a name="store_uav_typed-sm5---asm"></a>archivio \_ UAV \_ tipizzato (SM5-ASM)

Scrittura ad accesso casuale di un elemento in una visualizzazione di accesso non ordinato (UAV) tipizzata.



| archivio \_ UAV \_ tipizzato dstUAV. xyzw, dstAddress \[ . Swizzle \] , src0 \[ . Swizzle\] |
|-------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                 | \[in \] contiene il risultato dell'operazione.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[nell' \] indirizzo in cui scrivere.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[nei \] componenti da scrivere.<br/>              |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un elemento a \* 32 bit a 4 componenti scritto da *Src0* in *DstUAV* all'indirizzo in *dstAddress*. *dstUAV* è un UAV tipizzato (u \# ).

Il formato del UAV determina la conversione del formato.

Il numero di componenti Unsigned Integer a 32 bit presi dall'indirizzo è determinato dalla dimensionalità della risorsa dichiarata in *dstUAV*. Questo indirizzo si trova in elementi.

L'indirizzamento fuori limite indica che non viene scritto alcun elemento nella memoria.

*dstUAV* ha sempre una maschera di scrittura xyzw. È necessario scrivere tutti i componenti.

Non è valido e non è definito per usare questa istruzione in un UAV non dichiarato come tipizzato. Ovvero, l'operazione su un UAV strutturato o non di tipo non è valida.

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



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





