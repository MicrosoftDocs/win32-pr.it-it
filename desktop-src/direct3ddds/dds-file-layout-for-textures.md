---
title: Esempio di trama DDS
description: Per una trama non compressa, usare i \_ flag DDSD pitch e DDPF \_ RGB. per una trama compressa, usare i \_ flag DDSD LINEARSIZE e DDPF \_ fourcc.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298364"
---
# <a name="dds-texture-example"></a>Esempio di trama DDS

Per una trama non compressa, usare i \_ flag DDSD pitch e DDPF \_ RGB. per una trama compressa, usare i \_ flag DDSD LINEARSIZE e DDPF \_ fourcc. Per una trama mipmap, usare i \_ flag complessi DDSD MIPMAPCOUNT, ddsCaps \_ MIPMAP e ddsCaps, oltre \_ al membro MIPMAP Count. Se vengono generati mipmap, tutti i livelli fino a 1 per 1 vengono in genere scritti.

Per una trama compressa, le dimensioni di ogni immagine a livello di mipmap sono in genere pari a un quarto della dimensione precedente, con un minimo di 8 (DXT1) o 16 (DXT2-5) byte (per le trame quadre). Utilizzare la formula seguente per calcolare le dimensioni di ogni livello per una trama non quadrata:


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



Questa tabella elenca la quantità di spazio occupata da ogni livello per una trama R8G8B8 256 per 256, senza usare la compressione.



| Componenti DDS          | \# Byte |
|-------------------------|----------|
| header                  | 128      |
| immagine principale 256 per 256   | 196608   |
| immagine mipmap 128 per 128 | 49152    |
| immagine mipmap 64 per 64   | 12288    |
| immagine mipmap 32 per 32   | 3072     |
| immagine mipmap 16 per 16   | 768      |
| immagine mipmap 8 per 8     | 192      |
| immagine mipmap 4 per 4     | 48       |
| immagine mipmap 2 per 2     | 12       |
| immagine mipmap 1 per 1     | 3        |



 

Questa tabella elenca la quantità di spazio occupata da ogni livello per la stessa trama usando la compressione (DXT1).



| Componenti DDS         | \# Byte |
|------------------------|----------|
| header                 | 128      |
| immagine principale 256 per 64   | 8192     |
| immagine mipmap 128 per 32 | 2048     |
| immagine mipmap 64 per 16  | 512      |
| immagine mipmap 32 per 8   | 128      |
| immagine mipmap 16 per 4   | 32       |
| immagine mipmap 8 per 2    | 16       |
| immagine di mipmap 4 per 1    | 8        |
| immagine mipmap 2 per 1    | 8        |
| immagine mipmap 1 per 1    | 8        |



 

Questa tabella elenca la quantità di spazio occupata da ogni livello per la stessa trama usando un formato di compressione DXGI (in questo caso BC3 \_ UNORM) che richiede pertanto l'intestazione estesa:



| Componenti DDS                                                | \# Byte |
|---------------------------------------------------------------|----------|
| Header (FourCC impostato su "DX10")                                 | 128      |
| intestazione estesa (formato DXGI impostato sul \_ formato DXGI \_ BC3 \_ UNORM) | 20       |
| immagine principale 256 per 64                                          | 16384    |
| immagine mipmap 128 per 32                                        | 4096     |
| immagine mipmap 64 per 16                                         | 1024     |
| immagine mipmap 32 per 8                                          | 256      |
| immagine mipmap 16 per 4                                          | 64       |
| immagine mipmap 8 per 2                                           | 32       |
| immagine di mipmap 4 per 1                                           | 16       |
| immagine mipmap 2 per 1                                           | 16       |
| immagine mipmap 1 per 1                                           | 16       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




