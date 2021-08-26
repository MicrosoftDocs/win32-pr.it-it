---
title: ld_uav_typed (sm5 - asm)
description: Lettura ad accesso casuale di un elemento da una visualizzazione di accesso non ordinata tipiata.
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9685341f4a3a2e6b22bbbcc4b36f6ecccc153f17c67f38c390e6beeef94358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982071"
---
# <a name="ld_uav_typed-sm5---asm"></a>ld \_ uav \_ typed (sm5 - asm)

Lettura ad accesso casuale di un elemento da una visualizzazione di accesso non ordinata tipiata.



| ld \_ uav \_ typed dst0 \[ .mask \] , srcAddress \[ .swizzle \] , srcUAV \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] Indirizzo dei risultati dell'operazione.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/> | \[in \] Specifica l'indirizzo da cui leggere.<br/>          |
| <span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*<br/>                 | \[in \] Origine da cui leggere. <br/>                    |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un elemento a 4 componenti letto da *srcUAV* in corrispondenza dell'indirizzo intero senza segno in *srcAddress*, convertito a 32 bit per componente in base al formato e quindi scritto in *dst0* nello shader.

*srcUAV* è un UAV (u \# ) dichiarato come tipiato. Tuttavia, il tipo della risorsa associata deve essere R32 \_ UINT/SINT/FLOAT.

Il numero di componenti di interi senza segno a 32 bit prelevati dall'indirizzo è determinato dalla dimensionalità della risorsa dichiarata in *srcUAV.* L'indirizzamento è uguale [all'istruzione ld.](ld--sm4---asm-.md)

L'indirizzamento fuori dai limiti è uguale **all'istruzione ld.**

Il comportamento di questa istruzione è identico all'istruzione **ld** se chiamata come **ld dst0 \[ .mask \] , srcAddress \[ .swizzle \] , srcUAV \[ .swizzle \]**

Non è valido e non è definito usare questa istruzione in un UAV non dichiarato come tipiato. Questa operazione in un UAV strutturato o senza tipo non è valida.

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



 

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV, SRV e TGSM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (HLSL DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





