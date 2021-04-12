---
description: Origini supporti
ms.assetid: 65132e7d-22f6-4209-bc58-f5ea86ebd514
title: Origini supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd69b63679ba73bc4049f37207b1d07940edada
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234484"
---
# <a name="media-sources"></a>Origini supporti

Le *origini multimediali* sono oggetti che generano dati multimediali nella pipeline Media Foundation. In questa sezione vengono descritte in dettaglio le API di origine multimediale. Leggere questa sezione se si sta implementando un'origine multimediale personalizzata o usando un'origine multimediale esterna alla pipeline Media Foundation.

Se l'applicazione usa il livello di controllo, deve usare solo un subset limitato delle API di origine multimediale. Per informazioni, vedere l'argomento [uso di origini multimediali con la sessione multimediale](using-media-sources-with-the-media-session.md).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                 | Descrizione                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Modello a oggetti di origine multimediale](media-source-object-model.md)<br/>                                 | Questo argomento descrive il modello a oggetti per le origini multimediali in Microsoft Media Foundation<br/>                     |
| [Descrittori di presentazione](presentation-descriptors.md)<br/>                                   | Un *descrittore di presentazione* è un oggetto che contiene la descrizione di una particolare presentazione.<br/>      |
| [Eventi di origine dei supporti](media-source-events.md)<br/>                                             | Questo argomento elenca gli eventi inviati da origini multimediali e flussi multimediali.<br/>                             |
| [Scrittura di un'origine multimediale personalizzata](writing-a-custom-media-source.md)<br/>                         | Questo argomento descrive come implementare un'origine multimediale personalizzata in Media Foundation.<br/>                          |
| [Case Study: origine supporto MPEG-1](tutorial--writing-a-custom-media-source.md)<br/>             | In questo argomento viene illustrata in dettaglio l'esempio [MPEG-1 media source](mpeg1source-sample.md) SDK.<br/>        |
| [Provider di metadati personalizzati per i file multimediali](custom-metadata-providers-for-media-files.md)<br/> | In questo argomento viene descritto come scrivere un gestore di proprietà della shell personalizzato per un Media Foundation origine multimediale.<br/>    |
| [Resolver di origine](source-resolver.md)<br/>                                                     | Il resolver dell'origine accetta un URL o un flusso di byte e crea l'origine multimediale appropriata per il contenuto.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline Media Foundation](media-foundation-pipeline.md)
</dt> <dt>

[Provider di metadati personalizzati per i file multimediali](custom-metadata-providers-for-media-files.md)
</dt> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 




