---
title: ld_uav_typed (SM5-ASM)
description: Lettura ad accesso casuale di un elemento da una visualizzazione di accesso non ordinato (UAV) tipizzata.
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b22392c802378c094b443c8ff2f2282909bd1f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335535"
---
# <a name="ld_uav_typed-sm5---asm"></a>LD \_ UAV \_ tipizzato (SM5-ASM)

Lettura ad accesso casuale di un elemento da una visualizzazione di accesso non ordinato (UAV) tipizzata.



| LD \_ UAV \_ tipizzato dst0 \[ . mask \] , srcAddress \[ . Swizzle \] , srcUAV \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descrizione                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[nell' \] indirizzo dei risultati dell'operazione.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/> | \[in \] specifica l'indirizzo da cui leggere.<br/>          |
| <span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*<br/>                 | \[nell' \] origine da cui eseguire la lettura. <br/>                    |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue un elemento a 4 componenti letto da *srcUAV* in corrispondenza dell'indirizzo Unsigned Integer in *srcAddress*, convertito a 32 bit per componente in base al formato, quindi scritto in *dst0* nello shader.

*srcUAV* è un UAV (u \# ) dichiarato come tipizzato. Il tipo della risorsa associata, tuttavia, deve essere R32 \_ uint/Sint/float.

Il numero di componenti Unsigned Integer a 32 bit presi dall'indirizzo è determinato dalla dimensionalità della risorsa dichiarata in *srcUAV*. L'indirizzamento è identico a quello dell'istruzione [LD](ld--sm4---asm-.md) .

L'indirizzamento fuori limite equivale all'istruzione **LD** .

Il comportamento di questa istruzione è identico all'istruzione **LD** se viene chiamato come **LD dst0 \[ . mask \] , srcAddress \[ . Swizzle \] , srcUAV \[ . \] swizzle**

Non è valido e non è definito per usare questa istruzione in un UAV non dichiarato come tipizzato. Questa operazione su un UAV strutturato o non di tipo non è valida.

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



 

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV, SRV e TGSM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





