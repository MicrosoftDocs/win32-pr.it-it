---
title: Esempio di trama DDS
description: Per una trama non compressa, usare i flag DDSD PITCH e DDPF RGB. Per una trama compressa, usare i flag \_ \_ DDSD LINEARSIZE e \_ DDPF \_ FOURCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47fe1d7da71727c2c84bb3745772a10520367ac1cf6e9c4033932548d86c1302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289798"
---
# <a name="dds-texture-example"></a>Esempio di trama DDS

Per una trama non compressa, usare i flag DDSD PITCH e DDPF RGB. Per una trama compressa, usare i flag \_ \_ DDSD LINEARSIZE e \_ DDPF \_ FOURCC. Per una trama mipmapped, usare anche i flag DDSD \_ MIPMAPCOUNT, DDSCAPS \_ MIPMAP e DDSCAPS COMPLEX, nonché il membro \_ mipmap count. Se vengono generate mipmap, in genere vengono scritti tutti i livelli fino a 1 per 1.

Per una trama compressa, le dimensioni di ogni immagine a livello di mipmap sono in genere un quarto delle dimensioni della precedente, con un minimo di 8 (DXT1) o 16 (DXT2-5) byte (per trame quadrate). Usare la formula seguente per calcolare le dimensioni di ogni livello per una trama non quadrata:


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



Questa tabella elenca la quantità di spazio utilizzato da ogni livello per una trama R8G8B8 256 per 256, senza usare la compressione.



| Componenti DDS          | \# Byte |
|-------------------------|----------|
| header                  | 128      |
| Immagine principale 256 per 256   | 196608   |
| Immagine mipmap 128 per 128 | 49152    |
| Immagine mipmap 64 per 64   | 12288    |
| Immagine mipmap 32 per 32   | 3072     |
| Immagine mipmap 16 per 16   | 768      |
| Immagine mipmap 8 per 8     | 192      |
| Immagine mipmap 4 per 4     | 48       |
| Immagine mipmap 2 per 2     | 12       |
| Immagine mipmap 1 per 1     | 3        |



 

Questa tabella elenca la quantità di spazio utilizzato da ogni livello per la stessa trama usando la compressione (DXT1).



| Componenti DDS         | \# Byte |
|------------------------|----------|
| header                 | 128      |
| Immagine principale 256 per 64   | 8192     |
| Immagine mipmap 128 per 32 | 2048     |
| Immagine mipmap 64 per 16  | 512      |
| Immagine mipmap 32 per 8   | 128      |
| Immagine mipmap 16 per 4   | 32       |
| Immagine mipmap 8 per 2    | 16       |
| Immagine mipmap 4 per 1    | 8        |
| Immagine mipmap 2 per 1    | 8        |
| Immagine mipmap 1 per 1    | 8        |



 

Questa tabella elenca la quantità di spazio utilizzato da ogni livello per la stessa trama usando un formato di compressione DXGI (in questo caso BC3 UNORM) che richiede pertanto \_ l'intestazione estesa:



| Componenti DDS                                                | \# Byte |
|---------------------------------------------------------------|----------|
| header (FourCC impostato su "DX10")                                 | 128      |
| intestazione estesa (formato DXGI impostato su DXGI \_ FORMAT \_ BC3 \_ UNORM) | 20       |
| Immagine principale 256 per 64                                          | 16384    |
| Immagine mipmap 128 per 32                                        | 4096     |
| Immagine mipmap 64 per 16                                         | 1024     |
| Immagine mipmap 32 per 8                                          | 256      |
| Immagine mipmap 16 per 4                                          | 64       |
| Immagine mipmap 8 per 2                                           | 32       |
| Immagine mipmap 4 per 1                                           | 16       |
| Immagine mipmap 2 per 1                                           | 16       |
| Immagine mipmap 1 per 1                                           | 16       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori per DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




