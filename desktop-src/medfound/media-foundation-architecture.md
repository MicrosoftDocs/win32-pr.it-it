---
description: Questa sezione descrive la progettazione generale di Microsoft Media Foundation. Per informazioni sull'uso Media Foundation per attività di programmazione specifiche, vedere guida Media Foundation programmazione.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Architettura di Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abcc95b1fdb39ad7d0e90e44b66df0dd7eb3c06418c16b4efc452abba4a9738d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974216"
---
# <a name="media-foundation-architecture"></a>Architettura di Media Foundation

Questa sezione descrive la progettazione generale di Microsoft Media Foundation. Per informazioni sull'uso Media Foundation per attività di programmazione specifiche, vedere Media Foundation [Programming Guide](media-foundation-programming-guide.md).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Panoramica dell'architettura Media Foundation distribuzione](overview-of-the-media-foundation-architecture.md)<br/> | Offre una panoramica generale dell'architettura Media Foundation generale.<br/>                                                                                                                                                                                                               |
| [Media Foundation primitive](media-foundation-primitives.md)<br/>                                     | Vengono descritte alcune interfacce di base usate in Media Foundation.<br/> Quasi tutte Media Foundation applicazioni useranno queste interfacce.<br/>                                                                                                                       |
| [API Media Foundation platform](media-foundation-platform-apis.md)<br/>                               | Vengono descritte le Media Foundation di base, ad esempio callback asincroni e code di lavoro.<br/> Alcune applicazioni potrebbero usare interfacce a livello di piattaforma. Inoltre, i plug-in personalizzati, ad esempio origini multimediali e MFT, usano queste interfacce.<br/>                                       |
| [Media Foundation Pipeline](media-foundation-pipeline.md)<br/>                                         | Il Media Foundation pipeline è costituito da origini multimediali, MFT e sink multimediali. La maggior parte delle applicazioni non chiama i metodi direttamente sul livello della pipeline. Al contrario, le applicazioni usano uno dei livelli superiori, ad esempio la sessione multimediale o il lettore di origine e sink writer.<br/> |
| [Sessione multimediale](media-session.md)<br/>                                                                 | La sessione multimediale gestisce il flusso di dati nella pipeline Media Foundation dati.<br/>                                                                                                                                                                                                           |
| [Lettore di origine](source-reader.md)<br/>                                                                 | Il lettore di origine consente a un'applicazione di ottenere dati da un'origine multimediale, senza che sia necessario chiamare direttamente le API dell'origine multimediale. Il lettore di origine può anche eseguire la decodifica dei flussi compressi.<br/>                                                            |
| [Percorso del supporto protetto](protected-media-path.md)<br/>                                                   | Il percorso multimediale protetto (PMP) fornisce un ambiente protetto per la riproduzione di contenuto video Premium. Non è necessario usare il PMP durante la scrittura di un'Media Foundation applicazione. <br/>                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation: concetti essenziali](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation e COM](media-foundation-and-com.md)
</dt> <dt>

[Media Foundation di programmazione](media-foundation-programming-guide.md)
</dt> </dl>

 

 




