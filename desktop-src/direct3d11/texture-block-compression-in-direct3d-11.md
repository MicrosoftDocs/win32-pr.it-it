---
title: Compressione dei blocchi di trama in Direct3D 11
description: Il supporto per la compressione dei blocchi (BC) per le trame è stato esteso in Direct3D 11 per includere gli algoritmi BC6H e BC7.
ms.assetid: E0735D4E-9C0F-45DC-854A-C27EB8367D86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f80a22c97c8a706a3825abfb4ac2b5133c1a9beb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117838"
---
# <a name="texture-block-compression-in-direct3d-11"></a>Compressione dei blocchi di trama in Direct3D 11

Il supporto per la compressione dei blocchi (BC) per le trame è stato esteso in Direct3D 11 per includere gli algoritmi BC6H e BC7. BC6H supporta i dati di origine dei colori con intervallo dinamico elevato e BC7 offre una compressione di qualità migliore rispetto alla media con meno elementi per i dati di origine RGB standard.

Per informazioni più specifiche sul supporto dell'algoritmo di compressione dei blocchi precedente a Direct3D 11, incluso il supporto per il BC1 tramite formati BC5, vedere [compressione dei blocchi (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).

**Nota sui formati di file:** I formati di compressione della trama BC6H e BC7 usano il formato di file DDS per archiviare i dati di trama compressi. Per ulteriori informazioni, vedere la [Guida alla programmazione per DDS](/windows/desktop/direct3ddds/dx-graphics-dds-pguide) per informazioni dettagliate.

## <a name="block-compression-formats-supported-in-direct3d-11"></a>Formati di compressione dei blocchi supportati in Direct3D 11



| Dati di origine                                  | Risoluzione minima della compressione dei dati richiesta                              | Formato consigliato | Livello di funzionalità minimo supportato |
|----------------------------------------------|---------------------------------------------------------------------------|--------------------|---------------------------------|
| Colore a tre canali con canale alfa       | Tre canali di colore (5 bit: 6 bit: 5 bit) con 0 o 1 bit di alfa  | BC1                | Direct3D 9,1                    |
| Colore a tre canali con canale alfa       | Tre canali di colore (5 bit: 6 bit: 5 bit) con 4 bit di alfa         | RB2                | Direct3D 9,1                    |
| Colore a tre canali con canale alfa       | Tre canali di colore (5 bit: 6 bit: 5 bit) con 8 bit di alfa          | BC3                | Direct3D 9,1                    |
| Colore di un canale                            | Un canale di colore (8 bit)                                                | BC4                | Direct3D 10                     |
| Colore a due canali                            | Due canali di colore (8 bit: 8 bit)                                        | BC5                | Direct3D 10                     |
| Colore HDR (High Dynamic Range) a tre canali | Tre canali di colore (16 bit: 16 bit: 16 bit) nel punto a virgola mobile "Half"\* | BC6H               | Direct3D 11                     |
| Colore a tre canali, canale alfa facoltativo  | Tre canali di colore (da 4 a 7 bit per canale) con 0 a 8 bit di alfa  | BC7                | Direct3D 11                     |



 

\*Il valore a virgola mobile "Half" è un valore a 16 bit costituito da un bit di segno facoltativo, da un esponente distorta a 5 bit e da un mantissa di 10 o 11 bit.

## <a name="bc1-bc2-and-b3-formats"></a>Formati BC1, BC2 e B3

I formati BC1, BC2 e BC3 sono equivalenti ai formati di compressione della trama Direct3D 9 DXTn e corrispondono ai formati Direct3D 10 BC1, BC2 e BC3 corrispondenti. Il supporto per questi tre formati è richiesto da tutti i livelli di funzionalità (D3D \_ feature \_ level \_ 9 \_ 1, D3D \_ funzionalità \_ level \_ 9 \_ 2, D3D \_ funzionalità \_ level \_ 9 \_ 3, D3D \_ funzionalità \_ level \_ 10 \_ 0, D3D \_ funzionalità \_ level \_ 10 \_ 1 e D3D \_ feature \_ level \_ 11 \_ 0).



