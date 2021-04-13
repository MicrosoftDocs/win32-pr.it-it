---
description: Informazioni sull'origine del sequencer
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Informazioni sull'origine del sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526611"
---
# <a name="about-the-sequencer-source"></a>Informazioni sull'origine del sequencer

L'origine di Sequencer consente a un'applicazione di riprodurre in sequenza una raccolta di [origini multimediali](media-sources.md) , con transizioni senza problemi tra le origini. L'origine di Sequencer può essere usata per gli scenari seguenti:

-   Creare una playlist che passa facilmente da un'origine multimediale a quella successiva.
-   Riprodurre flussi da più origini contemporaneamente; ad esempio, riprodurre l'audio da un file con il video da un altro.
-   Passare da un flusso all'altro in diverse origini multimediali in voci consecutive della playlist; ad esempio, una playlist può includere voci che condividono la stessa origine video mentre ogni voce contiene un'origine audio diversa.

Per ogni elemento di una playlist, l'applicazione crea una topologia separata. Le origini multimediali in queste topologie sono denominate *origini native*, per distinguerle dall'origine del sequencer. Durante la riproduzione, l'intera sequenza di topologie viene chiamata *presentazione* e ogni topologia all'interno della sequenza viene chiamata *segmento*.

La riproduzione è controllata dalla [sessione multimediale](media-session.md), che fornisce controlli di trasporto, ad esempio riproduzione, pausa e arresto. La sessione multimediale gestisce anche l'ora di presentazione e invia gli eventi all'applicazione. (Gli eventi dell'origine di Sequencer vengono trasmessi all'applicazione tramite la sessione multimediale).

Per creare una playlist, l'applicazione crea una o più topologie di riproduzione e le accoda nell'origine del sequencer nell'ordine di riproduzione desiderato. Internamente, l'origine del sequencer modifica le topologie in modo che i nodi di origine puntino all'origine del sequencer invece che all'origine nativa. L'applicazione invia alla sessione multimediale le topologie modificate, anziché le topologie originali. Ciò consente all'origine del sequencer di aggregare le origini native e di comunicare con la sessione multimediale.

Per ottenere transizioni senza problemi tra i segmenti, l'origine del Sequencer esegue il prerolling di ogni segmento. Mentre un segmento viene riprodotto e prima che sia il momento di riprodurre il segmento seguente, l'origine del sequencer genera un evento [MENewPresentation](menewpresentation.md) che contiene un descrittore di presentazione. L'applicazione utilizza questo descrittore di presentazione per ottenere la topologia per il segmento successivo nella presentazione e accoda la topologia nella sessione multimediale.

Nella figura seguente viene illustrato il flusso di dati per le voci della playlist tramite l'origine del sequencer. L'applicazione utilizza il resolver di origine per creare le origini native, compila le topologie per ogni segmento e accoda le topologie nell'origine del sequencer.

![diagramma che mostra il flusso di dati dei segmenti imfmediasession, imfsequencersource e playlist che portano a IMFMediaSource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare una playlist](how-to-create-a-playlist.md)
</dt> <dt>

[Topologie](topologies.md)
</dt> <dt>

[Utilizzo dell'origine sequencer](using-the-sequencer-source.md)
</dt> <dt>

[Origine sequencer](sequencer-source.md)
</dt> </dl>

 

 



