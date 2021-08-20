---
description: Timestamp
ms.assetid: 445fe6b9-9d5b-45fd-9c9e-8c632c5228ae
title: Timestamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed14f0155a0bfbf209719f4aff97cbbd19501e6aa32d57e9f0c1cbb2df0964b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072315"
---
# <a name="time-stamps"></a>Timestamp

Il *timestamp definisce* le ore di inizio e fine di un campione multimediale, misurate in tempo di flusso. Il timestamp viene talvolta chiamato ora *di presentazione.* Quando si legge il resto di questo articolo, è importante ricordare che non tutti i formati usano i timestamp nello stesso modo. Ad esempio, non tutti gli esempi MPEG sono contrassegnati con timestamp. Nei grafici di filtro MPEG, il timestamp non viene applicato a ogni fotogramma finché non vengono restituiti dal decodificatore.

Quando un filtro renderer riceve un campione, pianifica il rendering in base al timestamp. Se l'esempio arriva in ritardo o non ha timestamp, il filtro esegue immediatamente il rendering dell'esempio. In caso contrario, il filtro attende l'ora di inizio dell'esempio prima di eseguire il rendering dell'esempio. Attende l'ora di inizio chiamando il metodo [**IReferenceClock::AdviseTime.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime)

I filtri di origine e i filtri del parser sono responsabili dell'impostazione dei timestamp corretti sugli esempi che elaborano. Usare le linee guida seguenti.

-   Riproduzione di file: il primo esempio viene contrassegnato con un'ora di inizio pari a zero. I timestamp successivi sono determinati dalla lunghezza del campione e dalla velocità di riproduzione, che a sua volta è determinata dal formato di file. Il filtro che analizza il file è responsabile del calcolo dei timestamp corretti, ad esempio [AVI Splitter.](avi-splitter-filter.md)
-   Acquisizione di video e audio: ogni campione viene contrassegnato con un'ora di inizio uguale all'ora del flusso in cui è stato acquisito, con le avvertenze seguenti:
    -   I fotogrammi video da un segnaposto di anteprima (anziché un segnaposto di acquisizione) non sono contrassegnati con il timestamp. A causa della latenza del grafico, un fotogramma video contrassegnato con il tempo di acquisizione arriverà sempre in ritardo al renderer video. Ciò potrebbe causare l'eliminazione di frame da parte del renderer, nel tentativo di controllare la qualità. Per informazioni sul controllo di qualità, vedere [Quality-Control Management](quality-control-management.md).
    -   Acquisizione audio: il filtro di acquisizione audio usa un proprio set di buffer, separati da quelli usati dal driver audio. Il driver audio riempie i buffer del filtro di acquisizione a intervalli fissi. L'intervallo dipende dal driver, ma in genere non è superiore a 10 millisecondi. I timestamp sugli esempi audio riflettono l'ora in cui il driver ha riempito i buffer del filtro di acquisizione audio. Questi tempi possono essere leggermente imprecisi, soprattutto se l'applicazione usa dimensioni del buffer molto ridotte. Tuttavia, i tempi dei supporti rifletteranno in modo accurato il numero di campioni audio nel buffer.
-   Filtri Mux: a seconda del formato di output, un filtro mux potrebbe dover generare timestamp oppure potrebbe non farlo. Ad esempio, il formato di file AVI usa una frequenza di fotogrammi fissa senza timestamp, quindi il filtro [Mux AVI](avi-mux-filter.md) presuppone che gli esempi arrivino all'ora più o meno corretta. Se i timestamp in ingresso mostrano uno spazio maggiore di un frame, tuttavia, il mux AVI scrive una voce di indice con dimensione zero, per indicare un frame eliminato. Durante la riproduzione di file, i nuovi timestamp vengono generati in fase di esecuzione, come descritto in precedenza.

Per impostare il timestamp in un esempio, chiamare il [**metodo IMediaSample::SetTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime)

**Media Times**

Facoltativamente, il filtro può anche specificare *un'ora multimediale* per l'esempio. In un flusso video, il tempo multimediale rappresenta il numero di fotogramma. In un flusso audio, il tempo multimediale rappresenta il numero di esempio nel pacchetto. Ad esempio, se ogni pacchetto contiene un secondo di 44,1 kilohertz (kHz), il primo pacchetto ha un'ora di inizio del supporto pari a zero e un tempo di arresto multimediale pari a 44100. In un flusso ricercabile, l'ora del supporto è sempre relativa all'ora di inizio del flusso. Si supponga, ad esempio, di cercare a 2 secondi dall'inizio di un flusso video di 15 fps. Il primo campione di supporti dopo la ricerca ha un timestamp pari a zero, ma un'ora media pari a 30.

I filtri renderer e mux possono usare il tempo multimediale per determinare se i fotogrammi o i campioni sono stati eliminati, verificando la presenza di gap. Tuttavia, i filtri non sono necessari per impostare l'ora del supporto. Per impostare l'ora del supporto in un esempio, chiamare il [**metodo IMediaSample::SetMediaTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ora e orologi in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



