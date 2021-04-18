---
description: In questa sezione viene descritta la progettazione generale di Microsoft Media Foundation. Per informazioni sull'utilizzo di Media Foundation per attività di programmazione specifiche, vedere Guida alla programmazione di Media Foundation.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Architettura di Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320771"
---
# <a name="media-foundation-architecture"></a>Architettura di Media Foundation

In questa sezione viene descritta la progettazione generale di Microsoft Media Foundation. Per informazioni sull'utilizzo di Media Foundation per attività di programmazione specifiche, vedere [Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Panoramica dell'architettura Media Foundation](overview-of-the-media-foundation-architecture.md)<br/> | Fornisce una panoramica di alto livello dell'architettura Media Foundation.<br/>                                                                                                                                                                                                               |
| [Primitive Media Foundation](media-foundation-primitives.md)<br/>                                     | Vengono descritte alcune interfacce di base utilizzate in Media Foundation.<br/> Quasi tutte le applicazioni Media Foundation utilizzeranno tali interfacce.<br/>                                                                                                                       |
| [API della piattaforma Media Foundation](media-foundation-platform-apis.md)<br/>                               | Descrive le funzioni di base Media Foundation, ad esempio callback asincroni e code di lavoro.<br/> Alcune applicazioni possono utilizzare interfacce a livello di piattaforma. Inoltre, i plug-in personalizzati, ad esempio le origini supporti e MFTs, usano queste interfacce.<br/>                                       |
| [Pipeline Media Foundation](media-foundation-pipeline.md)<br/>                                         | Il Media Foundation livello della pipeline è costituito da origini supporti, MFTs e sink multimediali. La maggior parte delle applicazioni non chiama i metodi direttamente sul livello della pipeline. Al contrario, le applicazioni utilizzano uno dei livelli più elevati, ad esempio la sessione multimediale o l'Reader di origine e il writer del sink.<br/> |
| [Sessione multimediale](media-session.md)<br/>                                                                 | La sessione multimediale gestisce il flusso di dati nella pipeline Media Foundation.<br/>                                                                                                                                                                                                           |
| [Lettore di origine](source-reader.md)<br/>                                                                 | Il lettore di origine consente a un'applicazione di recuperare i dati da un'origine multimediale, senza che il applicating debba chiamare direttamente le API di origine multimediale. Il lettore di origine può inoltre eseguire la decodifica dei flussi compressi.<br/>                                                            |
| [Percorso supporto protetto](protected-media-path.md)<br/>                                                   | Il percorso multimediale protetto (PMP) fornisce un ambiente protetto per la riproduzione di contenuti video Premium. Non è necessario usare PMP quando si scrive un'applicazione Media Foundation. <br/>                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation: concetti essenziali](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Media Foundation e COM](media-foundation-and-com.md)
</dt> <dt>

[Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




