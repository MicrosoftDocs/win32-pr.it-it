---
description: Le mappe di trama sono immagini digitalizzate disegnate su forme tridimensionali per aggiungere dettagli visivi.
ms.assetid: 0ea5cb07-a21a-4e2c-93e2-54966153bb8a
title: Risorse di trama compresse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b7ef048c0e1780f92246a407863a4fa48a94a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225750"
---
# <a name="compressed-texture-resources-direct3d-9"></a>Risorse di trama compresse (Direct3D 9)

Le mappe di trama sono immagini digitalizzate disegnate su forme tridimensionali per aggiungere dettagli visivi. Viene eseguito il mapping a queste forme durante la rasterizzazione e il processo può utilizzare grandi quantità sia del bus di sistema che della memoria. Per ridurre la quantità di memoria utilizzata dalle trame, Direct3D supporta la compressione delle superfici della trama. Alcuni dispositivi Direct3D supportano le superfici di trama compresse in modo nativo. In tali dispositivi, quando è stata creata una superficie compressa in cui sono stati caricati i dati, la superficie può essere usata in Direct3D come qualsiasi altra superficie di trama. Direct3D gestisce la decompressione quando viene eseguito il mapping della trama a un oggetto 3D.

## <a name="storage-efficiency-and-texture-compression"></a>Efficienza di archiviazione e compressione della trama

Tutti i formati di compressione di trama sono potenze di due. Anche se ciò non significa che una trama è necessariamente quadrata, significa che sia x che y sono potenze di due. Se, ad esempio, una trama è originariamente 512 di 128 byte, il mapping MIP successivo sarà 256 per 64 e così via, con ogni livello che diminuisce di una potenza di due. Ai livelli inferiori, in cui la trama viene filtrata in base a 16 per 2 e 8 per 1, saranno presenti bit inutili perché il blocco di compressione è sempre un blocco 4 per 4 di Texel. Le parti inutilizzate del blocco vengono riempite. Sebbene siano presenti bit sprecati ai livelli più bassi, il miglioramento complessivo è ancora significativo. Il caso peggiore è, in teoria, una trama da 2K a 1 (2 ⁰ di alimentazione). In questo caso, viene codificata una sola riga di pixel per blocco, mentre il resto del blocco è inutilizzato.

## <a name="mixing-formats-within-a-single-texture"></a>Combinazione di formati all'interno di una singola trama

È importante notare che una singola trama deve specificare che i dati vengono archiviati come 64 o 128 bit per gruppo di 16 Texel. Se i blocchi a 64 bit, ovvero Format DXT1, vengono usati per la trama, è possibile combinare i formati alfa opachi e a 1 bit in base ai singoli blocchi all'interno della stessa trama. In altre parole, il confronto tra il Unsigned Integer Magnitude del colore \_ 0 e il colore \_ 1 viene eseguito in modo univoco per ogni blocco di 16 Texel.

Una volta usati i blocchi 128 bit, il canale alfa deve essere specificato in modo esplicito (format DXT2 e DXT3) o in modalità interpolata (format DXT4 e DXT5) per l'intera trama. Come con il colore, quando si seleziona la modalità interpolata (format DXT4 e DXT5), è possibile usare otto alfa interpolate o sei modalità alfa interpolate in base a blocchi. Anche in questo caso, il confronto di magnitude tra Alpha \_ 0 e Alpha \_ 1 viene eseguito in modo univoco in base a blocchi.

Direct3D fornisce servizi per comprimere le superfici usate per la texturing di modelli 3D. In questa sezione vengono fornite informazioni sulla creazione e la modifica dei dati in una superficie di trama compressa.

Le informazioni sono contenute negli argomenti seguenti.

-   [Trame alfa opache e a 1 bit (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Trame con canali alfa (Direct3D 9)](textures-with-alpha-channels.md)
-   [Formati di trama compressi (Direct3D 9)](compressed-texture-formats.md)
-   [Uso di trame compresse (Direct3D 9)](using-compressed-textures.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 



