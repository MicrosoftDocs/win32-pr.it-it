---
description: Miglioramenti della riproduzione DVD in Windows Vista
ms.assetid: b3cf043f-c974-4240-8291-5c717bd8afaa
title: Miglioramenti della riproduzione DVD in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159056d2c7acaec18a73a30b21f79bcd6267ca33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304015"
---
# <a name="dvd-playback-enhancements-in-windows-vista"></a>Miglioramenti della riproduzione DVD in Windows Vista

In questa sezione vengono descritti i miglioramenti apportati alla riproduzione e alla navigazione dei DVD in Windows Vista.

**Specifica di un decodificatore**

Nelle versioni precedenti di DirectShow era difficile specificare un particolare decodificatore MPEG-2 quando si crea un grafico di riproduzione DVD. A partire da Windows Vista, un'applicazione può specificare il decodificatore come indicato di seguito:

1.  Aggiungere il decodificatore al grafo prima di chiamare [**IDvdGraphBuilder:: RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume).
2.  Chiamare **RenderDvdVideoVolume** e impostare il \_ flag AM DVD non \_ \_ \_ deselezionare. Il navigatore DVD fornirà le preferenze al decodificatore aggiunto.

**Supporto per il renderer video migliorato**

È consigliabile che le applicazioni scritte per Windows Vista o versioni successive usino il [**renderer video avanzato**](enhanced-video-renderer-filter.md) (EVR) per la riproduzione video. Per usare EVR in un'applicazione di riproduzione DVD, impostare il \_ flag AM DVD \_ EVR \_ only quando si chiama **RenderDvdVideoVolume**.

Per configurare il EVR prima di compilare il grafo, chiamare [**IDvdGraphBuilder:: GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) ed eseguire una query per l'interfaccia **IEVRFilterConfig** o **IMFVideoRenderer** . Queste interfacce sono documentate nella documentazione di Media Foundation SDK. Per ulteriori informazioni sulla configurazione del renderer video in un grafico di riproduzione DVD, vedere la pagina relativa [alla creazione del grafico del filtro DVD](building-the-dvd-filter-graph.md).

Il navigatore DVD non userà EVR, a meno che il metodo [**IAMDecoderCaps:: GetDecoderCaps**](/windows/desktop/api/Strmif/nf-strmif-iamdecodercaps-getdecodercaps) del decodificatore non restituisca il \_ \_ flag di supporto EVR della query am GETDECODERCAP \_ \_ . Questo flag viene definito per garantire che le applicazioni siano compatibili con i decodificatori esistenti. Se **RenderDvdVideoVolume** non riesce a usare il \_ flag AM DVD \_ EVR \_ only, eseguire il fallback a un altro renderer video chiamando il metodo senza il flag.

**Riproduzione smussata inversa**

Il navigatore DVD può ora eseguire la riproduzione senza problemi. Nella riproduzione Smooth inversa, il navigatore DVD invia intere unità di oggetti video (VOBUs) al decodificatore e il decodificatore emette i frame in ordine inverso. Questa funzionalità richiede che i decodificatori supportino la riproduzione Smooth inversa.

Quando l'applicazione imposta la velocità di riproduzione su un valore negativo, il navigatore DVD esegue una query sui decodificatori per la proprietà [**am \_ rate \_ ReverseMaxFullDataRate**](am-rate-reversemaxfulldatarate-property.md) . Il valore di questa proprietà è il valore assoluto della velocità inversa massima x 10000. Se ad esempio la velocità massima inversa è-2,0, il valore è 20000.

Se il decodificatore video supporta la proprietà, il navigatore DVD usa la riproduzione Smooth inversa. Il flusso audio viene riprodotto in senso inverso se il decodificatore audio supporta la proprietà; in caso contrario, il flusso audio viene disattivato. Se il decodificatore video non supporta la proprietà o la velocità di riproduzione supera la frequenza inversa massima del decodificatore video, il navigatore DVD passa alla *modalità di analisi*. In modalità di analisi, il navigatore DVD invia solo i frame i al decodificatore e rilascia tutti i frame B e P.

Durante la riproduzione Smooth inversa, il navigatore DVD invia VOBUs completi al decodificatore. Il navigatore DVD invia il VOBUs in ordine inverso, ma invia i frame all'interno di ogni VOBU nel normale ordine di avanzamento. All'inizio di ogni VOBU, il navigatore DVD imposta il \_ flag AM ReverseBlockStart sul campione. Alla fine di VOBU, il navigatore DVD invia un campione vuoto con il flag AM \_ ReverseBlockEnd. Per recuperare questi flag, chiamare [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) nell'esempio. I flag vengono impostati nel membro **dwTypeSpecificFlags** della struttura delle [**\_ \_ Proprietà SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

Il decodificatore memorizza nella cache i dati del video fino a quando non riceve l'esempio con il \_ flag AM ReverseBlockEnd. A questo punto, il decodificatore recapita i frame decodificati in ordine inverso. Se, ad esempio, VOBU 1 contiene frame da 1 a 4 e VOBU 2 contiene frame da 5 a 8, il navigatore DVD invierà i frame nell'ordine seguente:

