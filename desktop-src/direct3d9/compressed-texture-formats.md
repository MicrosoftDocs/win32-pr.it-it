---
description: Questa sezione contiene informazioni sull'organizzazione interna dei formati di trama compressi.
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: Formati di trama compressi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748799"
---
# <a name="compressed-texture-formats-direct3d-9"></a>Formati di trama compressi (Direct3D 9)

Questa sezione contiene informazioni sull'organizzazione interna dei formati di trama compressi. Questi dettagli non sono necessari per usare le trame compresse, perché è possibile usare le funzioni D3DX per la conversione da e verso formati compressi. Tuttavia, queste informazioni sono utili se si desidera operare direttamente sui dati della superficie compressa.

Direct3D usa un formato di compressione che divide le mappe di trama in blocchi di Texel 4x4. Se la trama non contiene trasparenza, è opaca o se la trasparenza è specificata da un alfa a 1 bit, un blocco a 8 byte rappresenta il blocco mappa di trama. Se la mappa di trama contiene Texel trasparenti, usando un canale alfa, un blocco a 16 byte lo rappresenta.

-   [Trame alfa opache e a 1 bit (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Trame con canali alfa (Direct3D 9)](textures-with-alpha-channels.md)

Ogni singola trama deve specificare che i dati vengono archiviati come 64 o 128 bit per gruppo di 16 Texel. Se i blocchi a 64 bit, ovvero Format DXT1, vengono usati per la trama, è possibile combinare i formati alfa opachi e a 1 bit in base ai singoli blocchi all'interno della stessa trama. In altre parole, il confronto tra il Unsigned Integer Magnitude del colore \_ 0 e il colore \_ 1 viene eseguito in modo univoco per ogni blocco di 16 Texel.

Quando si utilizzano blocchi a 128 bit, il canale alfa deve essere specificato in modo esplicito (format DXT2 o DXT3) o in modalità interpolata (format DXT4 o DXT5) per l'intera trama. Come con il colore, quando si seleziona la modalità interpolata, è possibile usare otto Alpha interpolati o sei modalità alfa interpolate in base a blocchi. Anche in questo caso, il confronto di magnitude tra Alpha \_ 0 e Alpha \_ 1 viene eseguito in modo univoco in base a blocchi.

Il pitch per i formati DXTn è diverso da quello restituito in DirectX 7,0. Il pitch è ora misurato in byte (non in blocchi). Se, ad esempio, si dispone di una larghezza di 16, sarà presente un passo di quattro blocchi (4 \* 8 per DXT1, 4 \* 16 per DXT2-5).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse di trama compresse](compressed-texture-resources.md)
</dt> </dl>

 

 



