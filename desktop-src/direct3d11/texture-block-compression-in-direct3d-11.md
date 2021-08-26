---
title: Compressione dei blocchi di trama in Direct3D 11
description: Il supporto della compressione a blocchi per le trame è stato esteso in Direct3D 11 per includere gli algoritmi BC6H e BC7.
ms.assetid: E0735D4E-9C0F-45DC-854A-C27EB8367D86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52c2c764c0f9dca4021dcb14187db67e697cd7155701294a9c6214b4543d00b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027801"
---
# <a name="texture-block-compression-in-direct3d-11"></a>Compressione dei blocchi di trama in Direct3D 11

Il supporto della compressione a blocchi per le trame è stato esteso in Direct3D 11 per includere gli algoritmi BC6H e BC7. BC6H supporta i dati di origine dei colori a intervalli dinamici elevati e BC7 offre una compressione di qualità migliore della media con meno artefatti per i dati di origine RGB standard.

Per informazioni più specifiche sul supporto dell'algoritmo di compressione a blocchi prima di Direct3D 11, incluso il supporto per i formati BC1 e BC5, vedere Compressione a blocchi [(Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)

**Nota sui formati di file:** I formati di compressione delle trame BC6H e BC7 usano il formato di file DDS per l'archiviazione dei dati di trama compressi. Per altre informazioni, vedere la [Guida alla programmazione per DDS.](/windows/desktop/direct3ddds/dx-graphics-dds-pguide)

## <a name="block-compression-formats-supported-in-direct3d-11"></a>Formati di compressione a blocchi supportati in Direct3D 11



| Dati di origine                                  | Risoluzione minima della compressione dei dati richiesta                              | Formato consigliato | Livello di funzionalità minimo supportato |
|----------------------------------------------|---------------------------------------------------------------------------|--------------------|---------------------------------|
| Colore a tre canali con canale alfa       | Tre canali di colore (5 bit:6 bit:5 bit), con 0 o 1 bit di alfa  | BC1                | Direct3D 9.1                    |
| Colore a tre canali con canale alfa       | Tre canali di colore (5 bit:6 bit:5 bit), con 4 bit di alfa         | RB2                | Direct3D 9.1                    |
| Colore a tre canali con canale alfa       | Tre canali di colore (5 bit:6 bit:5 bit) con 8 bit di alfa          | BC3                | Direct3D 9.1                    |
| Colore a un canale                            | Canale a un colore (8 bit)                                                | BC4                | Direct3D 10                     |
| Colore a due canali                            | Due canali di colore (8 bit:8 bit)                                        | BC5                | Direct3D 10                     |
| Colore HDR (High Dynamic Range) a tre canali | Tre canali di colore (16 bit:16 bit:16 bit) in virgola mobile "a metà"\* | BC6H               | Direct3D 11                     |
| Colore a tre canali, canale alfa facoltativo  | Tre canali di colore (da 4 a 7 bit per canale) con da 0 a 8 bit di alfa  | BC7                | Direct3D 11                     |



 

\*La virgola mobile "Half" è un valore a 16 bit costituito da un bit di segno facoltativo, un esponente distorto a 5 bit e una mantissa a 10 o 11 bit.

## <a name="bc1-bc2-and-b3-formats"></a>Formati BC1, BC2 e B3

I formati BC1, BC2 e BC3 sono equivalenti ai formati di compressione delle trame DXTn Direct3D 9 e corrispondono ai formati Direct3D 10 BC1, BC2 e BC3 corrispondenti. Il supporto per questi tre formati è richiesto da tutti i livelli di funzionalità (D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1, D3D \_ FEATURE LEVEL \_ \_ 9 \_ 2, D3D \_ FEATURE LEVEL \_ \_ 9 \_ 3, D3D \_ FEATURE LEVEL \_ \_ 10 \_ 0, D3D \_ FEATURE LEVEL \_ \_ 10 1 e \_ D3D \_ FEATURE LEVEL \_ \_ 11 \_ 0).



| Formato di compressione a blocchi | Formato DXGI                                                                           | Formato equivalente Direct3D 9                               | Byte per blocco di 4x4 pixel |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------|---------------------------|
| BC1                      | DXGI \_ FORMAT \_ BC1 \_ UNORM, DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC1 \_ TYPELESS | D3DFMT \_ DXT1, FourCC="DXT1"                                | 8                         |
| RB2                      | DXGI \_ FORMAT \_ BC2 \_ UNORM, DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC2 \_ TYPELESS | D3DFMT \_ DXT2, \* FourCC="DXT2", D3DFMT \_ DXT3, FourCC="DXT3" | 16                        |
| BC3                      | DXGI \_ FORMAT \_ BC3 \_ UNORM, DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC3 \_ TYPELESS | D3DFMT \_ DXT4, \* FourCC="DXT4", D3DFMT \_ DXT5, FourCC="DXT5" | 16                        |



 

