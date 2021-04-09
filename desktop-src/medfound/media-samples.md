---
description: Esempi di supporti
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Esempi di supporti (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e10df770f0edcdcb329cf8d2bda3d3dc46acbf6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968921"
---
# <a name="media-samples-microsoft-media-foundation"></a>Esempi di supporti (Microsoft Media Foundation)

Un esempio di supporto è un oggetto che contiene un elenco ordinato di zero o più buffer. Gli esempi di supporti espongono l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) . La quantità di dati contenuti in un campione dipende dal componente che crea l'esempio e dal tipo di dati nei buffer. Per i video non compressi, un esempio include in genere un singolo fotogramma video. Per l'audio non compresso, la quantità di dati può variare, ma in genere un frame audio non si estende su due esempi. Per i dati compressi, queste linee guida potrebbero non essere valide.

Un singolo campione potrebbe contenere più buffer per motivi di efficienza. Ad esempio, in un file ASF, un frame video è spesso distribuito tra più pacchetti ASF. L'origine multimediale potrebbe leggere i pacchetti in più buffer. Anziché copiare ogni frammento in un unico buffer, l'origine inserisce semplicemente tutti i buffer in un campione. I componenti downstream possono quindi decidere se copiare i buffer più piccoli in un buffer contiguo. In genere, se si sta scrivendo un componente della pipeline, è necessario presupporre che qualsiasi esempio possa contenere più di un buffer.

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                        | Descrizione                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Utilizzo degli esempi di supporti](working-with-media-samples.md) | Descrive il comportamento generale degli esempi di supporti.                                                                         |
| [Esempi video](video-samples.md)                           | Descrive un'implementazione specializzata di [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) progettata per contenere frame video non compressi. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer multimediali](media-buffers.md)
</dt> <dt>

[Primitive Media Foundation](media-foundation-primitives.md)
</dt> </dl>

 

 



