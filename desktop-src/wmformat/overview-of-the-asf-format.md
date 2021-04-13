---
title: Panoramica del formato ASF
description: Panoramica del formato ASF
ms.assetid: ef22a493-d6cf-40d2-ab17-d87159066d1d
keywords:
- Windows Media Format SDK, panoramica del formato ASF
- Formato avanzato dei sistemi (ASF), panoramica del formato
- ASF (formato avanzato dei sistemi), panoramica del formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2858ae1845629c25b52d4c15b5ce7fbb5eb82146
ms.sourcegitcommit: d230e7720c0b566919f8ca11ff7fe3c6b32e028c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/26/2020
ms.locfileid: "104398776"
---
# <a name="overview-of-the-asf-format"></a>Panoramica del formato ASF

Il formato ASF (Advanced Systems Format) è un formato di file estendibile progettato principalmente per l'archiviazione e la riproduzione di flussi multimediali digitali sincronizzati e la relativa trasmissione su reti. ASF è il formato del contenitore per Windows Media Audio e il contenuto basato su Windows Media Video. L'estensione WMA o WMV viene utilizzata per specificare un file ASF che contiene il contenuto codificato con i codec Windows Media Audio e/o Windows Media Video. Windows Media Format SDK può essere utilizzato per creare e leggere i file di Windows Media, nonché i file ASF che contengono altri tipi di dati compressi o non compressi.

In questa sezione viene fornita una descrizione generale del formato ASF come informazioni di base. Poiché gli oggetti Reader e writer gestiscono tutte le attività di analisi e formattazione dei file di basso livello, non è necessario avere una conoscenza approfondita di ASF prima di usare questo SDK per creare file ASF. La specifica ASF completa si trova nel [sito Web Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

Gli obiettivi principali del formato ASF sono:

-   Per supportare la riproduzione efficiente da server multimediali, server HTTP e dispositivi di archiviazione locale.
-   Per supportare i tipi di supporto scalabili, ad esempio audio e video.
-   Per consentire la presentazione di una singola composizione multimediale in un'ampia gamma di larghezze di banda.
-   Per consentire il controllo della creazione di relazioni tra flussi multimediali, soprattutto in scenari con larghezza di banda limitata.
-   Per essere indipendente da qualsiasi particolare sistema di composizione multimediale, sistema operativo del computer o protocollo di comunicazione dati.

Un file ASF può contenere più flussi indipendenti o dipendenti, tra cui più flussi audio per audio multicanale o flussi video a velocità in bit più idonei per la trasmissione su larghezze di banda diverse. I flussi possono essere in qualsiasi formato compresso o non compresso; Tuttavia, la compressione migliore viene eseguita con i codec della serie Microsoft Windows Media Audio e video 9. Oltre ai tipi di flusso audio e video standard, un file ASF può contenere anche flussi di testo, pagine Web e comandi script e qualsiasi altro tipo di dati arbitrario. ASF supporta contenuti multimediali live e su richiesta. Può essere usato come veicolo per registrare o riprodurre le conferenze H. 32X (ad esempio, H. 323 e H. 324) o MBONE.

Un file ASF è organizzato in sezioni denominate "oggetti". Sono disponibili tre oggetti di primo livello, un oggetto intestazione e un oggetto dati (entrambi necessari), oltre a un oggetto index facoltativo. L'oggetto header contiene informazioni generali sul file, ad esempio le dimensioni del file, il numero di flussi, i metodi di correzione degli errori e i codec utilizzati. I metadati vengono archiviati anche qui. L'oggetto intestazione è l'unico oggetto di primo livello che può contenere altri oggetti. L'oggetto dati contiene i dati del flusso, organizzati in pacchetti. L'oggetto indice semplice contiene un elenco di coppie Indice/fotogrammi chiave associate che consentono alle applicazioni di eseguire ricerche in un file in modo efficiente. L'indice associato a ciascun fotogramma chiave può essere un tempo di presentazione, un numero di fotogramma video o un timestamp di riferimento.

Ogni oggetto di primo livello o di livello inferiore inizia con un identificatore univoco globale (GUID) e un valore di dimensione. Questi numeri consentono al lettore di file di analizzare le informazioni in posizioni appropriate in oggetti identificabili. A causa di questi GUID, gli oggetti di livello inferiore possono essere inviati in qualsiasi ordine e comunque riconosciuti. Il formato ASF è progettato per superare la ricezione dei dati non accurati. Un file ASF scaricato parzialmente può comunque essere letto, purché contenga l'oggetto intestazione e almeno un oggetto dati.

Informazioni dettagliate su ASF in presentate nella specifica ASF. È possibile scaricare la specifica dal [sito Web Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