(Inizio blocco) F5 F6 F7 F8 (fine blocco) (inizio blocco) F1 F2 F3 F4 (fine blocco)

Il decodificatore deve elaborare i frame come indicato di seguito:

1.  Decodifica VOBU 2.
2.  Frame di output: F8 F7 F6 F5
3.  Decodifica VOBU 1.
4.  Frame di output: F4 F3 F2 F1

Il navigatore DVD imposta il timestamp del primo campione in VOBU (F1 e F5 in questo esempio), ma il timestamp contiene l'ora di presentazione dell'inizio del blocco, quindi il decodificatore deve applicare questa ora all'ultimo campione nel blocco (F4 e F8). I tempi di presentazione aumentano durante la riproduzione inversa.

In genere un VOBU contiene fino a 42 frame e potrebbe contenere più di un Group of Pictures (GOP). Per consentire la decodifica dell'intero VOBU, il decodificatore deve memorizzare nella cache i frame i e P decodificati. VOBUs nei DVD non sono GOPs chiusi, quindi un frame B in un GOP potrebbe richiedere la decodifica di tutti i frame di riferimento nel GOP precedente. Se il decodificatore non dispone di una superficie sufficiente per contenere tutti i frame decodificati, potrebbe essere necessario decodificare i frame selezionati.

**Modificare le tariffe**

Per impostazione predefinita, il navigatore DVD Scarica il grafico tra le variazioni di frequenza. Se il decodificatore supporta la proprietà [**am \_ rate \_ ResetOnTimeDisc**](am-rate-resetontimedisc-property.md) , tuttavia, il navigatore DVD non Scarica il grafo, ottenendo una transizione più uniforme tra le frequenze di riproduzione.

Il navigatore DVD sempre timbra gli esempi per la riproduzione a una velocità 1x, indipendentemente dalla velocità effettiva di riproduzione. Il decodificatore deve ridimensionare i timestamp degli esempi decodificati in modo che corrispondano alla velocità effettiva di riproduzione. Per informazioni dettagliate, vedere [**am \_ rate \_ SimpleRateChange Property**](am-rate-simpleratechange-property.md). Di conseguenza, quando si giocano a velocità diverse da 1x, i timestamp sui fotogrammi decodificati dipendono da quelli sui frame codificati. Ogni volta che il navigatore DVD imposta il \_ \_ flag TIMEDISCONTINUITY di esempio AM in un campione, il decodificatore deve risincronizzare i timestamp. In altre parole, il fotogramma decodificato deve avere lo stesso timestamp del frame di input. Per recuperare il \_ flag TIMEDISCONTINUITY di esempio AM \_ , chiamare [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) nell'esempio. Il flag viene impostato nel membro **dwSampleFlags** della struttura delle [**\_ \_ Proprietà SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

**Risparmio energia**

In Windows Vista, il navigatore DVD offre i miglioramenti seguenti al risparmio energia:

-   Risoluzione del timer superiore
-   Cache di dati di dimensioni maggiori

**Risoluzione del timer**: le applicazioni possono richiedere una risoluzione del timer minima chiamando la funzione **timeBeginPeriod** . Una risoluzione più elevata (periodo più breve) aumenta la velocità di risposta del sistema agli eventi periodici, ad esempio i timeout, ma può anche aumentare la frequenza delle commutazioni di contesto del thread.

Per impostazione predefinita, l'orologio di riferimento in DirectShow imposta la risoluzione del timer su 1 millisecondo. Con questa risoluzione, la CPU non entrerà in modalità di risparmio energia. A partire da Windows Vista, il navigatore DVD sostituisce il comportamento predefinito dell'orologio di riferimento chiamando [**IReferenceClockTimerControl:: SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) sull'orologio di riferimento. In questo modo viene rimossa la richiesta dell'orologio per una risoluzione del timer di 1 millisecondi. Questo potrebbe consentire alla CPU di accedere a una modalità di risparmio energia.

La risoluzione del timer è un'impostazione globale; Windows sceglie il valore minimo richiesto. I filtri VMR (video Mixing Renderer) (VMR-7 e VMR-9) impostano la risoluzione del timer su 1 millisecondo. Il EVR in genere imposta la risoluzione su un valore compreso tra 4 e 8 millisecondi, a seconda del fatto che la composizione del desktop sia abilitata e che il EVR sia in modalità schermo intero. Anche altre applicazioni potrebbero impostare la risoluzione.

**Dimensioni cache**: le applicazioni possono specificare la quantità di dati memorizzata nella cache dal NAVIGAtore DVD impostando l' \_ opzione DVD CacheSizeInMB nel metodo [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) . Se l'applicazione imposta questo flag su un valore elevato (> 50 MB), l'unità DVD potrebbe essere ridotta dopo il recupero iniziale, a seconda dell'hardware, che può ridurre il consumo di energia elettrica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



