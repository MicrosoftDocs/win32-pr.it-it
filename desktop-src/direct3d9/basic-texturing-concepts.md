---
description: Le prime immagini 3D generate dal computer, sebbene in genere avanzate per il loro tempo, tendono a avere un aspetto lucido in plastica.
ms.assetid: 548ae140-c746-4fab-8000-421289d4f0a2
title: Concetti di base sulla trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8c4971f70cbe5b7b371f71191de6edb4c2be46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305112"
---
# <a name="basic-texturing-concepts-direct3d-9"></a>Concetti di base sulla trama (Direct3D 9)

Le prime immagini 3D generate dal computer, sebbene in genere avanzate per il loro tempo, tendono a avere un aspetto lucido in plastica. Hanno mancato i tipi di contrassegno, ad esempio graffi, crepe, impronte digitali e sbavature, che offrono agli oggetti 3D complessità visiva realistica. Negli ultimi anni, le trame hanno acquisito popolarità tra gli sviluppatori come uno strumento per migliorare il realismo delle immagini 3D generate dal computer.

Nell'uso quotidiano, la trama della parola si riferisce alla fluidità o alla rugosità di un oggetto. In grafica computer, tuttavia, una trama è una bitmap di colori pixel che assegna a un oggetto l'aspetto della trama.

Poiché le trame Direct3D sono bitmap, qualsiasi bitmap può essere applicata a una primitiva Direct3D. Ad esempio, le applicazioni possono creare e modificare gli oggetti che sembrano avere un modello di grana a legna. È possibile applicare erba, sporcizia e rocce a un set di primitive 3D che formano una collina. Il risultato è un Hillside di aspetto realistico. È anche possibile usare il texturing per creare effetti quali i segni lungo una strada, gli strati rocciosi in una scogliera o l'aspetto del marmo in un piano.

Inoltre, Direct3D supporta tecniche di texturing più avanzate, ad esempio la combinazione di trame, con o senza la trasparenza e il mapping chiaro. Per altre informazioni, vedere [blending di trame (Direct3D 9)](texture-blending.md) e [mapping chiaro con trame (Direct3D 9)](light-mapping-with-textures.md).

Se l'applicazione crea un dispositivo HAL (Hardware Abstraction Layer) o un dispositivo software, può usare trame 8, 16, 24, 32, 64 o 128 bit.

Informazioni aggiuntive sono contenute negli argomenti seguenti.

-   [Modalità di indirizzamento delle trame (Direct3D 9)](texture-addressing-modes.md)
-   [Aree dirty texture (Direct3D 9)](texture-dirty-regions.md)
-   [Tavolozze delle trame (Direct3D 9)](texture-palettes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 



