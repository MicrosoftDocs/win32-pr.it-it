---
description: Informazioni sui flag D3DX_FILTER usati per specificare i canali di una trama su cui operare, ad esempio D3DX_FILTER_TRIANGLE.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7580749eca2134f899356c4632d8171b147aa7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408224"
---
# <a name="d3dx_filter"></a>FILTRO D3DX \_

I flag seguenti vengono usati per specificare i canali in una trama su cui operare.



| \#Definire                | Descrizione                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FILTRO D3DX \_ \_ NESSUNO      | Non verrà fatto alcun ridimensionamento o filtro. Si presuppone che i pixel all'esterno dei limiti dell'immagine di origine siano di colore nero trasparente.                                                                                 |
| PUNTO DI FILTRO D3DX \_ \_     | Ogni pixel di destinazione viene calcolato tramite il campionamento del pixel più vicino dall'immagine di origine.                                                                                                                     |
| D3DX \_ FILTER \_ LINEAR    | Ogni pixel di destinazione viene calcolato tramite il campionamento dei quattro pixel più vicini dall'immagine di origine. Questo filtro funziona meglio quando la scala su entrambi gli assi è minore di due.                                          |
| TRIANGOLO FILTRO D3DX \_ \_  | Ogni pixel nell'immagine di origine contribuisce equamente all'immagine di destinazione. Questo è il più lento dei filtri.                                                                                           |
| CASELLA FILTRO \_ \_ D3DX       | Ogni pixel viene calcolato mediamente da una casella di 2x2(x2) di pixel dall'immagine di origine. Questo filtro funziona solo quando le dimensioni della destinazione sono metà di quelle dell'origine, come nel caso delle mipmap. |
| D3DX \_ FILTER \_ MIRROR \_ U | I pixel al di fuori del bordo della trama sull'asse u devono essere speculari, non di cui è stato eseguito il wrapping.                                                                                                                           |
| D3DX \_ FILTER \_ MIRROR \_ V | I pixel al di fuori del bordo della trama sull'asse v devono essere speculari, non di cui è stato eseguito il wrapping.                                                                                                                           |
| D3DX \_ FILTER \_ MIRROR \_ W | I pixel al di fuori del bordo della trama sull'asse w devono essere speculari, non di cui è stato eseguito il wrapping.                                                                                                                           |
| D3DX \_ FILTER \_ MIRROR    | L'impostazione di questo flag è uguale a quando si specificano i flag D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V e \_ \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.                                                                     |
| DITHERING \_ FILTRO \_ D3DX    | L'immagine risultante deve essere dithering usando un algoritmo dithering ordinato 4x4.                                                                                                                                  |
| D3DX \_ FILTER \_ SRGB \_ IN  | I dati di input si trova nello spazio colore sRGB (gamma 2.2).                                                                                                                                                              |
| FILTRO D3DX \_ \_ SRGB \_ OUT | I dati di output sono nello spazio colore sRGB (gamma 2.2).                                                                                                                                                         |
| D3DX \_ FILTER \_ SRGB      | Come specificare D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT.                                                                                                                                       |



 

Ogni filtro valido deve contenere esattamente uno dei flag seguenti: D3DX \_ FILTER \_ NONE, D3DX \_ FILTER \_ POINT, D3DX \_ FILTER \_ LINEAR, D3DX FILTER TRIANGLE o \_ \_ D3DX \_ FILTER \_ BOX. È anche possibile usare l'operatore OR per specificare zero o più dei flag facoltativi seguenti con un filtro valido: D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR \_ \_ V, D3DX \_ FILTER MIRROR \_ \_ W, \_ \_ D3DX FILTER MIRROR, D3DX \_ FILTER \_ DITHER, D3DX \_ FILTER \_ SRGB \_ IN, D3DX \_ FILTER SRGB OUT o \_ \_ D3DX \_ FILTER \_ SRGB.

Specificare D3DX DEFAULT per questo parametro equivale in genere a specificare \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER. Tuttavia, D3DX \_ DEFAULT può avere significati diversi, a seconda del metodo che usa il filtro. Ad esempio:

-   Quando si [**usa D3DXCreateTextureFromFileEx,**](d3dxcreatetexturefromfileex.md)D3DX DEFAULT esegue il mapping a \_ D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHER.
-   Quando si usa [**D3DXFilterTexture,**](d3dxfiltertexture.md)D3DX DEFAULT esegue il mapping a D3DX FILTER BOX se le dimensioni della trama sono due e \_ \_ \_ D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER DITHER \_ in caso contrario.

Fare riferimento a ogni metodo per verificare la modalità di mapping del filtro D3DX \_ DEFAULT.

## <a name="constant-information"></a>Informazioni costanti



| Requisito                         | Valore           |
|--------------------------|------------|
| Intestazione                   | d3dx9tex.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



