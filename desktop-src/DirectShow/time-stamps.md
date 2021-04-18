---
description: Timestamp
ms.assetid: 445fe6b9-9d5b-45fd-9c9e-8c632c5228ae
title: Timestamp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855d2c472d7964ccad6ec8bbc87efd39b1c4cdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319547"
---
# <a name="time-stamps"></a>Timestamp

Il *timestamp* definisce l'ora di inizio e di fine di un campione multimediale, misurata nel tempo del flusso. Il timestamp viene talvolta definito ora di *presentazione*. Quando si legge la parte restante di questo articolo, è importante ricordare che non tutti i formati usano i timestamp nello stesso modo. Ad esempio, non tutti gli esempi MPEG hanno un timestamp. Nei grafici di filtro MPEG, il timestamp non viene applicato a ogni frame fino a quando non vengono restituiti dal decodificatore.

Quando un filtro renderer riceve un campione, Pianifica il rendering in base al timestamp. Se l'esempio arriva in ritardo o non ha timestamp, il filtro esegue immediatamente il rendering dell'esempio. In caso contrario, il filtro attende fino all'ora di inizio dell'esempio prima di eseguire il rendering dell'esempio. Attende l'ora di inizio chiamando il metodo [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .

I filtri di origine e i filtri del parser sono responsabili dell'impostazione dei timestamp corretti sugli esempi che elaborano. Usare le linee guida seguenti.

-   Riproduzione di file: il primo campione è il timestamp con l'ora di inizio zero. I timestamp successivi sono determinati dalla lunghezza del campione e dalla velocità di riproduzione, che a sua volta è determinata dal formato del file. Il filtro che analizza il file è responsabile del calcolo dei timestamp corretti (ad esempio, il [separatore AVI](avi-splitter-filter.md)).
-   Acquisizione video e audio: ogni campione ha un timestamp con un'ora di inizio uguale all'ora del flusso in cui è stato acquisito, con le avvertenze seguenti:
    -   I fotogrammi video di un pin di anteprima, anziché un pin di acquisizione, non hanno un timestamp. A causa della latenza del grafo, un frame video timbrato con il tempo di acquisizione arriverà sempre in ritardo nel renderer video. Questo può causare l'eliminazione dei frame dal renderer, in un tentativo di controllo della qualità. Per informazioni sul controllo della qualità, vedere [gestione del controllo di qualità](quality-control-management.md).
    -   Acquisizione audio: il filtro di acquisizione audio utilizza un proprio set di buffer distinti da quelli utilizzati dal driver audio. Il driver audio riempie i buffer del filtro di acquisizione a intervalli fissi. L'intervallo dipende dal driver, ma in genere non supera i 10 millisecondi. Il timestamp degli esempi audio riflette l'ora in cui il driver ha riempito i buffer del filtro di acquisizione audio. Questi tempi possono essere leggermente non accurati, soprattutto se l'applicazione usa una dimensione del buffer molto piccola. Tuttavia, i tempi dei supporti rifletteranno in modo accurato il numero di campioni audio nel buffer.
-   Filtri Mux: a seconda del formato di output, è possibile che un filtro Mux debba generare timestamp, altrimenti potrebbe non essere possibile. Ad esempio, il formato di file AVI usa una frequenza dei fotogrammi fissa senza timestamp, quindi il filtro [Mux AVI](avi-mux-filter.md) presuppone che gli esempi arrivino approssimativamente al momento giusto. Se i timestamp in ingresso mostrano un gap più grande di un frame, tuttavia, il mux AVI scrive una voce di indice con dimensioni pari a zero per indicare un frame eliminato. Al momento della riproduzione, i nuovi timestamp vengono generati in fase di esecuzione, come descritto in precedenza.

Per impostare il timestamp per un esempio, chiamare il metodo [**IMediaSample:: setime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

**Tempi dei supporti**

Facoltativamente, il filtro può specificare anche un *tempo di supporto* per l'esempio. In un flusso video, il tempo multimediale rappresenta il numero di frame. In un flusso audio, media time rappresenta il numero di campione nel pacchetto. Se, ad esempio, ogni pacchetto contiene un secondo di audio 44,1 kilohertz (kHz), il primo pacchetto ha un'ora di inizio del supporto pari a zero e un tempo di arresto del supporto pari a 44100. In un flusso ricercabile, il tempo dei supporti è sempre relativo all'ora di inizio del flusso. Si supponga, ad esempio, di dover cercare 2 secondi dall'inizio di un flusso video di 15 fps. Il primo campione multimediale dopo la ricerca ha un timestamp di zero, ma un tempo medio pari a 30.

I filtri renderer e MUX possono usare il tempo dei supporti per determinare se i frame o gli esempi sono stati eliminati, verificando la presenza di Gap. Tuttavia, i filtri non sono necessari per impostare il tempo del supporto. Per impostare il tempo del supporto per un esempio, chiamare il metodo [**IMediaSample:: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Time and Clocks in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



