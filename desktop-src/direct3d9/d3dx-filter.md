---
description: I flag seguenti vengono utilizzati per specificare i canali in una trama su cui operare.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128525de2e403c11239c300372b79bd8ee8c1277
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481308"
---
# <a name="d3dx_filter"></a>\_Filtro D3DX

I flag seguenti vengono utilizzati per specificare i canali in una trama su cui operare.



|                         |                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definire                | Descrizione                                                                                                                                                                                                 |
| \_Filtro D3DX \_ None      | Non verrà eseguita alcuna operazione di ridimensionamento o filtro. Si presuppone che i pixel all'esterno dei limiti dell'immagine di origine siano neri trasparenti.                                                                                 |
| \_Punto di filtro D3DX \_     | Ogni pixel di destinazione viene calcolato eseguendo il campionamento del pixel più vicino dall'immagine di origine.                                                                                                                     |
| \_Filtro D3DX \_ lineare    | Ogni pixel di destinazione viene calcolato eseguendo il campionamento dei quattro pixel più vicini dall'immagine di origine. Questo filtro funziona meglio quando la scala su entrambi gli assi è minore di due.                                          |
| \_Triangolo filtro \_ D3DX  | Ogni pixel nell'immagine di origine contribuisce ugualmente all'immagine di destinazione. Questo è il più lento dei filtri.                                                                                           |
| \_Casella filtro \_ D3DX       | Ogni pixel viene calcolato calcolando la media di una casella 2x2 (X2) di pixel dall'immagine di origine. Questo filtro funziona solo quando le dimensioni della destinazione sono la metà di quelle dell'origine, come nel caso di mipmap. |
| D3DX \_ filtro \_ mirror \_ U | I pixel al di fuori del bordo della trama sull'asse u devono essere speculari, non incapsulati.                                                                                                                           |
| \_Mirror del filtro D3DX \_ \_ V | I pixel al di fuori del bordo della trama sull'asse v devono essere rispecchiati, non incapsulati.                                                                                                                           |
| \_Mirror filtro \_ D3DX \_ W | I pixel al di fuori del bordo della trama sull'asse w devono essere speculari, non incapsulati.                                                                                                                           |
| \_Mirror del filtro D3DX \_    | Specificare questo flag equivale a specificare i flag D3DX Filter \_ mirror \_ \_ U, D3DX \_ Filter \_ mirror \_ V e D3DX \_ Filter \_ mirror \_ W.                                                                     |
| \_Dithering filtro D3DX \_    | L'immagine risultante deve essere retinata usando un algoritmo di dithering ordinato 4x4.                                                                                                                                  |
| \_Filtro D3DX \_ sRGB \_ in  | I dati di input sono nello spazio colore sRGB (gamma 2,2).                                                                                                                                                              |
| D3DX \_ filtro \_ sRGB in \_ uscita | I dati di output sono nello spazio colore sRGB (gamma 2,2).                                                                                                                                                         |
| D3DX \_ Filter \_ sRGB      | Equivale a specificare il \_ filtro \_ D3DX \_ sRGB \| nel \_ filtro \_ D3DX \_ .                                                                                                                                       |



 

Ogni filtro valido deve contenere esattamente uno dei flag seguenti: filtro D3DX \_ \_ None, punto di \_ filtro D3DX \_ , D3DX \_ filtro \_ lineare, \_ triangolo di filtro D3DX \_ o \_ casella filtro D3DX \_ . Inoltre, è possibile usare l'operatore OR per specificare zero o più dei flag facoltativi seguenti con un filtro valido: D3DX \_ Filter mirror \_ \_ U, D3DX \_ Filter \_ mirror \_ V, D3DX \_ Filter \_ mirror \_ W, D3DX \_ Filter \_ mirror, D3DX Filter \_ \_ spther, D3DX \_ Filter \_ sRGB \_ in, D3DX \_ Filter \_ sRGB \_ out o D3DX \_ Filter \_ sRGB.

Specificare \_ il valore predefinito di D3DX per questo parametro è in genere equivalente alla specifica del \_ \_ \| \_ dithering del filtro D3DX del triangolo di filtro D3DX \_ . Tuttavia, \_ il valore predefinito di D3DX può avere significati diversi, a seconda del metodo che usa il filtro. Ad esempio:

-   Quando si usa [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), l' \_ impostazione predefinita di D3DX viene mappata al \_ triangolo di filtro D3DX D3DX del \_ \| \_ filtro \_ .
-   Quando si usa [**D3DXFilterTexture**](d3dxfiltertexture.md), \_ il valore predefinito di D3DX viene mappato alla \_ casella di filtro D3DX \_ se le dimensioni della trama sono una potenza di due e la \_ casella di filtro D3DX \_ \| D3DX filtro di \_ \_ dithering.

Fare riferimento a ogni metodo per verificare le informazioni sulla modalità di \_ mapping del filtro predefinito di D3DX.

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |            |
|--------------------------|------------|
| Intestazione                   | d3dx9tex. h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



