---
title: Come viene affiancata l'area di una risorsa affiancata
description: Quando si crea una risorsa affiancata, le dimensioni, le dimensioni dell'elemento di formato e il numero di mipmap e/o sezioni di matrice (se applicabile) determinano il numero di riquadri necessari per eseguire il backup dell'intera superficie di attacco.
ms.assetid: 834E317F-CFFD-460C-9F89-793081BA1853
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75feaa7852a7bc2567d7b4983ff4d59d12b516f5feb4be2886f93294f77bd6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633221"
---
# <a name="how-a-tiled-resources-area-is-tiled"></a>Come viene affiancata l'area di una risorsa affiancata

Quando si crea una risorsa affiancata, le dimensioni, le dimensioni dell'elemento di formato e il numero di mipmap e/o sezioni di matrice (se applicabile) determinano il numero di riquadri necessari per eseguire il backup dell'intera superficie di attacco. Il layout pixel/byte all'interno dei riquadri è determinato dall'implementazione. Il numero di pixel che rientrano in un riquadro, a seconda delle dimensioni dell'elemento di formato, è fisso e identico indipendentemente dal fatto che si usi o meno uno swizzle standard.

Il numero di riquadri che verranno usati da una determinata dimensione della superficie e dalla larghezza dell'elemento di formato è ben definito e prevedibile in base alle tabelle nelle sezioni seguenti. Per le risorse che contengono mipmap o casi in cui le dimensioni della superficie non riempiono un riquadro, esistono alcuni vincoli e vengono illustrati in [Mipmap packing](mipmap-packing.md).

Risorse affiancate diverse possono puntare a memoria identica con formati diversi, purché le applicazioni non si basano sui risultati della scrittura in memoria con un formato e della lettura con un altro. In circostanze vincolate, tuttavia, le applicazioni possono basarsi sui risultati della scrittura in memoria con un formato e della lettura con un altro se i formati sono nella stessa famiglia di formati, ovvero hanno lo stesso formato padre senza tipi. Ad esempio, DXGI \_ FORMAT \_ R8G8B8A8 UNORM e DXGI FORMAT R8G8B8A8 UINT sono compatibili tra loro ma non con \_ \_ \_ \_ DXGI \_ FORMAT \_ R16G16 \_ UNORM. Un'applicazione deve corrispondere in modo conservativo a tutte le proprietà delle risorse per poter reinterpretare i dati tra due trame poiché i modelli di riquadro sono molto conservativi indefiniti. Ovviamente, tuttavia, il formato è più lax. I formati devono essere compatibili solo come illustrato in precedenza. Un'eccezione è il caso in cui i dati disagiati da un alias di formato a un altro sono ben definiti: se un riquadro contiene completamente 0 per tutti i bit, tale riquadro può essere usato con qualsiasi formato che interpreta il contenuto della memoria come 0 (indipendentemente dal layout della memoria). Pertanto, un riquadro potrebbe essere cancellato per 0x00 con il formato DXGI FORMAT R8 UNORM e quindi usato con un formato come DXGI FORMAT R32G32 FLOAT e sembra che il contenuto sia ancora \_ \_ \_ \_ \_ \_ (0.0f,0.0f).

Il layout dei dati all'interno di un riquadro può dipendere dalle proprietà delle risorse, dalla sottorisorsa in cui si trova e dalla posizione del riquadro all'interno della sottorisorsa. Le eccezioni principali sono illustrate in precedenza: formati compatibili con altre proprietà delle risorse uguali e quando tutti i texel hanno lo stesso modello.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                             | Descrizione                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Divisione in riquadri di sottorisorse Texture2D e Texture2DArray](texture2d-and-texture2darray-subresource-tiling.md)<br/> | Queste tabelle illustrano come vengono affiancate le sottorisorse [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray.**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) <br/>                                                                                                          |
| [Divisione in riquadri di sottorisorse Texture3D](texture3d-subresource-tiling.md)<br/>                                       | Questa tabella illustra come vengono affiancate le sottorisorse [**Texture3D.**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) <br/>                                                                                                                                                                            |
| [Divisione in riquadri di buffer](buffer-tiling.md)<br/>                                                                     | Una [risorsa buffer](overviews-direct3d-11-resources-buffers.md) è suddivisa in riquadri da 64 KB, con spazio vuoto nell'ultimo riquadro se le dimensioni non sono un multiplo di 64 KB.<br/>                                                                                                  |
| [Compressione di mipmap](mipmap-packing.md)<br/>                                                                   | A seconda [](tiled-resources-features-tiers.md) del livello di supporto delle risorse affiancate, le mipmap con determinate dimensioni non seguono le forme riquadro standard e vengono considerate tutte impacchetto insieme in modo opaco per l'applicazione. <br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di risorse affiancate](creating-tiled-resources.md)
</dt> </dl>

 

