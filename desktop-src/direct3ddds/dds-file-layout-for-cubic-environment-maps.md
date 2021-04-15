---
title: Esempio di mappa cubo DDS
description: Per le mappe di ambienti cubi, una o più facce di un cubo vengono scritte nel file, usando formati non compressi o compressi e tutti i visi devono avere le stesse dimensioni.
ms.assetid: a77234f6-ba10-40dd-902f-33e600384aa5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235749bc0cf95a2e2120f66f3bcfb8a46e158628
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515859"
---
# <a name="dds-cube-map-example"></a>Esempio di mappa cubo DDS

Per le mappe di ambienti cubi, una o più facce di un cubo vengono scritte nel file, usando formati non compressi o compressi e tutti i visi devono avere le stesse dimensioni. Per ogni viso può essere definito mipmap, anche se tutti i visi devono avere lo stesso numero di livelli di mipmap. Se un file contiene una mappa cubo, \_ è necessario impostare ddsCaps Complex, DDSCAPS2 \_ mappa cubi e uno o più DSCAPS2 \_ mappa cubi POSITIVEX \_ /y/z e/o DDSCAPS2 mappa cubi NEGATIVEX \_ \_ /y/z. I visi vengono scritti nell'ordine: positivo x, negativo x, positivo y, negativo y, positivo z, negativo z, con eventuali visi mancanti omessi. Ogni viso viene scritto con la relativa immagine principale, seguito da qualsiasi livello di mipmap.

Ad esempio, una mappa del cubo 256 per 256 con i visi positivi x, negativi y e positivi z, un formato pixel di DXT1 e tutti i livelli mipmap contengono quanto segue:



| Componenti DDS                                      | \# Byte |
|-----------------------------------------------------|----------|
| header                                              | 128      |
| immagine principale x positiva 256 per 256                    | 32768    |
| immagine x mipmap positivo 128 per 128                  | 8192     |
| immagine x mipmap positivo 64 per 64                    | 2048     |
| immagine x mipmap positivo 32 per 32                    | 512      |
| immagine mipmap x 16 per 16 positiva                    | 128      |
| immagine x mipmap positiva 8 per 8                      | 32       |
| immagine x mipmap positiva 4 per 4                      | 8        |
| immagine x mipmap positiva 2 per 2                      | 8        |
| immagine x mipmap positiva 1 per 1                      | 8        |
| Ripetere i 9 livelli precedenti per l'immagine mipmap y | 43704    |
| Ripetere i 9 livelli precedenti per l'immagine mipmap z | 43704    |



 

A partire da DirectX 8, una mappa cubo viene archiviata con tutti i visi definiti.

## <a name="dxgi-cube-maps"></a>DXGI Cube Maps

Le mappe di ambienti cubi in Direct3D 10. x e Direct3D 11 sono equivalenti a una matrice di trame 2D con 6 immagini e possono essere archiviate in file DDS come tali. Con Direct3D 10,1 e Direct3D 11, l'hardware può supportare anche matrici di CubeMaps, che sono a loro volta matrici di trame 2D con un multiplo di 6 immagini (6, 12, 18, 24 e così via).

Ad esempio, di seguito è riportato un mappa cubi 256 per 256 con livelli mipmap archiviati in un formato BC6H come matrice di trama 2D:



| Componenti DDS                                                                                                                                                                                                  | \# Byte |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| Header (FourCC di "DX10")                                                                                                                                                                                       | 128      |
| intestazione estesa (formato DXGI impostato su 95 \[ DXGI \_ formato \_ BC6H \_ UF16 \] , valore dimensione 3 \[ D3Dxx \_ dimensione risorsa \_ TEXTURE2D \_ \] , dimensione matrice di 6, flag varie della risorsa 0x4 \[ D3Dxx \_ \_ varie \_ TEXTURECUBE \] ) | 20       |
| 256-by-256 voce di matrice 0 (positivo x) immagine principale                                                                                                                                                                | 65536    |
| 128-by-128 voce di matrice 0 (positivo x) mipmap immagine                                                                                                                                                              | 16384    |
| 64-by-64 voce di matrice 0 (positivo x) mipmap immagine                                                                                                                                                                | 4096     |
| 32-by-32 voce di matrice 0 (positivo x) mipmap immagine                                                                                                                                                                | 1024     |
| voce di matrice di mipmap di 16 per 16 (x positivo)                                                                                                                                                                | 256      |
| voce di matrice 8 per 8 (0 (positivo x) mipmap immagine                                                                                                                                                                  | 64       |
| voce di matrice 4 per 4 (0 (positivo x) mipmap immagine                                                                                                                                                                  | 16       |
| 2-by-2 voce di matrice 0 (positivo x) mipmap immagine                                                                                                                                                                  | 16       |
| 1-per-1 voce di matrice 0 (positivo x) mipmap immagine                                                                                                                                                                  | 16       |
| Ripetere i 9 livelli precedenti per la voce della matrice mipmap immagine 1 (negativa x)                                                                                                                                        | 87408    |
| Ripetere i 9 livelli precedenti per la voce di matrice 2 (y positivo) mipmap immagine                                                                                                                                        | 87408    |
| Ripetere i 9 livelli precedenti per la voce di matrice 3 (y negativa) immagine mipmap                                                                                                                                        | 87408    |
| Ripetere i 9 livelli precedenti per la voce di matrice 4 (z positivo) mipmap immagine                                                                                                                                        | 87408    |
| Ripetere i 9 livelli precedenti per la voce di matrice 5 (negativo z) mipmap immagine                                                                                                                                        | 87408    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




