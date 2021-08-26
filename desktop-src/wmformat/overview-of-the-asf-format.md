---
title: Panoramica del formato ASF
description: Panoramica del formato ASF
ms.assetid: ef22a493-d6cf-40d2-ab17-d87159066d1d
keywords:
- Windows SDK per il formato multimediale, panoramica del formato ASF
- Advanced Systems Format (ASF), panoramica del formato
- ASF (Advanced Systems Format), panoramica del formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee075330e9c68ef1fbdadea12c70fd8deec584f99f8dadd31cb55070dc11eee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930561"
---
# <a name="overview-of-the-asf-format"></a>Panoramica del formato ASF

Advanced Systems Format (ASF) è un formato di file estendibile progettato principalmente per l'archiviazione e la riproduzione di flussi multimediali digitali sincronizzati e per la trasmissione su reti. ASF è il formato contenitore per Windows audio multimediale Windows contenuto basato su Media Video. L'estensione wma o wmv viene usata per specificare un file ASF che contiene contenuto codificato con i codec Windows Media Audio e/o Windows Media Video. L Windows Media Format SDK può essere usato per creare e leggere file multimediali Windows, nonché file ASF che contengono altri tipi di dati compressi o non compressi.

In questa sezione viene fornita una descrizione generale del formato ASF come informazioni di base. Poiché gli oggetti reader e writer gestiscono tutte le attività di analisi e formattazione di file di basso livello, non è necessario avere una conoscenza dettagliata di ASF prima di usare questo SDK per creare file ASF. La specifica ASF completa è disponibile nel sito [Web Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

Gli obiettivi principali del formato ASF sono:

-   Per supportare la riproduzione efficiente da server multimediali, server HTTP e dispositivi di archiviazione locali.
-   Per supportare tipi di supporti scalabili, ad esempio audio e video.
-   Per consentire la presentazione di una singola composizione multimediale su un'ampia gamma di larghezze di banda.
-   Per consentire il controllo della creazione sulle relazioni dei flussi multimediali, in particolare negli scenari con larghezza di banda vincolata.
-   Per essere indipendenti da qualsiasi particolare sistema di composizione multimediale, sistema operativo del computer o protocollo di comunicazione dati.

Un file ASF può contenere più flussi indipendenti o dipendenti, inclusi più flussi audio per l'audio multicanale o più flussi video a velocità in bit adatti per la trasmissione su larghezze di banda diverse. I flussi possono essere in qualsiasi formato compresso o non compresso. Tuttavia, la compressione migliore viene ottenuta con i codec Microsoft Windows Media Audio e Video serie 9. Oltre ai tipi di flusso multimediale audio e video standard, un file ASF può contenere anche flussi di testo, pagine Web e comandi script e qualsiasi altro tipo di dati arbitrario. ASF supporta contenuto multimediale live e su richiesta. Può essere usato come veicolo per registrare o riprodurre conferenze H.32X (ad esempio, H.323 e H.324) o MBONE.

Un file ASF è organizzato in sezioni denominate "oggetti". Sono disponibili tre oggetti di primo livello, un oggetto Header e un oggetto Data (entrambi obbligatori), oltre a un oggetto Index facoltativo. L'oggetto Header contiene informazioni generali sul file, ad esempio dimensioni del file, numero di flussi, metodi di correzione degli errori e codec usati. Anche i metadati vengono archiviati qui. L'oggetto Header è l'unico oggetto di primo livello che può contenere altri oggetti. L'oggetto Data contiene i dati del flusso, organizzati in pacchetti. L'oggetto Indice semplice contiene un elenco di coppie indice/fotogramma chiave associate che consente alle applicazioni di eseguire la ricerca in modo efficiente in un file. L'indice associato a ogni fotogramma chiave può essere un'ora di presentazione, un numero di fotogramma video o un timestamp di riferimento.

Ogni oggetto di primo livello o di livello inferiore inizia con un identificatore univoco globale (GUID) e un valore di dimensione. Questi numeri consentono al lettore di file di analizzare le informazioni nelle posizioni appropriate in oggetti identificabili. A causa di questi GUID, gli oggetti di livello inferiore possono essere inviati in qualsiasi ordine e comunque essere riconosciuti. Il formato ASF è progettato per superare la ricezione imprecisa dei dati. Un file ASF scaricato parzialmente può comunque essere letto, purché contenga l'oggetto Header e almeno un oggetto Data.

Informazioni dettagliate su ASF in presentate nella specifica ASF. È possibile scaricare la specifica dal sito [Web Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




