---
title: Come affiancare l'area di una risorsa affiancata
description: Quando si crea una risorsa affiancata, le dimensioni, le dimensioni degli elementi di formato e il numero di sezioni mipmap e/o matrici (se applicabile) determinano il numero di riquadri necessari per eseguire il backup dell'intera superficie di attacco.
ms.assetid: 834E317F-CFFD-460C-9F89-793081BA1853
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ae1bf4ad1ca308fb3c93a36c4b3478aabdb0f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993512"
---
# <a name="how-a-tiled-resources-area-is-tiled"></a>Come affiancare l'area di una risorsa affiancata

Quando si crea una risorsa affiancata, le dimensioni, le dimensioni degli elementi di formato e il numero di sezioni mipmap e/o matrici (se applicabile) determinano il numero di riquadri necessari per eseguire il backup dell'intera superficie di attacco. Il layout pixel/byte all'interno dei riquadri è determinato dall'implementazione di. Il numero di pixel che si adattano a un riquadro, a seconda della dimensione dell'elemento di formato, è fisso e identico se si usa un swizzle standard o meno.

Il numero di riquadri che verranno usati da una determinata dimensione della superficie e la larghezza dell'elemento di formato è ben definito e prevedibile in base alle tabelle delle sezioni seguenti. Per le risorse che contengono mipmap o casi in cui le dimensioni della superficie non compilano un riquadro, sono presenti alcuni vincoli e sono descritti in [compressione di mipmap](mipmap-packing.md).

Risorse affiancate diverse possono puntare a una memoria identica con formati diversi, purché le applicazioni non si basino sui risultati della scrittura nella memoria con un formato e la lettura con un'altra. Tuttavia, nelle circostanze vincolate, le applicazioni possono basarsi sui risultati della scrittura nella memoria con un formato e la lettura con un altro se i formati si trovano nella stessa famiglia di formati (ovvero hanno lo stesso formato padre senza tipo). Ad esempio, DXGI \_ Format \_ R8G8B8A8 \_ UNORM e DXGI \_ Format \_ R8G8B8A8 \_ uint sono compatibili tra loro, ma non con il \_ formato \_ DXGI \_ R16G16 UNORM. Un'applicazione deve corrispondere in modo conservativo a tutte le proprietà delle risorse per poter interpretare nuovamente i dati tra due trame, perché i modelli di riquadro sono molto conservativi. Ovviamente, tuttavia, il formato è più permissivo. I formati devono essere compatibili solo come illustrato in precedenza. Un'eccezione è rappresentata dal fatto che i dati di emorragia da un alias di formato a un altro sono ben definiti: se un riquadro contiene completamente 0 per tutti i relativi bit, tale riquadro può essere usato con qualsiasi formato che interpreti il contenuto della memoria come 0 (indipendentemente dal layout della memoria). Quindi, un riquadro può essere cancellato in 0x00 con il formato DXGI \_ formato \_ R8 \_ UNORM e quindi usato con un formato come dxgi \_ Format \_ R32G32 \_ float e sembrerebbe che il contenuto sia ancora (0,0 f, 0,0 f).

Il layout dei dati all'interno di un riquadro può dipendere dalle proprietà delle risorse, dalla sottorisorsa in cui risiede e dalla posizione della sezione all'interno della sottorisorsa. Le eccezioni principali sono illustrate sopra: i formati compatibili con altre proprietà delle risorse sono uguali e quando tutti i Texel sono dello stesso tipo.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                             | Descrizione                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Divisione in riquadri di sottorisorse Texture2D e Texture2DArray](texture2d-and-texture2darray-subresource-tiling.md)<br/> | In queste tabelle viene illustrato come affiancare le sottorisorse [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) . <br/>                                                                                                          |
| [Divisione in riquadri di sottorisorse Texture3D](texture3d-subresource-tiling.md)<br/>                                       | Questa tabella Mostra come affiancare le sottorisorse di [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) . <br/>                                                                                                                                                                            |
| [Divisione in riquadri di buffer](buffer-tiling.md)<br/>                                                                     | Una risorsa [buffer](overviews-direct3d-11-resources-buffers.md) è divisa in riquadri 64KB, con uno spazio vuoto nell'ultimo riquadro se la dimensione non è un multiplo di 64KB.<br/>                                                                                                  |
| [Compressione di mipmap](mipmap-packing.md)<br/>                                                                   | A seconda del [livello](tiled-resources-features-tiers.md) di supporto per le risorse affiancate, mipmap con determinate dimensioni non seguono le forme standard del riquadro e sono considerate tutte raggruppate tra loro in modo che sia opaco per l'applicazione. <br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di risorse affiancate](creating-tiled-resources.md)
</dt> </dl>

 

