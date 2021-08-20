---
title: Panoramica di Windows Media Format SDK
description: Panoramica di Windows Media Format SDK
ms.assetid: 9e5d6254-6261-4ca8-84d6-38050c93db22
keywords:
- Windows MEDIA Format SDK, creazione e modifica di file ASF
- Advanced Systems Format (ASF), creazione e modifica di file
- ASF (Advanced Systems Format), creazione e modifica di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b80436415a6017d0429493b1d4b5be92dcb682f572796e5e9e1c3cfaa8795e66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846428"
---
# <a name="overview-of-the-windows-media-format-sdk"></a>Panoramica di Windows Media Format SDK

L Windows Media Format SDK contiene oggetti per eseguire attività in tre punti della vita di un file ASF: creazione, modifica e riproduzione. Alcune applicazioni, in particolare quelle per la modifica video, useranno l'ampia funzionalità di Windows Media Format SDK per leggere il contenuto dei file ASF, modificare tale contenuto e scrivere i risultati in un nuovo file. Tuttavia, è più semplice pensare a questo SDK nelle tre fasi di creazione, modifica e riproduzione di file.

## <a name="asf-file-creation-with-the-windows-media-format-sdk"></a>Creazione di file ASF con Windows Media Format SDK

Il processo di scrittura di file ASF con Windows Media Format SDK è, a livello di alto livello, piuttosto semplice. La creazione di file viene gestita da un oggetto writer. Per indicare all'oggetto writer il tipo di file da creare, specificare un oggetto profilo da usare. Ogni oggetto profilo contiene le impostazioni per un file ASF. Alcuni profili sono inclusi in questo SDK e il supporto per la modifica dei profili è fornito da diversi oggetti. Dopo aver impostato un profilo per l'utilizzo dell'oggetto writer, è possibile iniziare a passare gli esempi al writer per l'elaborazione. Nella maggior parte dei casi, un campione è una parte di audio o video non compressa, ma un campione può essere qualsiasi tipo di dati.

Internamente, il writer esegue tre attività principali. In primo luogo, se il flusso a cui appartiene un esempio deve essere compresso, il writer comunica con la parte di codifica del codec (codec/decompressore) per comprimere l'esempio. Quando gli esempi sono nel formato specificato dal profilo, il writer suddivide gli esempi in pacchetti di dimensioni appropriate da trasmettere in rete. Infine, i dati dei vari flussi sono multiplexed o interleaved in modo che gli esempi con tempi di presentazione simili in tutti i flussi siano vicini l'uno all'altro nella sezione dei dati del file ASF.

L'oggetto writer non scrive effettivamente un file stesso. Comunica con uno o più oggetti denominati sink, che recapitare i dati dal writer alla destinazione. Nel caso di file locali, un sink di file gestisce la scrittura dei dati nel file. È anche possibile configurare i sink di rete per recapitare i dati ASF in una rete. In genere, vengono usati più sink. Ad esempio, un'applicazione può trasmettere un file in una rete e salvare una copia come file su un disco locale contemporaneamente. Usando un sink di push, è possibile trasmettere il contenuto dall'applicazione di scrittura a uno o più server che eseguono Servizi Windows Media, che distribuiranno il contenuto agli utenti.

## <a name="asf-file-editing-with-the-windows-media-format-sdk-metadata-editing"></a>Modifica di file ASF con Windows Media Format SDK (modifica dei metadati)

La modifica del contenuto della sezione dei dati di un file ASF comporta la riscrittura del file. L Windows Media Format SDK non fornisce oggetti che modificano la sezione dei dati sul posto. Per le semplici modifiche, ad esempio la concatenazione di due file o il taglio di contenuto da un file, è possibile leggere gli esempi senza decomprimerli e quindi scriverli in un nuovo file usando le stesse informazioni di intestazione. Le modifiche più complesse comportano l'applicazione di modifiche al profilo usato per il nuovo file.

L Windows Media Format SDK supporta la modifica di parti della sezione di intestazione senza riscrivere il file. L'intestazione di un file ASF contiene molti tipi diversi di dati. I più comunemente modificati sono gli attributi dei metadati, ovvero coppie nome/valore che descrivono gli aspetti del contenuto e le persone coinvolte nella creazione. È possibile modificare i metadati usando l'oggetto editor di metadati di Windows Media Format SDK. Questo oggetto aprirà un file ASF, consentirà di modificare parte del contenuto dell'intestazione, scrivere le modifiche nel file e chiudere il file. La modifica dei metadati è molto semplice, con semplici chiamate al metodo per recuperare e impostare valori.

## <a name="asf-file-reading-with-the-windows-media-format-sdk"></a>Lettura di file ASF con Windows Media Format SDK

L Windows Media Format SDK fornisce due oggetti distinti per la lettura dei file ASF: l'oggetto lettore e l'oggetto lettore sincrono. L'oggetto lettore è disponibile in tutte le versioni dell'SDK, mentre l'oggetto lettore sincrono richiede Windows Media Format 9 Series SDK o una versione successiva. La differenza principale tra i due consiste nel fatto che l'oggetto reader recapita esempi all'applicazione generando eventi a un metodo di callback, mentre il lettore sincrono fornisce singoli esempi in risposta alle chiamate al metodo.

Per usare l'oggetto lettore, è necessario implementare diversi metodi di callback per reagire allo stato e ai messaggi di esempio dall'oggetto lettore. Configurare il lettore per recapitare il contenuto come si desidera, avviare il lettore e attendere i messaggi di esempio. Il processo di recupero di esempi da un file ASF è fondamentalmente il contrario del processo di scrittura. L'oggetto lettore comunica con i codec necessari per decodificare i flussi compressi e recapitare i dati non compressi all'applicazione. È anche possibile configurare l'oggetto lettore per distribuire gli esempi nello stato compresso, in modo da poter includere un flusso codificato in precedenza in un nuovo file.

L'oggetto lettore sincrono funziona in modo molto identico all'oggetto lettore. Invece di configurare i callback, è necessario richiedere ogni esempio al lettore sincrono singolarmente. L'uso del lettore sincrono richiede un solo thread, mentre l'uso del lettore richiede più thread. L'oggetto lettore sincrono offre diversi vantaggi rispetto all'oggetto lettore in determinate circostanze, principalmente per le applicazioni di modifica del contenuto che devono accedere rapidamente a parti diverse di un file e copiare i dati tra i file. L'oggetto lettore sincrono è molto più semplice da usare e semplifica la ricerca in posizioni specifiche nella sezione dei dati. Tuttavia, il lettore sincrono non supporta la lettura di file in rete e non supporta digital rights management.

## <a name="other-operations-with-the-windows-media-format-sdk"></a>Altre operazioni con l'SDK Windows Media Format

Oltre alle tre principali aree funzionali appena descritte, Windows Media Format SDK include oggetti per eseguire altre operazioni relative ai file ASF. L'oggetto di gestione dei profili viene usato per creare e accedere ai profili e salvarli. L'oggetto indicizzatore crea oggetti indice nei file ASF che consentono la ricerca nei file video. Infine, l'oggetto lettore e l'oggetto writer supportano la gestione dei diritti digitali per proteggere i diritti intellettuale degli autori di contenuti.

**Nota** L'intenzione della struttura di file ASF e di questo SDK in generale è produrre file multimediali digitali contenenti audio e video e questa documentazione è scritta con questo scopo. Tuttavia, la struttura di file ASF funzionerà anche per altri tipi di contenuto. È possibile trovare molte applicazioni per i file ASF che non sono correlate a audio e video.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




