---
title: Esempio di mapping del cubo DDS
description: Per le mappe dell'ambiente cubico, uno o più visi di un cubo vengono scritti nel file usando formati non compressi o compressi e tutti i visi devono avere le stesse dimensioni.
ms.assetid: a77234f6-ba10-40dd-902f-33e600384aa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97a51526570a775eb0cff8ec5ed665ac3dc4b218a876743b29e983bd9c03e9ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289863"
---
# <a name="dds-cube-map-example"></a>Esempio di mapping del cubo DDS

Per le mappe dell'ambiente cubico, uno o più visi di un cubo vengono scritti nel file usando formati non compressi o compressi e tutti i visi devono avere le stesse dimensioni. Ogni viso può avere mipmap definiti, anche se tutti i visi devono avere lo stesso numero di livelli mipmap. Se un file contiene una mappa del cubo, È necessario impostare \_ DDSCAPS COMPLEX, DDSCAPS2 CUBEMAP e uno o più di \_ DSCAPS2 \_ CUBEMAP \_ POSITIVEX/Y/Z e/o DDSCAPS2 \_ CUBEMAP \_ NEGATIVEX/Y/Z. I visi vengono scritti nell'ordine: positivo x, x negativo, y positivo, y negativo, z positivo, z negativo, con tutti i visi mancanti omessi. Ogni viso viene scritto con l'immagine principale, seguita da qualsiasi livello mipmap.

Ad esempio, una mappa cubo 256 per 256 con visi x, y e z positivi positivi, un formato pixel di DXT1 e tutti i livelli mipmap conterrebbero quanto segue:



| Componenti DDS                                      | \# Byte |
|-----------------------------------------------------|----------|
| header                                              | 128      |
| 256 x 256 positivo x immagine principale                    | 32768    |
| Immagine x mipmap positiva 128 per 128                  | 8192     |
| Immagine mipmap positiva 64 per 64                    | 2048     |
| Immagine mipmap positiva 32 per 32                    | 512      |
| Immagine mipmap positiva 16 per 16                    | 128      |
| Immagine mipmap positiva 8 per 8                      | 32       |
| Immagine mipmap positiva 4 per 4                      | 8        |
| Immagine mipmap positiva 2 per 2                      | 8        |
| Immagine mipmap positiva 1 per 1                      | 8        |
| ripetere i 9 livelli precedenti per l'immagine mipmap y | 43704    |
| ripetere i 9 livelli precedenti per l'immagine z mipmap | 43704    |



 

A partire da DirectX 8, una mappa cubo viene archiviata con tutti i visi definiti.

## <a name="dxgi-cube-maps"></a>Cubo DXGI Mappe

Le mappe dell'ambiente cubico in Direct3D 10.x e Direct3D 11 sono equivalenti a una matrice di trame 2D con 6 immagini e possono essere archiviate in file DDS come tali. Con Direct3D 10.1 e Direct3D 11, l'hardware può supportare anche matrici di mappe cubi che sono a loro volta matrici di trame 2D con un multiplo di 6 immagini (6, 12, 18, 24 e così via).

Ad esempio, ecco una mappa cubo 256 per 256 con livelli mipmap archiviati in un formato BC6H come matrice di trame 2D:



| Componenti DDS                                                                                                                                                                                                  | \# Byte |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| header (FourCC di "DX10")                                                                                                                                                                                       | 128      |
| intestazione estesa (formato DXGI impostato su 95 \[ DXGI \_ FORMAT \_ BC6H UF16, valore della dimensione \_ di \] \[ 3 D3Dxx RESOURCE DIMENSION TEXTURE2D, dimensione della matrice pari a 6, flag misc di \_ 0x4 \_ \_ \] \[ D3Dxx \_ RESOURCE \_ MISC \_ TEXTURECUBE \] ) | 20       |
| Immagine principale 0 (x positiva) della voce di matrice 256 per 256                                                                                                                                                                | 65536    |
| 128 per 128 voce di matrice 0 (x positiva) immagine mipmap                                                                                                                                                              | 16384    |
| 64 per 64 voce di matrice 0 (x positiva) immagine mipmap                                                                                                                                                                | 4096     |
| 32-by-32 array entry 0 (positive x) mipmap image                                                                                                                                                                | 1024     |
| 16 per 16 voce di matrice 0 (x positiva) immagine mipmap                                                                                                                                                                | 256      |
| 8 per 8 voce di matrice 0 (x positiva) immagine mipmap                                                                                                                                                                  | 64       |
| 4 per 4 voce di matrice 0 (x positiva) immagine mipmap                                                                                                                                                                  | 16       |
| 2 per 2 voce di matrice 0 (x positiva) immagine mipmap                                                                                                                                                                  | 16       |
| 1 per 1 voce di matrice 0 (x positiva) immagine mipmap                                                                                                                                                                  | 16       |
| ripetere i 9 livelli precedenti per l'immagine mipmap della voce di matrice 1 (x negativa)                                                                                                                                        | 87408    |
| ripetere i 9 livelli precedenti per l'immagine mipmap della voce di matrice 2 (y positiva)                                                                                                                                        | 87408    |
| ripetere i 9 livelli precedenti per l'immagine mipmap della voce di matrice 3 (y negativa)                                                                                                                                        | 87408    |
| ripetere i 9 livelli precedenti per l'immagine mipmap della voce di matrice 4 (z positiva)                                                                                                                                        | 87408    |
| ripetere i 9 livelli precedenti per l'immagine mipmap della voce di matrice 5 (z negativa)                                                                                                                                        | 87408    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori per DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




