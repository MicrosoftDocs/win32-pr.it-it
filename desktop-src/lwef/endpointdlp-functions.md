---
title: Funzioni di prevenzione della perdita dei dati degli endpoint
description: Funzioni usate dalla funzionalità di prevenzione della perdita dei dati degli endpoint.
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: f8713a6a6051bf477b4f9c7f6f8a7430abf70a52
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495588"
---
# <a name="endpoint-data-loss-prevention-functions"></a>Funzioni di prevenzione della perdita dei dati degli endpoint

Funzioni usate dalla funzionalità di prevenzione della perdita dei dati degli endpoint.



| Funzioni                                                       | Descrizione                                                           |
|-------------------------------------------------------------------|-----------------------------------------------------------------------|
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di chiusura del documento.                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di chiusura del documento.                                  |
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | Fornisce al sistema informazioni su un documento quando viene immesso un obiettivo di rilascio.                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | Recupera la versione dell'API di prevenzione della perdita dei dati (DLP) dell'endpoint nel dispositivo corrente.                                  |
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | Notifica al sistema le modalità di imposizione desiderate per un set di operazioni dlp (Data Loss Prevention) dell'endpoint.                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Determina se l'app deve eseguire il pull dei dati dagli Appunti di sistema anziché dalla cache interna.                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | Fornisce al sistema informazioni su un documento quando un obiettivo di rilascio viene chiuso.                                  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di copia negli Appunti.  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di trascinamento della selezione.  |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md)                       | Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di apertura.                                  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di apertura.                                  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione Incolla dagli Appunti.                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | Fornisce al sistema informazioni su un documento al termine di un'operazione di stampa.                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di salvataggio con nome.                                  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | Fornisce al sistema informazioni su un documento dopo l'avvio di un'operazione di stampa.                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | Fornisce al sistema informazioni sullo stato dopo il completamento di un'operazione di stash degli Appunti.                                  |
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione di copia negli Appunti.  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione di trascinamento della selezione.  |
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md)                         | Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di apertura.  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di apertura.  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione Incolla dagli Appunti.  |
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di stampa.  |
| [DlpNotifyPreSaveDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di salvataggio con nome.                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | Notifica al sistema prima che venga avviata un'operazione di stash clipboard.                                  |