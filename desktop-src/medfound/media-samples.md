---
description: Informazioni sugli esempi multimediali in Microsoft Media Foundation. Un campione multimediale è un oggetto che contiene un elenco ordinato di zero o più buffer.
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Esempi di supporti (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83bad0186d54d99b6c7f7666a5971f6c35e8e2a561109e7bfd6afd45fd5f5e6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061071"
---
# <a name="media-samples-microsoft-media-foundation"></a>Esempi di supporti (Microsoft Media Foundation)

Un campione multimediale è un oggetto che contiene un elenco ordinato di zero o più buffer. Gli esempi multimediali espongono [**l'interfaccia IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) La quantità di dati contenuti in un campione dipende dal componente che crea il campione e dal tipo di dati nei buffer. Per i video non compressi, un esempio contiene in genere un singolo fotogramma video. Per l'audio non compresso, la quantità di dati può variare, ma in genere un frame audio non si estende su due campioni. Per i dati compressi, queste linee guida potrebbero non essere applicabili.

Un singolo campione può contenere più buffer per motivi di efficienza. In un file ASF, ad esempio, un fotogramma video viene spesso distribuito tra più pacchetti ASF. L'origine multimediale potrebbe leggere i pacchetti in più buffer. Invece di copiare ogni frammento in un unico buffer, l'origine inserisce semplicemente tutti i buffer in un unico campione. I componenti downstream possono quindi decidere se copiare i buffer più piccoli in un unico buffer contiguo. In genere, se si scrive un componente della pipeline, è necessario presupporre che qualsiasi esempio possa contenere più di un buffer.

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                        | Descrizione                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Uso di esempi multimediali](working-with-media-samples.md) | Descrive il comportamento generale degli esempi di supporti.                                                                         |
| [Esempi video](video-samples.md)                           | Descrive un'implementazione specializzata di [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) progettata per contenere fotogrammi video non compressi. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer multimediali](media-buffers.md)
</dt> <dt>

[Media Foundation primitive](media-foundation-primitives.md)
</dt> </dl>

 

 



