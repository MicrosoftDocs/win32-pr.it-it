---
description: Buffer multimediali
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Buffer multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320776"
---
# <a name="media-buffers"></a>Buffer multimediali

Un buffer multimediale è un oggetto COM che gestisce un blocco di memoria, in genere per memorizzare i dati multimediali. I buffer multimediali vengono usati per spostare i dati da un componente della pipeline a quello successivo. La maggior parte delle applicazioni non usa direttamente i buffer multimediali, perché la sessione multimediale gestisce tutto il flusso di dati tra oggetti pipeline. È necessario utilizzare i buffer multimediali se si sta scrivendo un componente della pipeline personalizzato o se si utilizza direttamente un componente della pipeline senza la sessione multimediale.

Buffer multimediali espone l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . Questa interfaccia è progettata per la lettura o la scrittura di qualsiasi tipo di dati. I frame video non compressi richiedono una gestione speciale, perché possono essere archiviati in superfici Direct3D situate nella memoria video.

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                        | Descrizione                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [Uso dei buffer multimediali](working-with-media-buffers.md) | Descrive il comportamento generale dei buffer multimediali per tutti i tipi di supporto. |
| [Buffer video non compressi](uncompressed-video-buffers.md) | Come usare i buffer multimediali che contengono frame video non compressi.  |
| [Buffer della superficie DirectX](directx-surface-buffer.md)         | Viene descritto come archiviare una superficie Direct3D in un buffer multimediale.         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitive Media Foundation](media-foundation-primitives.md)
</dt> </dl>

 

 



