---
title: Mapping tra dichiarazioni D3D9 e D3D8
description: Questa tabella esegue il mapping dei membri di una dichiarazione D3DVERTEXELEMENT9 a una dichiarazione Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38e6c94836499a6f2bf5dc4e88c76b822ef3143278581a4020e76dba16c9869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069031"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a>Mapping tra dichiarazioni D3D9 e D3D8

Questa tabella esegue il mapping dei [**membri di una dichiarazione D3DVERTEXELEMENT9**](d3dvertexelement9.md) a una dichiarazione Direct3D 8.



| Utilizzo di Direct3D 9           | Indice di utilizzo Direct3D 9 | Direct3D 8            |
|----------------------------|------------------------|-----------------------|
| POSIZIONE D3DDECLUSAGE \_     | 0                      | POSIZIONE D3DVSDE \_     |
| POSIZIONE D3DDECLUSAGE \_     | 1                      | POSIZIONE D3DVSDE2 \_    |
| D3DDECLUSAGE \_ NORMAL       | 0                      | D3DVSDE \_ NORMAL       |
| D3DDECLUSAGE \_ NORMAL       | 1                      | D3DVSDE \_ NORMAL2      |
| D3DDECLUSAGE \_ BLENDWEIGHT  | 0                      | D3DVSDE \_ BLENDWEIGHT  |
| D3DDECLUSAGE \_ BLENDINDICES | 0                      | D3DVSDE \_ BLENDINDICES |
| D3DDECLUSAGE \_ PSIZE        | 0                      | D3DVSDE \_ PSIZE        |
| COLORE D3DDECLUSAGE \_        | 0                      | D3DVSDE \_ DIFFUSE      |
| COLORE D3DDECLUSAGE \_        | 1                      | SPECULARE D3DVSDE \_     |
| D3DDECLUSAGE \_ TEXCOORD     | n                      | D3DVSDE \_ TEXCOORDn    |



 

Quando una dichiarazione viene usata con l'elaborazione dei vertici hardware in un driver Direct3D 7, il runtime Direct3D la converte in FVF con le regole seguenti:

-   Deve essere usato solo il flusso 0 (evidente dal limite MaxStreams).
-   L'ordine degli elementi vertice deve essere uguale all'ordine dei bit FVF.
-   Gli spazi vuoti nelle coordinate della trama non sono consentiti.
-   Qualsiasi elemento vertice non descritto nella tabella non può essere convertito in un FVF valido per tutti i driver pre-DirectX 8 e, di conseguenza, non può essere usato in tali driver.
-   Solo D3DDECLTYPE FLOAT2 è consentito per gli elementi vertice con D3DDECLUSAGE TEXCOORD se il dispositivo non imposta uno dei limiti \_ \_ D3DPTEXTURECAPS PROJECTED o \_ D3DPTEXTURECAPS \_ CUBEMAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione dei vertici](vertex-declaration.md)
</dt> </dl>

 

 



