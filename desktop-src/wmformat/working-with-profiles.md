---
title: Uso dei profili
description: Uso dei profili
ms.assetid: e1e31632-0db7-47db-a992-f5db9d8824c1
keywords:
- Windows MEDIA Format SDK, profili
- Windows Media Format SDK, interfaccia IWMCodecInfo3
- profili, informazioni
- profili, Windows Media Format SDK
- profiles,IWMCodecInfo3
- IWMCodecInfo3,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68982a47b743aaa12397e937ad9bd213fbd7ac0a78b41087d01929c1d42bb622
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055431"
---
# <a name="working-with-profiles"></a>Uso dei profili

Questa sezione descrive come progettare, creare e modificare i profili. Ogni profilo descrive i flussi che costituiscono un file e le relative relazioni tra loro. Un oggetto profilo contiene informazioni di configurazione del flusso per ogni flusso, informazioni di esclusione reciproca per i flussi che non possono essere recapitati contemporaneamente, informazioni sulla condivisione della larghezza di banda e informazioni sulla priorità dei flussi.

Lo scopo principale dei profili è fornire informazioni di configurazione del flusso all'oggetto writer. Il writer usa le informazioni in un profilo per coordinare con i codec il processo di compressione degli input. Quando si configura un flusso multimediale compresso, si specifica il codec usato per comprimere i dati e le impostazioni usate dal codec. È anche possibile creare profili per i flussi non compressi. Sono supportati diversi tipi di flusso non compressi. Anche se non richiedono un codec, questi tipi hanno requisiti specifici per la configurazione del flusso. Per altre informazioni, vedere [Configuring Flussi](configuring-streams.md) and [Using Uncompressed Audio and Video Flussi](using-uncompressed-audio-and-video-streams.md).

Le informazioni di configurazione del flusso per un flusso che usano uno dei codec Windows Media devono essere ottenute dal codec usando i metodi [**dell'interfaccia IWMCodecInfo3.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) La procedura per l'uso dei formati di flusso è diversa per i codec video rispetto ai codec audio, ma in entrambi i casi è necessario iniziare ottenendo il formato dal codec. Non provare mai a configurare manualmente un flusso usando uno dei codec di Windows Media, perché piccoli errori nel profilo possono avere un effetto negativo sul file ASF.

I passaggi di base per la creazione e/o la modifica dei profili sono:

1.  Creare un profilo vuoto o caricare un profilo esistente da modificare.
2.  Configurare ogni flusso, se necessario, in base ai dati di profilo supportati recuperati dal codec che verrà usato per codificare il flusso.
3.  Configurare l'esclusione reciproca, se necessario.
4.  Configurare la condivisione della larghezza di banda, se necessario.
5.  Impostare la priorità dei flussi nel file, se necessario.

Le sezioni seguenti illustrano il processo di creazione e modifica dei profili.



| Sezione                                                        | Descrizione                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Progettazione di profili](designing-profiles.md)                   | Viene descritto come progettare un profilo.                                                                 |
| [Creazione di profili](creating-profiles.md)                     | Viene descritto come creare un profilo vuoto.                                                          |
| [Configurazione di Flussi](configuring-streams.md)                 | Viene descritto come configurare i flussi e includerli in un profilo.                                  |
| [Uso dell'esclusione reciproca](using-mutual-exclusion.md)           | Viene descritto come creare oggetti di esclusione reciproca e includerli in un profilo.                    |
| [Uso della condivisione della larghezza di banda](using-bandwidth-sharing.md)         | Descrive come usare la condivisione della larghezza di banda in un profilo.                                               |
| [Uso della definizione delle priorità dei flussi](using-stream-prioritization.md) | Viene descritto come usare l'assegnazione delle priorità dei flussi in un profilo.                                           |
| [Salvataggio dei profili](saving-profiles.md)                         | Viene descritto come salvare i profili personalizzati in un file.                                              |
| [Uso dei profili di sistema](using-system-profiles.md)             | Descrive come usare i profili di sistema per risparmiare tempo e impegno nella creazione dei profili.           |
| [Gestione delle dimensioni dei pacchetti](managing-packet-size.md)               | Viene illustrato come controllare le dimensioni dei pacchetti nei flussi di dati dei file effettuati usando il profilo. |



 

**Nota** Gli utenti delle versioni precedenti di Windows Media Format SDK possono essere abituati a usare i profili di sistema senza apportare modifiche per creare i file. In Windows Media Format 9 Series SDK o versioni successive non sono inclusi nuovi profili di sistema che usano i codec Windows Media 9 Series o versioni successive. Ciò è dovuto al numero crescente di profili necessari per coprire le varie funzionalità ora offerte dai codec. È comunque possibile usare i profili di sistema versione 8 come punto di partenza per i profili. Per altre informazioni, vedere [Uso dei profili di sistema.](using-system-profiles.md) Per informazioni sul nuovo meccanismo per la destinazione dei profili a dispositivi di recapito specifici, vedere [Uso dei modelli di conformità dei dispositivi.](working-with-device-conformance-templates.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità dei file ASF**](asf-file-features.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 