\*Questi schemi di compressione (DXT2 e DXT4) non fanno distinzione tra i formati alfa pre-moltiplicati Direct3D 9 e i formati alfa standard. Questa distinzione deve essere gestita dagli shader programmabili in fase di rendering.

## <a name="bc4-and-bc5-formats"></a>Formati BC4 e BC5



| Formato di compressione a blocchi | Formato DXGI                                                                     | Formato equivalente Direct3D 9 | Byte per blocco di 4x4 pixel |
|--------------------------|---------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC4                      | DXGI \_ FORMAT \_ BC4 \_ UNORM, DXGI \_ FORMAT \_ BC4 \_ SNORM, DXGI \_ FORMAT \_ BC4 \_ TYPELESS | FourCC="ATI1"                | 8                         |
| BC5                      | DXGI \_ FORMAT \_ BC5 \_ UNORM, DXGI \_ FORMAT \_ BC5 \_ SNORM, DXGI \_ FORMAT \_ BC5 \_ TYPELESS | FourCC="ATI2"                | 16                        |



 

## <a name="bc6h-format"></a>Formato BC6H

Per informazioni più dettagliate su questo formato, vedere la documentazione [sul formato BC6H.](bc6h-format.md)



| Formato di compressione a blocchi | Formato DXGI                                                                      | Formato equivalente Direct3D 9 | Byte per blocco di 4x4 pixel |
|--------------------------|----------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC6H                     | FORMATO DXGI \_ \_ BC6H \_ UF16, FORMATO DXGI \_ \_ BC6H \_ SF16, FORMATO DXGI \_ \_ BC6H \_ SENZA TIPI | N/A                          | 16                        |



 

Il formato BC6H può selezionare modalità di codifica diverse per ogni blocco di 4x4 pixel. Sono disponibili in totale 14 diverse modalità di codifica, ognuna con compromessi leggermente diversi nella qualità visiva risultante della trama visualizzata. La scelta delle modalità consente la decodifica rapida da parte dell'hardware con il livello di qualità selezionato o adattato in base al contenuto di origine, ma aumenta notevolmente anche la complessità dello spazio di ricerca.

## <a name="bc7-format"></a>Formato BC7

Per informazioni più dettagliate su questo formato, vedere la documentazione [sul formato BC7.](bc7-format.md)



| Formato di compressione a blocchi | Formato DXGI                                                                           | Formato equivalente Direct3D 9 | Byte per blocco di 4x4 pixel |
|--------------------------|---------------------------------------------------------------------------------------|------------------------------|---------------------------|
| BC7                      | DXGI \_ FORMAT \_ BC7 \_ UNORM, DXGI \_ FORMAT \_ BC7 \_ UNORM \_ SRGB, DXGI \_ FORMAT \_ BC7 \_ TYPELESS | N/A                          | 16                        |



 

Il formato BC7 può selezionare modalità di codifica diverse per ogni blocco di 4x4 pixel. Sono disponibili in totale 8 diverse modalità di codifica, ognuna con compromessi leggermente diversi nella qualità visiva risultante della trama visualizzata. La scelta delle modalità consente la decodifica rapida da parte dell'hardware con il livello di qualità selezionato o adattato in base al contenuto di origine, ma aumenta notevolmente anche la complessità dello spazio di ricerca.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                 | Descrizione                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Formato BC6H](bc6h-format.md)<br/>                             | Il formato BC6H è un formato di compressione trame progettato per supportare spazi colori HDR (High Dynamic Range) nei dati di origine.<br/> |
| [Formato BC7](bc7-format.md)<br/>                               | Il formato BC7 è un formato di compressione trame usato per la compressione di alta qualità dei dati RGB e RGBA.<br/>                    |
| [Informazioni di riferimento sulla modalità formato BC7](bc7-format-mode-reference.md)<br/> | Questa documentazione contiene un elenco delle modalità a 8 blocchi e delle allocazioni di bit per i blocchi di formato di compressione trame BC7.<br/>    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compressione a blocchi (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> <dt>

[Trame](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

