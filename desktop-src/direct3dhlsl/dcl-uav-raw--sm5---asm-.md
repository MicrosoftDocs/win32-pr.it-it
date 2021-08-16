---
title: dcl_uav_raw (sm5 - asm)
description: Dichiarare una visualizzazione di accesso non ordinato (UAV) per l'uso da parte di uno shader. | dcl_uav_raw (sm5 - asm)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b7af99a1747d23d6269ffc1b7199fb142277b46e73bfd822d31fd4b0fbf3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986691"
---
# <a name="dcl_uav_raw-sm5---asm"></a>dcl \_ uav \_ raw (sm5 - asm)

Dichiarare una visualizzazione di accesso non ordinato (UAV) per l'uso da parte di uno shader.



| dcl \_ uav \_ raw \[ \_ glc \] dstUAV |
|-------------------------------|



 



| Elemento                                                                                           | Descrizione                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[\]nell'UAV.<br/> |



 

## <a name="remarks"></a>Commenti

*dstUAV* è un registro u dichiarato come riferimento a UnorderedAccessView di un buffer, in cui il buffer viene visualizzato come una semplice matrice 1D di voci non tipizzate \# a 32 bit.

Le operazioni eseguite sulla memoria possono interpretare in modo implicito i dati come con un tipo.

Il \_ flag glc indica "globalmente coerente". L'assenza di glc indica che l'UAV viene dichiarato solo come "coerente del gruppo" nel compute shader o "coerente localmente" in una singola pixel shader \_ chiamata.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché gli UAV sono disponibili in tutte le fasi dello shader per Direct3D 11.1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11.1, disponibile a partire da Windows 8.



| Vertice | Scafo | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello shader 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

> [!Note]  
> Questa istruzione è supportata in cs \_ 4 \_ 0 e cs \_ 4 \_ 1.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly del modello shader 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





