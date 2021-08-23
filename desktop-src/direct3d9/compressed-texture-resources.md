---
description: Le mappe trame sono immagini digitalizzate disegnate su forme tridimensionali per aggiungere dettagli visivi.
ms.assetid: 0ea5cb07-a21a-4e2c-93e2-54966153bb8a
title: Risorse trame compresse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cd4e21dfd0e042f8d8d97fd8415529a2b4a5a952334df3e7f39ef8ae20a890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989281"
---
# <a name="compressed-texture-resources-direct3d-9"></a>Risorse trame compresse (Direct3D 9)

Le mappe trame sono immagini digitalizzate disegnate su forme tridimensionali per aggiungere dettagli visivi. Vengono mappati a queste forme durante la rasterizzazione e il processo può utilizzare grandi quantità di memoria e bus di sistema. Per ridurre la quantità di memoria utilizzata dalle trame, Direct3D supporta la compressione delle superfici di trama. Alcuni dispositivi Direct3D supportano le superfici di trama compresse in modo nativo. In tali dispositivi, dopo aver creato una superficie compressa e caricato i dati, la superficie può essere usata in Direct3D come qualsiasi altra superficie di trama. Direct3D gestisce la decompressione quando la trama viene mappata a un oggetto 3D.

## <a name="storage-efficiency-and-texture-compression"></a>Archiviazione Efficienza e compressione delle trame

Tutti i formati di compressione trame sono potenza di due. Anche se ciò non significa che una trama è necessariamente quadrata, significa che sia x che y sono potenze di due. Ad esempio, se una trama è originariamente di 512 per 128 byte, il mipmapping successivo sarà 256 per 64 e così via, con ogni livello che diminuisce di una potenza di due. Ai livelli inferiori, in cui la trama viene filtrata a 16 per 2 e 8 per 1, verranno sprecati bit perché il blocco di compressione è sempre un blocco 4 per 4 di texel. Le parti inutilizzate del blocco vengono riempite. Anche se ci sono bit sprecati ai livelli più bassi, il guadagno complessivo è ancora significativo. Il caso peggiore è, in teoria, una trama 2K per 1 (2⁰ potenza). In questo caso, viene codificata una sola riga di pixel per blocco, mentre il resto del blocco non viene usato.

## <a name="mixing-formats-within-a-single-texture"></a>Combinazione di formati all'interno di una singola trama

È importante notare che qualsiasi singola trama deve specificare che i dati vengono archiviati come 64 o 128 bit per gruppo di 16 texel. Se per la trama vengono usati blocchi a 64 bit, ad esempio il formato DXT1, è possibile combinare i formati alfa opachi e a 1 bit per blocco all'interno della stessa trama. In altre parole, il confronto tra la grandezza dell'intero senza segno di colore 0 e il colore 1 viene eseguito in modo univoco per ogni blocco di \_ \_ 16 texel.

Dopo aver usato i blocchi a 128 bit, il canale alfa deve essere specificato in modalità esplicita (formato DXT2 e DXT3) o interpolata (formato DXT4 e DXT5) per l'intera trama. Come per il colore, quando è selezionata la modalità interpolata (formato DXT4 e DXT5), è possibile usare otto alfa interpolati o sei modalità alfa interpolate per blocco. Anche in questo caso, il confronto di grandezza di alfa 0 e alfa 1 viene eseguito in modo univoco blocco \_ \_ per blocco.

Direct3D fornisce servizi per comprimere le superfici usate per la texturing di modelli 3D. In questa sezione vengono fornite informazioni sulla creazione e la modifica dei dati in una superficie di trama compressa.

Le informazioni sono contenute negli argomenti seguenti.

-   [Trame alfa opache e a 1 bit (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Trame con canali alfa (Direct3D 9)](textures-with-alpha-channels.md)
-   [Formati di trama compressa (Direct3D 9)](compressed-texture-formats.md)
-   [Uso di trame compresse (Direct3D 9)](using-compressed-textures.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 



