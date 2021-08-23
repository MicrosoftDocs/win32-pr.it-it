---
description: Buffer multimediali
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Buffer multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef02570ab994f0a15a9b53f2df8a0ac0b96a91a3bf3f260c1bcc5f866ade87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827511"
---
# <a name="media-buffers"></a>Buffer multimediali

Un buffer multimediale è un oggetto COM che gestisce un blocco di memoria, in genere per contenere i dati multimediali. I buffer multimediali vengono usati per spostare i dati da un componente della pipeline a quello successivo. La maggior parte delle applicazioni non usa direttamente i buffer multimediali, perché la sessione multimediale gestisce tutto il flusso di dati tra gli oggetti della pipeline. È necessario usare i buffer multimediali se si scrive un componente della pipeline personalizzato o se si usa un componente della pipeline direttamente senza la sessione multimediale.

I buffer multimediali espongono [**l'interfaccia IMFMediaBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) Questa interfaccia è progettata per la lettura o la scrittura di qualsiasi tipo di dati. I fotogrammi video non compressi richiedono una gestione speciale, perché potrebbero essere archiviati in superfici Direct3D che si trovano nella memoria video.

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                        | Descrizione                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [Uso dei buffer multimediali](working-with-media-buffers.md) | Descrive il comportamento generale dei buffer multimediali per tutti i tipi di supporti. |
| [Buffer video non compressi](uncompressed-video-buffers.md) | Come usare i buffer multimediali contenenti fotogrammi video non compressi.  |
| [DirectX Surface Buffer](directx-surface-buffer.md)         | Viene descritto come archiviare una superficie Direct3D in un buffer multimediale.         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation primitive](media-foundation-primitives.md)
</dt> </dl>

 

 



