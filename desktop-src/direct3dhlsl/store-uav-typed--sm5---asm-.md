---
title: store_uav_typed (sm5 - asm)
description: Scrittura ad accesso casuale di un elemento in una visualizzazione di accesso non ordinata tipiata.
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc190662ebab4629c92bba8fafbe75fe23704f8543c7eb9ceba53b9ab02b1029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508241"
---
# <a name="store_uav_typed-sm5---asm"></a>store \_ uav \_ typed (sm5 - asm)

Scrittura ad accesso casuale di un elemento in una visualizzazione di accesso non ordinata tipiata.



| store \_ uav \_ typed dstUAV.xyzw, dstAddress \[ .swizzle \] , src0 \[ .swizzle\] |
|-------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                 | \[in \] Contiene il risultato dell'operazione.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Indirizzo in cui scrivere.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Componenti da scrivere.<br/>              |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un elemento a 4 componenti a 32 bit scritto da \* *src0* a *dstUAV* all'indirizzo in *dstAddress*. *dstUAV* è un UAV tipiato (u \# ).

Il formato dell'UAV determina la conversione del formato.

Il numero di componenti di interi senza segno a 32 bit prelevati dall'indirizzo è determinato dalla dimensionalità della risorsa dichiarata in *dstUAV*. Questo indirizzo è in elementi .

L'indirizzamento fuori dai limiti indica che non viene scritto nulla in memoria.

*dstUAV* ha sempre una maschera di scrittura con estensione xyzw. Tutti i componenti devono essere scritti.

Non è valido e non è definito usare questa istruzione in un UAV non dichiarato come tipiato. Ciò significa che l'operazione in un UAV strutturato o senza tipo non è valida.

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



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





