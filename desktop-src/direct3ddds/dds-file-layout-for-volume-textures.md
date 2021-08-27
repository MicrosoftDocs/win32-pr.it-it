---
title: Esempio di trama del volume DDS
description: Per una trama di volume, usare DDSCAPS \_ COMPLEX, DDSCAPS2 \_ VOLUME, DDSD \_ DEPTH, flags e set e dwDepth. Una trama di volume è un'estensione di una trama standard per Direct3D 9; Una trama del volume può essere definita con o senza mipmap.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79501ea3ffa6f4a660f4ab3b248fedbdc7df17bf8af94520cad5808c3c611fd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025741"
---
# <a name="dds-volume-texture-example"></a>Esempio di trama del volume DDS

Per una trama di volume, usare DDSCAPS \_ COMPLEX, DDSCAPS2 \_ VOLUME, DDSD \_ DEPTH, flags e set e dwDepth. Una trama di volume è un'estensione di una trama standard per Direct3D 9; Una trama del volume può essere definita con o senza mipmap.

Per i volumi senza mipmap, ogni sezione di profondità viene scritta nel file nell'ordine indicato. Se sono incluse mipmap, tutte le sezioni di profondità per un determinato livello di mipmap vengono scritte insieme, con ogni livello che contiene la metà del numero di sezioni del livello precedente con un minimo di 1.

Ad esempio, una mappa di volume 64 per 64 per 4 che usa un formato pixel R8G8B8 (3 byte per pixel) con tutti i livelli di mipmap conterrà quanto segue:



| Componenti DDS                      | \# Byte    |
|-------------------------------------|-------------|
| header                              | 128 byte   |
| Sezione 1 64 per 64 di 4 immagini principali.   | 12288 byte |
| Sezione 2 64 per 64 di 4 immagini principali.   | 12288 byte |
| Sezione 3 di 4 immagini principali 64 per 64.   | 12288 byte |
| Sezione 4 di 4 immagini principali 64 per 64.   | 12288 byte |
| 32 per 32 sezione 1 di 2 immagini mipmap. | 3072 byte  |
| 32 per 32 sezione 2 di 2 immagini mipmap. | 3072 byte  |
| 16 per 16 sezione 1 di 1 immagine mipmap. | 768 byte   |
| Sezione 1 di 1 immagine mipmap 8 per 8.   | 192 byte   |
| 4 per 4 sezione 1 di 1 immagine mipmap.   | 48 byte    |
| 2 per 2 sezione 1 di 1 immagine mipmap.   | 12 byte    |
| 1-by-1 sezione 1 di 1 immagine mipmap.   | 3 byte     |



 

Si noti che il livello di mipmap più piccolo è di soli 3 byte perché il numero di bit è 24 e non esiste alcuna compressione aggiunta a questo livello.

Il supporto per le trame di volume è stato aggiunto in DirectX 8.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di programmazione per DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




