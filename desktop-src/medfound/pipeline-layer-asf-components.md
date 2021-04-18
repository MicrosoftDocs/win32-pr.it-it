---
description: Nel modello di pipeline di Media Foundation, un'origine multimediale è connessa a una trasformazione che è più connessa a un sink multimediale.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Componenti ASF a livello pipeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309038"
---
# <a name="pipeline-layer-asf-components"></a>Componenti ASF a livello pipeline

Nel modello di pipeline di Media Foundation, un'origine multimediale è connessa a una trasformazione che è ulteriormente connessa a un sink multimediale. I dati contenuti nell'origine passano attraverso la trasformazione e generano esempi di supporti di output nel sink ai fini della riproduzione o della codifica. A seconda che l'applicazione voglia riprodurre contenuto ASF o codificare in un file ASF, l'applicazione deve compilare la pipeline in modo diverso.

Negli argomenti seguenti sono contenute informazioni sui componenti del livello pipeline.

-   [Origine supporto ASF](asf-media-source.md)
-   [Codificatori Windows Media](windows-media-encoders.md)
-   [Sink di supporti ASF](asf-media-sinks.md)

I tre componenti principali di una pipeline ASF per la riproduzione sono i seguenti:

-   L'origine dei supporti ASF viene fornita da Media Foundation che rappresenta un file ASF.
-   Ricampionatori audio, ridimensionamenti di immagini video e così via (trasformazione)
-   Renderer audio e video (sink)

Per informazioni sulla compilazione di una pipeline di riproduzione, vedere [creazione di topologie di riproduzione](creating-playback-topologies.md).

I tre componenti principali di una pipeline ASF per la codifica sono i seguenti:

-   Origine multimediale che rappresenta i dati in un formato che deve essere convertito. Questo componente può essere una delle origini multimediali predefinite fornite da Media Foundation o un'origine personalizzata che espone l'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .
-   Codificatori Windows Media (Transform) che eseguono la conversione del formato.
-   Sink di supporti ASF forniti da Media Foundation che scrivono oggetti ASF ed esempi di supporti in un file di output specificato dall'applicazione.

La pipeline è rappresentata in una topologia e ogni oggetto nella pipeline è rappresentato da un nodo di topologia. Per la riproduzione e la codifica, tutte le operazioni della pipeline sono gestite dalla sessione multimediale. Una delle responsabilità della sessione multimediale consiste nel verificare che la pipeline disponga di tutti i componenti necessari per generare l'output. Ad esempio, in una pipeline di codifica, se il formato di origine audio è diverso dal formato di destinazione, la sessione multimediale inserisce componenti di trasformazione aggiuntivi, ad esempio il Resampler, che esegue conversioni di frequenza di campionamento appropriate. Il controllo del flusso di dati tramite la pipeline viene anche gestito dalla sessione multimediale. In uno scenario di riproduzione, avviando la sessione multimediale, la sessione multimediale Invia esempi a SAR e EVR, che li esegue il rendering sul dispositivo di output. Per la codifica, l'avvio della sessione multimediale avvia il processo di codifica. La sessione invia una notifica in modo asincrono all'applicazione quando la codifica è completa.

Nell'argomento seguente vengono fornite istruzioni dettagliate sull'utilizzo dei componenti del livello pipeline per la compilazione di una topologia di codifica. componenti per la lettura e la scrittura di file ASF.

-   [Esercitazione: codifica Windows Media da 1 passaggio](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