| Formato di compressione dei blocchi | Formato DXGI                                                                           | Formato equivalente a Direct3D 9                               | Byte per blocco pixel 4x4 |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------|---------------------------|
| BC1                      | DXGI \_ Format \_ BC1 \_ UNORM, DXGI \_ Format \_ BC1 \_ UNORM \_ sRGB, DXGI \_ Format \_ \_ BC1 | D3DFMT \_ DXT1, FourCC = "DXT1"                                | 8                         |
| RB2                      | DXGI \_ Format \_ BC2 \_ UNORM, DXGI \_ Format \_ BC2 \_ UNORM \_ sRGB, DXGI \_ Format \_ \_ BC2 | D3DFMT \_ DXT2 \* , FourCC = "DXT2", D3DFMT \_ DXT3, FourCC = "DXT3" | 16                        |
| BC3                      | DXGI \_ Format \_ BC3 \_ UNORM, DXGI \_ Format \_ BC3 \_ UNORM \_ sRGB, DXGI \_ Format \_ \_ BC3 | D3DFMT \_ DXT4 \* , FourCC = "DXT4", D3DFMT \_ DXT5, FourCC = "DXT5" | 16                        |



 

\*Questi schemi di compressione (DXT2 e DXT4) non fanno distinzione tra i formati alfa pre-moltiplicati di Direct3D 9 e i formati Alpha standard. Questa distinzione deve essere gestita dagli shader programmabili in fase di rendering.

## <a name="bc4-and-bc5-formats"></a>Formati BC4 e BC5



| Formato di compressione dei blocchi | Formato DXGI                                                                     | Formato equivalente a Direct3D 9 | Byte per blocco pixel 4x4 |
|--------------------------|---------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC4                      | DXGI \_ Format \_ BC4 \_ UNORM, DXGI \_ Format \_ BC4 \_ russar, DXGI \_ Format \_ \_ BC4 | FourCC = "ATI1"                | 8                         |
| BC5                      | DXGI \_ Format \_ BC5 \_ UNORM, DXGI \_ Format \_ BC5 \_ russar, DXGI \_ Format \_ \_ BC5 | FourCC = "ATI2"                | 16                        |



 

## <a name="bc6h-format"></a>Formato BC6H

Per informazioni più dettagliate su questo formato, vedere la documentazione del [formato BC6H](bc6h-format.md) .



| Formato di compressione dei blocchi | Formato DXGI                                                                      | Formato equivalente a Direct3D 9 | Byte per blocco pixel 4x4 |
|--------------------------|----------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC6H                     | DXGI \_ Format \_ BC6H \_ UF16, DXGI \_ Format \_ BC6H SF16 \_ , DXGI \_ Format \_ \_ BC6H | N/D                          | 16                        |



 

Il formato BC6H può selezionare modalità di codifica diverse per ogni blocco di pixel 4x4. Sono disponibili 14 diverse modalità di codifica, ognuna con compromessi leggermente diversi nella qualità visiva risultante della trama visualizzata. La scelta delle modalità consente la decodifica rapida da parte dell'hardware con il livello di qualità selezionato o adattato in base al contenuto di origine, ma aumenta notevolmente anche la complessità dello spazio di ricerca.

## <a name="bc7-format"></a>Formato BC7

Per informazioni più dettagliate su questo formato, vedere la documentazione del [formato BC7](bc7-format.md) .



| Formato di compressione dei blocchi | Formato DXGI                                                                           | Formato equivalente a Direct3D 9 | Byte per blocco pixel 4x4 |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC7                      | DXGI \_ Format \_ BC7 \_ UNORM, DXGI \_ Format \_ BC7 \_ UNORM \_ sRGB, DXGI \_ Format \_ \_ BC7 | N/D                          | 16                        |



 

Il formato BC7 può selezionare modalità di codifica diverse per ogni blocco di pixel 4x4. Sono disponibili un totale di 8 diverse modalità di codifica, ognuna con compromessi leggermente diversi nella qualità visiva risultante della trama visualizzata. La scelta delle modalità consente la decodifica rapida da parte dell'hardware con il livello di qualità selezionato o adattato in base al contenuto di origine, ma aumenta notevolmente anche la complessità dello spazio di ricerca.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                 | Descrizione                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Formato BC6H](bc6h-format.md)<br/>                             | Il formato BC6H è un formato di compressione di trama progettato per supportare spazi dei colori HDR (High Dynamic Range) nei dati di origine.<br/> |
| [Formato BC7](bc7-format.md)<br/>                               | Il formato BC7 è un formato di compressione di trama usato per la compressione di alta qualità dei dati RGB e RGBA.<br/>                    |
| [Riferimento alla modalità di formattazione BC7](bc7-format-mode-reference.md)<br/> | Questa documentazione contiene un elenco delle 8 modalità di blocco e delle allocazioni di bit per i blocchi di formato della compressione di trama BC7.<br/>    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compressione dei blocchi (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> <dt>

[Trame](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

