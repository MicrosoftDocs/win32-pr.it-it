---
description: Viene descritto come archiviare i dati di Windows Media in un file AVI.
ms.assetid: f2a9d9ff-4876-4f24-b96a-5d89e42fa3d5
title: Archiviazione di supporti compressi in file AVI (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080524a47b4295517d50705f6aeb125d085a8346
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351496"
---
# <a name="storing-compressed-media-in-avi-files-microsoft-media-foundation"></a>Archiviazione di supporti compressi in file AVI (Microsoft Media Foundation)

Tutti i contenuti compressi con i codec Windows Media Audio e video devono essere inseriti in un formato di contenitore. Uno dei formati più diffusi è il video audio interleave o AVI. È possibile usare Microsoft video for Windows (VfW) o Microsoft DirectShow per creare file AVI. Per ulteriori informazioni sull'utilizzo di video per Windows o DirectShow, consultare la documentazione del prodotto su MSDN.

I codec Windows Media Audio e video sono stati sviluppati per usare le proprietà del formato ASF (Advanced Systems Format), ovvero il contenitore usato da Windows Media. Poiché AVI e ASF archiviano il contenuto in modo diverso, si verificano alcune difficoltà quando si archivia il contenuto compresso con i codec Windows Media Audio e video in un file AVI.

I codec di Windows Media Audio comprimono il contenuto audio in modo tale che non possa essere decompresso correttamente senza timestamp per i singoli esempi. In questo modo è possibile ottimizzare i supporti compressi. Poiché il contenitore ASF mantiene i timestamp con tutti gli esempi, questa caratteristica degli algoritmi audio ha sempre funzionato correttamente.

I file AVI, tuttavia, non mantengono i timestamp con i campioni. Ciò significa che Windows Media Audio contenuto non può essere decompresso correttamente quando viene archiviato in un file AVI. Windows Media Video contenuto non presenta questa limitazione e può essere incluso nei file AVI. Per codificare Windows Media Video contenuto in un file AVI con audio sincronizzato, è necessario usare un altro codec audio.

L'altro problema relativo all'uso di un file AVI come contenitore per Windows Media riguarda i video a bassa velocità in bit. Uno dei modi in cui i codec di Windows Media Video producono contenuti video per velocità in bit ridotti è l'eliminazione di frame duplicati. Se si desidera inserire Windows Media Video contenuto in un file ASF, è necessario impostare il codificatore per il recapito di frame fittizi per i frame duplicati (impostare [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) su Variant \_ true) in modo che ogni frame sia rappresentato nel file. I frame fittizi prodotti dal codec hanno dimensioni pari a 8 byte. Tuttavia, il frame scritto nel file dal multiplexer AVI può essere di centinaia di byte più grande e riempito con dati casuali. Un file AVI creato in questo modo sarà ancora giocabile, ma sarà molto più grande del previsto. È possibile evitare questo problema usando velocità in bit maggiori durante la codifica del video per l'archiviazione nei file AVI.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



