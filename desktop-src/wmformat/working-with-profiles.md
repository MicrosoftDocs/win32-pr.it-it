---
title: Utilizzo dei profili
description: Utilizzo dei profili
ms.assetid: e1e31632-0db7-47db-a992-f5db9d8824c1
keywords:
- Windows Media Format SDK, profili
- Windows Media Format SDK, interfaccia IWMCodecInfo3
- profili, informazioni
- profili, Windows Media Format SDK
- profili, IWMCodecInfo3
- IWMCodecInfo3, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664bbafd6c628588aa3b45b0a62a216db7bd7749
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398576"
---
# <a name="working-with-profiles"></a>Utilizzo dei profili

In questa sezione viene descritto come progettare, creare e modificare i profili. Ogni profilo descrive i flussi che compongono un file e le relazioni tra loro. Un oggetto profilo contiene le informazioni di configurazione del flusso per ogni flusso, le informazioni di esclusione reciproca per i flussi che non possono essere recapitati simultaneamente, le informazioni di condivisione della larghezza di banda e le informazioni

Lo scopo principale dei profili è fornire informazioni di configurazione del flusso all'oggetto writer. Il writer usa le informazioni contenute in un profilo per coordinare con i codec il processo di compressione degli input. Quando si configura un flusso multimediale compresso, si specifica il codec usato per comprimere i dati e le impostazioni utilizzate dal codec. È anche possibile creare profili per i flussi non compressi. Sono supportati diversi tipi di flusso non compressi. Sebbene non richiedano un codec, questi tipi presentano requisiti specifici per la configurazione del flusso. Per altre informazioni, vedere [configurazione di flussi](configuring-streams.md) e [uso di flussi audio e video non compressi](using-uncompressed-audio-and-video-streams.md).

È necessario ottenere le informazioni di configurazione del flusso per un flusso usando uno dei codec di Windows Media dal codec usando i metodi dell'interfaccia [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) . La procedura per l'uso di formati di flusso è diversa per i codec video rispetto ai codec audio, ma in entrambi i casi è necessario iniziare ottenendo il formato dal codec. Non provare mai a configurare manualmente un flusso usando uno dei codec di Windows Media, perché piccoli errori nel profilo possono avere un effetto significativo sul file ASF.

I passaggi di base per la creazione e/o la modifica di profili sono:

1.  Creare un profilo vuoto o caricare un profilo esistente da modificare.
2.  Configurare ognuno dei flussi, se necessario, in base ai dati del profilo supportati recuperati dal codec che verrà usato per codificare il flusso.
3.  Se necessario, configurare l'esclusione reciproca.
4.  Configurare la condivisione della larghezza di banda, se necessario.
5.  Impostare la priorità dei flussi nel file, se necessario.

Le sezioni seguenti illustrano il processo di creazione e modifica di profili.



| Sezione                                                        | Descrizione                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Progettazione di profili](designing-profiles.md)                   | Viene descritto come progettare un profilo.                                                                 |
| [Creazione di profili](creating-profiles.md)                     | Viene descritto come creare un profilo vuoto.                                                          |
| [Configurazione di flussi](configuring-streams.md)                 | Viene descritto come configurare i flussi e includerli in un profilo.                                  |
| [Uso dell'esclusione reciproca](using-mutual-exclusion.md)           | Viene descritto come creare oggetti di esclusione reciproca e includerli in un profilo.                    |
| [Uso della condivisione della larghezza di banda](using-bandwidth-sharing.md)         | Viene descritto come usare la condivisione della larghezza di banda in un profilo.                                               |
| [Uso della priorità di flusso](using-stream-prioritization.md) | Viene descritto come usare la definizione di priorità del flusso in un profilo.                                           |
| [Salvataggio di profili](saving-profiles.md)                         | Viene descritto come salvare i profili personalizzati in un file.                                              |
| [Uso dei profili di sistema](using-system-profiles.md)             | Viene descritto come utilizzare i profili di sistema per risparmiare tempo e impegno nella creazione di profili.           |
| [Gestione delle dimensioni dei pacchetti](managing-packet-size.md)               | Viene descritto come controllare le dimensioni dei pacchetti nei flussi di dati dei file creati usando il profilo. |



 

**Nota** È possibile che gli utenti delle versioni precedenti di Windows Media Format SDK siano abituati a usare i profili di sistema senza modifiche per creare i file. Windows Media Format 9 Series SDK o versioni successive non include i nuovi profili di sistema che usano la serie Windows Media 9 o i codec successivi. Questo è dovuto all'aumento del numero di profili necessari per coprire le varie funzionalità ora offerte dai codec. È comunque possibile usare i profili di sistema versione 8 come punto di partenza per i profili. Per ulteriori informazioni, vedere [utilizzo dei profili di sistema](using-system-profiles.md). Per informazioni sul nuovo meccanismo per indirizzare i profili a specifici dispositivi di recapito, vedere [utilizzo dei modelli di conformità dei dispositivi](working-with-device-conformance-templates.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 




