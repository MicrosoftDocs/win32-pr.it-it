---
description: Informazioni sull'origine Sequencer
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Informazioni sull'origine Sequencer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d81799a8bc1e46ade10989bbe485c69e839832fce0ded14220c536809e23e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065560"
---
# <a name="about-the-sequencer-source"></a>Informazioni sull'origine Sequencer

L'origine sequencer consente a un'applicazione di riprodurre una raccolta di origini multimediali [in](media-sources.md) sequenza, con transizioni senza interruzioni tra le origini. L'origine sequencer può essere usata per gli scenari seguenti:

-   Creare una playlist che passa facilmente da un'origine multimediale all'altra.
-   Riprodurre flussi da più origini contemporaneamente; Ad esempio, riprodurre l'audio da un file con il video di un altro.
-   Passare da un flusso all'altro in origini multimediali diverse in voci di playlist consecutive; Ad esempio, una playlist può avere voci che condividono la stessa origine video, mentre ogni voce contiene un'origine audio diversa.

Per ogni elemento di una playlist, l'applicazione crea una topologia separata. Le origini multimediali in queste topologie sono denominate origini *native,* per distinguerle dall'origine sequencer. Durante la riproduzione, l'intera sequenza di topologie è denominata presentazione e ogni topologia all'interno della sequenza è denominata *segmento*.

La riproduzione è controllata dalla [sessione multimediale](media-session.md), che fornisce controlli di trasporto, ad esempio riproduzione, sospensione e arresto. La sessione multimediale gestisce anche l'ora di presentazione e invia gli eventi all'applicazione. Gli eventi dell'origine sequencer vengono inoltrati all'applicazione tramite la sessione multimediale.

Per creare una playlist, l'applicazione crea una o più topologie di riproduzione e le accoda nell'origine sequencer nell'ordine di riproduzione desiderato. Internamente, l'origine sequencer modifica le topologie in modo che i nodi di origine puntino all'origine sequencer anziché all'origine nativa. L'applicazione invia queste topologie modificate, anziché le topologie originali, alla sessione multimediale. Ciò consente all'origine sequencer di aggregare le origini native e di comunicare con la sessione multimediale.

Per ottenere transizioni senza problemi tra i segmenti, l'origine sequencer esegue il preroll di ogni segmento. Durante la riproduzione di un segmento e prima che sia il momento di riprodurre il segmento seguente, l'origine del sequencer genera un evento [MENewPresentation](menewpresentation.md) che contiene un descrittore di presentazione. L'applicazione usa questo descrittore di presentazione per ottenere la topologia per il segmento successivo nella presentazione e accoda la topologia nella sessione multimediale.

La figura seguente mostra il flusso di dati per le voci della playlist tramite l'origine sequencer. L'applicazione usa il resolver di origine per creare le origini native, compila topologie per ogni segmento e accoda le topologie nell'origine sequencer.

![diagramma che mostra il flusso di dati da imfmediasession, imfsequencersource e segmenti di playlist che portano a imfmediasource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare una playlist](how-to-create-a-playlist.md)
</dt> <dt>

[Topologie](topologies.md)
</dt> <dt>

[Uso dell'origine Sequencer](using-the-sequencer-source.md)
</dt> <dt>

[Origine Sequencer](sequencer-source.md)
</dt> </dl>

 

 



