---
title: Panoramica di Windows Media Format SDK
description: Panoramica di Windows Media Format SDK
ms.assetid: 9e5d6254-6261-4ca8-84d6-38050c93db22
keywords:
- Windows Media Format SDK, creazione e modifica di file ASF
- ASF (Advanced Systems Format), creazione e modifica di file
- ASF (formato avanzato dei sistemi), creazione e modifica di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4f58be5d377e44fc0f68c89ad580a554902c58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328740"
---
# <a name="overview-of-the-windows-media-format-sdk"></a>Panoramica di Windows Media Format SDK

Windows Media Format SDK contiene oggetti per eseguire attività in tre punti della durata di un file ASF: creazione, modifica e riproduzione. Alcune applicazioni, in particolare quelle per la modifica dei video, utilizzeranno le funzionalità generali di Windows Media Format SDK per leggere il contenuto dei file ASF, modificare il contenuto e scrivere i risultati in un nuovo file. Tuttavia, è più facile pensare a questo SDK nelle tre fasi della creazione, della modifica e della riproduzione dei file.

## <a name="asf-file-creation-with-the-windows-media-format-sdk"></a>Creazione di file ASF con Windows Media Format SDK

Il processo di scrittura di file ASF con Windows Media Format SDK è, a un livello elevato, piuttosto semplice. La creazione di file è gestita da un oggetto writer. Si indica all'oggetto writer quale tipo di file si vuole creare specificando un oggetto profilo da usare. Ogni oggetto profilo contiene le impostazioni per un file ASF. Alcuni profili sono inclusi in questo SDK e il supporto per la modifica del profilo è fornito da un certo numero di oggetti. Quando è stato impostato un profilo per l'oggetto writer da usare, è possibile iniziare a passare gli esempi al writer per l'elaborazione. Nella maggior parte dei casi, un esempio è un frammento di audio o video non compresso, ma un esempio può essere qualsiasi tipo di dati.

Internamente, il writer esegue tre attività principali. Prima di tutto, se il flusso a cui appartiene un campione deve essere compresso, il writer comunica con la parte di codifica del codec (compressore/decompressore) per comprimere l'esempio. Una volta che gli esempi sono nel formato specificato dal profilo, il writer suddivide gli esempi in pacchetti di dimensioni appropriate da trasmettere in una rete. Infine, i dati dei vari flussi vengono multiplexati o Interleaved, in modo che i campioni con tempi di presentazione simili in tutti i flussi siano vicini tra loro nella sezione dati del file ASF.

L'oggetto writer non scrive effettivamente un file. Comunica con uno o più oggetti denominati sink, che inviano i dati dal writer alla relativa destinazione. Nel caso di file locali, un sink di file gestisce la scrittura dei dati nel file. È anche possibile configurare i sink di rete per distribuire i dati ASF in una rete. In genere viene usato più di un sink. Ad esempio, un'applicazione può trasmettere un file in rete e salvare una copia come file su un disco locale simultaneamente. Usando un sink di push, è possibile trasmettere il contenuto dall'applicazione di scrittura a uno o più server che eseguono servizi Windows Media, che distribuirà quindi il contenuto agli utenti.

## <a name="asf-file-editing-with-the-windows-media-format-sdk-metadata-editing"></a>Modifica di file ASF con Windows Media Format SDK (modifica dei metadati)

Per modificare il contenuto della sezione relativa ai dati di un file ASF è necessario riscrivere il file. Windows Media Format SDK non fornisce alcun oggetto che modifichi la sezione dei dati sul posto. Per le semplici modifiche, ad esempio la concatenazione di due file o la riduzione del contenuto da un file, è possibile leggere esempi senza decomprimerli e quindi scriverli in un nuovo file usando le stesse informazioni di intestazione. Modifiche più complesse comportano l'esecuzione di modifiche al profilo utilizzato per il nuovo file.

Windows Media Format SDK supporta la modifica di parti della sezione dell'intestazione senza riscrivere il file. L'intestazione di un file ASF contiene molti tipi diversi di dati. Gli attributi più comunemente modificati sono gli attributi dei metadati, ovvero coppie nome/valore che descrivono gli aspetti del contenuto e le persone che lo fanno. È possibile modificare i metadati utilizzando l'oggetto dell'editor di metadati di Windows Media Format SDK. Questo oggetto consente di aprire un file ASF, di modificare il contenuto dell'intestazione, di scrivere le modifiche apportate al file e di chiudere il file. La modifica dei metadati è molto semplice, con semplici chiamate al metodo per recuperare e impostare i valori.

## <a name="asf-file-reading-with-the-windows-media-format-sdk"></a>Lettura di file ASF con Windows Media Format SDK

Windows Media Format SDK fornisce due oggetti distinti per la lettura dei file ASF, ovvero l'oggetto Reader e l'oggetto Reader sincrono. L'oggetto Reader è disponibile in tutte le versioni dell'SDK, mentre l'oggetto Reader sincrono richiede Windows Media Format 9 Series SDK o una versione successiva. La differenza principale tra i due è che l'oggetto Reader recapita esempi all'applicazione generando eventi in un metodo di callback, mentre il lettore sincrono fornisce singoli esempi in risposta alle chiamate al metodo.

Per utilizzare l'oggetto Reader, è necessario implementare diversi metodi di callback per rispondere ai messaggi di stato e di esempio dall'oggetto Reader. Il lettore viene configurato per recapitare il contenuto nel modo desiderato, avviare il lettore e attendere i messaggi di esempio. Il processo di recupero degli esempi da un file ASF è fondamentalmente il contrario del processo di scrittura. L'oggetto Reader comunica con i codec necessari per decodificare i flussi compressi e recapita i dati non compressi all'applicazione. È anche possibile configurare l'oggetto Reader per recapitare gli esempi nello stato compresso, in modo che sia possibile includere un flusso codificato in precedenza in un nuovo file.

L'oggetto Reader sincrono funziona in modo molto simile all'oggetto Reader. Anziché configurare i callback, è tuttavia necessario richiedere singolarmente ogni esempio dal lettore sincrono. L'utilizzo del lettore sincrono richiede un solo thread, mentre l'utilizzo del lettore richiede più thread. In determinate circostanze, l'oggetto Reader sincrono presenta diversi vantaggi rispetto all'oggetto Reader, soprattutto per le applicazioni di modifica del contenuto che devono accedere rapidamente a diverse parti di un file e copiare i dati tra i file. L'oggetto Reader sincrono è molto più semplice da utilizzare e consente di semplificare la ricerca di posizioni specifiche nella sezione di dati. Tuttavia, il lettore sincrono non supporta la lettura di file in rete e non supporta Digital Rights Management.

## <a name="other-operations-with-the-windows-media-format-sdk"></a>Altre operazioni con Windows Media Format SDK

Oltre alle tre principali aree funzionali appena descritte, Windows Media Format SDK include oggetti per eseguire altre operazioni relative ai file ASF. L'oggetto Gestione profili viene utilizzato per creare e accedere ai profili e per salvarli. L'oggetto indicizzatore crea oggetti index nei file ASF che consentono la ricerca nei file video. Infine, l'oggetto Reader e l'oggetto writer supportano Digital Rights Management per proteggere i diritti intellettuali dei creatori di contenuti.

**Nota** L'intenzione della struttura dei file ASF e di questo SDK in generale è quella di generare file multimediali digitali contenenti audio e video e questa documentazione viene scritta con tale scopo. Tuttavia, la struttura dei file ASF funzionerà anche per altri tipi di contenuto. È possibile trovare molte applicazioni per i file ASF che non sono correlati a audio e video.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




