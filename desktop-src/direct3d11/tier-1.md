---
title: Livello 1
description: In questa sezione viene descritto il supporto di livello 1.
ms.assetid: 8E2907D2-EFCB-4F97-9B40-6835A65D3DE5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4111fa48dafa7f38a26d5ca09f95898eacef6f55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729946"
---
# <a name="tier-1"></a>Livello 1

In questa sezione viene descritto il supporto di livello 1.

-   Hardware a livello di funzionalità minimo 11,0.
-   Nessun supporto per l'Unione.
-   Nessun supporto Texture1D o Texture3D.
-   Nessun 2, 8 o 16 supporto per l'anti-aliasing di campionamento (MSAA). È necessario solo il 4x, eccetto i formati 128 BPP.
-   Nessun modello swizzle standard (il layout all'interno dei riquadri 64KB e la compressione Tail MIP spetta al fornitore dell'hardware).
-   Limitazioni relative al modo in cui è possibile accedere ai riquadri quando sono presenti mapping duplicati, descritti in limitazioni di accesso ai riquadri [con mapping duplicati](tile-access-limitations-with-duplicate-mappings-.md).

### <a name="limitations-affecting-tier-1-only"></a>Limitazioni che interessano solo il livello 1

-   Le risorse affiancate possono avere mapping **null** , ma la lettura o la scrittura in essi genera risultati non definiti, incluso il dispositivo rimosso. Le applicazioni possono aggirare questo problema eseguendo il mapping di una singola pagina fittizia a tutte le aree vuote. Prestare attenzione se si scrive e si esegue il rendering in una pagina mappata a più percorsi di destinazione di rendering perché l'ordine delle Scritture non sarà definito.
-   Le istruzioni dello shader per la chiusura di LOD e il feedback dello stato mappato non sono disponibili. Per altre informazioni, vedere [esposizione di risorse affiancate HLSL](hlsl-tiled-resources-exposure.md).
-   Vincoli di allineamento per le forme dei riquadri standard: è garantito solo che MIPS (a partire dal Finest) le cui dimensioni siano tutti multipli delle dimensioni standard del riquadro supportano le forme standard del riquadro e possono avere singoli riquadri mappati/non mappati. Il primo mipmap in una risorsa affiancata con una dimensione diversa da un multiplo delle dimensioni standard del riquadro, insieme a tutti i mipmap più grossolani, può avere una forma di affiancamento non standard, adattabile a N riquadri 64KB per questo set di MIPS contemporaneamente (N segnalato all'applicazione). Questi N riquadri sono considerati compressi come un'unità, che deve essere completamente mappata o completamente senza mapping da parte dell'applicazione in un determinato momento, sebbene i mapping di ognuno dei due riquadri possano trovarsi in posizioni arbitrariamente non contigue in un pool di sezioni.
-   Le risorse affiancate con qualsiasi mipmap non un multiplo di dimensioni del riquadro standard in tutte le dimensioni non possono avere una dimensione della matrice maggiore di 1.
-   Per passare tra i riquadri di riferimento in un pool di sezioni tramite una risorsa [buffer](overviews-direct3d-11-resources-buffers.md) per fare riferimento agli stessi riquadri tramite una risorsa di [trama](overviews-direct3d-11-resources-textures.md) o viceversa, la chiamata più recente a [**UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) o [**CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) che definisce i mapping a tali riquadri del pool di sezioni deve essere per la stessa dimensione di risorsa (buffer e trama \* ) della dimensione della risorsa che verrà usata per accedere ai riquadri. In caso contrario, il comportamento non è definito, inclusa la possibilità di reimpostazione del dispositivo. Quindi, ad esempio, chiamando **UpdateTileMappings** per definire i mapping dei riquadri per un buffer, quindi **UpdateTileMappings** agli stessi riquadri nel pool di sezioni tramite una risorsa [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) , l'accesso ai riquadri tramite il buffer non è valido. Le operazioni di tipo soluzione alternativa ridefiniscono i mapping dei riquadri per una risorsa quando si passa da un buffer a un altro o viceversa, ovvero si condividono i riquadri o non si condividono mai i riquadri in un pool di sezioni tra le risorse del buffer e le risorse di trama.
-   Il filtro di riduzione min/max non è supportato. Per informazioni sul filtro di riduzione min/max, vedere [funzionalità di campionamento delle trame delle risorse affiancate](tiled-resources-texture-sampling-features.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Livelli di funzionalità delle risorse affiancate](tiled-resources-features-tiers.md)
</dt> </dl>

 

 