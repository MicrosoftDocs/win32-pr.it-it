---
title: Eseguire il mapping tra le dichiarazioni D3D9 e D3D8
description: Questa tabella esegue il mapping dei membri di una dichiarazione D3DVERTEXELEMENT9 a una dichiarazione Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745551"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a>Eseguire il mapping tra le dichiarazioni D3D9 e D3D8

Questa tabella esegue il mapping dei membri di una Dichiarazione [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) a una dichiarazione Direct3D 8.



| Utilizzo di Direct3D 9           | Indice di utilizzo di Direct3D 9 | Direct3D 8            |
|----------------------------|------------------------|-----------------------|
| \_Posizione D3DDECLUSAGE     | 0                      | \_Posizione D3DVSDE     |
| \_Posizione D3DDECLUSAGE     | 1                      | \_POSITION2 D3DVSDE    |
| D3DDECLUSAGE \_ normale       | 0                      | D3DVSDE \_ normale       |
| D3DDECLUSAGE \_ normale       | 1                      | \_NORMAL2 D3DVSDE      |
| \_BLENDWEIGHT D3DDECLUSAGE  | 0                      | \_BLENDWEIGHT D3DVSDE  |
| \_BLENDINDICES D3DDECLUSAGE | 0                      | \_BLENDINDICES D3DVSDE |
| \_PSIZE D3DDECLUSAGE        | 0                      | \_PSIZE D3DVSDE        |
| \_Colore D3DDECLUSAGE        | 0                      | D3DVSDE \_ diffuse      |
| \_Colore D3DDECLUSAGE        | 1                      | D3DVSDE \_ speculare     |
| \_TEXCOORD D3DDECLUSAGE     | n                      | \_TEXCOORDN D3DVSDE    |



 

Quando si usa una dichiarazione con l'elaborazione dei vertici hardware in un driver Direct3D 7, il runtime di Direct3D lo converte in una FVF con le regole seguenti:

-   È necessario usare solo il flusso 0 (evidente dal limite MaxStreams).
-   L'ordine degli elementi Vertex deve essere uguale a quello di FVF bit.
-   Non sono consentiti gap nelle coordinate di trama.
-   Qualsiasi elemento Vertex non descritto la tabella non può essere convertito in un FVF valido per tutti i driver pre-DirectX 8 e, di conseguenza, non può essere usato in questi driver.
-   Solo D3DDECLTYPE \_ FLOAT2 è consentito per gli elementi Vertex con D3DDECLUSAGE \_ TEXCOORD se il dispositivo non imposta una delle \_ estremità D3DPTEXTURECAPS previste o \_ D3DPTEXTURECAPS mappa cubi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione vertici](vertex-declaration.md)
</dt> </dl>

 

 



