---
description: Descrive come archiviare i Windows multimediali in un file AVI.
ms.assetid: f2a9d9ff-4876-4f24-b96a-5d89e42fa3d5
title: Archiviazione di supporti compressi in file AVI (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d52c33f6ea01cd1a10572294eaf3ee57ab4423567e3b2cc1f0feb86e199707e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057726"
---
# <a name="storing-compressed-media-in-avi-files-microsoft-media-foundation"></a>Archiviazione di supporti compressi in file AVI (Microsoft Media Foundation)

Qualsiasi contenuto compresso usando i codec audio e video Windows deve essere inserito in un formato contenitore. Uno dei formati più diffusi è Audio Video Interleave o AVI. È possibile usare Microsoft Video for Windows (VfW) o Microsoft DirectShow per creare file AVI. Per altre informazioni sull'uso di Video per Windows o DirectShow, vedere la documentazione del prodotto in MSDN.

I codec Windows Audio e Video multimediali sono stati sviluppati per usare le proprietà di Advanced Systems Format (ASF), che è il contenitore usato da Windows Media. Poiché AVI e ASF archiviano il contenuto in modo diverso, si verificano alcune difficoltà quando si archivia il contenuto compresso con i codec audio e video di Windows In un file AVI.

I Windows codec Audio multimediali comprimeno il contenuto audio in modo che non possa essere decompresso correttamente senza timestamp per i singoli campioni. In questo modo viene abilitata un'ottimizzazione nei supporti compressi. Poiché il contenitore ASF mantiene i timestamp con tutti i campioni, questa caratteristica degli algoritmi audio ha sempre funzionato bene.

I file AVI, tuttavia, non mantengono i timestamp con gli esempi. Ciò significa che Windows contenuto audio multimediale non può essere decompresso correttamente se archiviato in un file AVI. Windows Il contenuto video multimediale non presenta questa limitazione e può essere incluso nei file AVI. Per codificare Windows contenuto video multimediale in un file AVI con audio sincronizzato, è necessario usare un altro codec audio.

L'altro problema relativo all'uso di un file AVI come contenitore per Windows media riguarda video a bassa velocità in bit. Uno dei modi in cui i codec Windows Media Video producono contenuto video per velocità in bit basse è l'eliminazione di fotogrammi duplicati. Se si vuole inserire contenuto di Windows Media Video in un file ASF, è necessario impostare il codificatore per distribuire fotogrammi fittizi per i fotogrammi duplicati (impostare [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) su VARIANT TRUE) in modo che ogni fotogramma sia rappresentato \_ nel file. I fotogrammi fittizi prodotti dal codec hanno una dimensione di 8 byte. Tuttavia, il frame scritto nel file dal multiplexer AVI può essere di centinaia di byte più grandi e riempito con dati casuali. Un file AVI creato in questo modo sarà comunque riproducibile, ma sarà molto più grande del previsto. È possibile evitare questo problema usando velocità in bit più elevate durante la codifica di video per l'archiviazione in file AVI.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



