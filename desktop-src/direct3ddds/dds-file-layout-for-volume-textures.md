---
title: Esempio di trama del volume DDS
description: Per una trama del volume, usare il \_ complesso ddsCaps, DDSCAPS2 \_ volume, DDSD \_ Depth, Flags e set e dwDepth. Una trama del volume è un'estensione di una trama standard per Direct3D 9; è possibile definire una trama del volume con o senza mipmap.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298363"
---
# <a name="dds-volume-texture-example"></a>Esempio di trama del volume DDS

Per una trama del volume, usare il \_ complesso ddsCaps, DDSCAPS2 \_ volume, DDSD \_ Depth, Flags e set e dwDepth. Una trama del volume è un'estensione di una trama standard per Direct3D 9; è possibile definire una trama del volume con o senza mipmap.

Per i volumi senza mipmap, ogni sezione di profondità viene scritta nel file in ordine. Se sono inclusi mipmap, tutte le sezioni di profondità per un determinato livello di mipmap vengono scritte insieme, con ogni livello che contiene la metà di un numero di sezioni pari al livello precedente con un minimo di 1.

Ad esempio, una mappa del volume 64 per 64 per 4 usando un formato pixel di R8G8B8 (3 byte per pixel) con tutti i livelli di mipmap conterrà quanto segue:



| Componenti DDS                      | \# Byte    |
|-------------------------------------|-------------|
| header                              | 128 byte   |
| 64-by-64 sezione 1 di 4 immagine principale.   | 12288 byte |
| 64-by-64 sezione 2 di 4 immagine principale.   | 12288 byte |
| 64-by-64 sezione 3 di 4 immagine principale.   | 12288 byte |
| 64-by-64 sezione 4 di 4 immagine principale.   | 12288 byte |
| 32-by-32 Slice 1 di 2 mipmap image. | 3072 byte  |
| 32-by-32 Slice 2 of 2 mipmap image. | 3072 byte  |
| 16 per 16 sezione 1 di 1 immagine mipmap. | 768 byte   |
| 8-by-8 sezione 1 di 1 immagine mipmap.   | 192 byte   |
| 4 per 4 Slice 1 di 1 mipmap image.   | 48 byte    |
| 2-by-2 Slice 1 di 1 mipmap image.   | 12 byte    |
| 1-per-1 sezione 1 di 1 immagine mipmap.   | 3 byte     |



 

Si noti che il livello di mipmap più piccolo è di 3 byte perché bitCount è 24 e non è presente alcuna compressione aggiuntiva a questo livello.

In DirectX 8 è stato aggiunto il supporto per le trame del volume.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




