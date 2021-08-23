---
description: Miglioramenti della riproduzione di DVD in Windows Vista
ms.assetid: b3cf043f-c974-4240-8291-5c717bd8afaa
title: Miglioramenti della riproduzione di DVD in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5757f5dd73dc547ae123490fd8de84b0606d1ade8490c9600486df0b846541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148714"
---
# <a name="dvd-playback-enhancements-in-windows-vista"></a>Miglioramenti della riproduzione di DVD in Windows Vista

In questa sezione vengono descritti i miglioramenti apportati alla riproduzione e alla navigazione dei DVD in Windows Vista.

**Specifica di un decodificatore**

Nelle versioni precedenti di DirectShow, era difficile specificare un particolare decodificatore MPEG-2 quando si compilava un grafico di riproduzione DVD. A partire da Windows Vista, un'applicazione può specificare il decodificatore come segue:

1.  Aggiungere il decodificatore al grafo prima di chiamare [**IDvdGraphBuilder::RenderDvdVideoVolume**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume).
2.  Chiamare **RenderDvdVideoVolume e** impostare il \_ flag AM DVD DO NOT \_ \_ \_ CLEAR. Lo strumento di navigazione DVD offrirà la preferenza per il decodificatore aggiunto.

**Supporto per il renderer video avanzato**

È consigliabile che le applicazioni scritte per Windows Vista o versioni successive usino [**enhanced video renderer**](enhanced-video-renderer-filter.md) (EVR) per la riproduzione video. Per usare EVR in un'applicazione di riproduzione DVD, impostare il flag AM DVD EVR ONLY quando si \_ \_ chiama \_ **RenderDvdVideoVolume.**

Per configurare EVR prima di compilare il grafo, chiamare [**IDvdGraphBuilder::GetDvdInterface**](/windows/desktop/api/Strmif/nf-strmif-idvdgraphbuilder-getdvdinterface) ed eseguire una query per **l'interfaccia IEVRFilterConfig** o **IMFVideoRenderer.** Queste interfacce sono documentate nella documentazione Media Foundation SDK. Per altre informazioni sulla configurazione del renderer video in un grafico di riproduzione DVD, vedere [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).

Dvd Navigator non userà L'EVR a meno che il metodo [**IAMDecoderCaps::GetDecoderCaps**](/windows/desktop/api/Strmif/nf-strmif-iamdecodercaps-getdecodercaps) del decodificatore non restituisca il flag AM \_ GETDECODERCAP \_ QUERY \_ EVR \_ SUPPORT. Questo flag viene definito per garantire che le applicazioni siano compatibili con i decodificatori esistenti. Se **RenderDvdVideoVolume** non riesce a usare il flag AM \_ DVD EVR ONLY, eseguire il fall back a un altro renderer video chiamando di nuovo il metodo \_ senza il flag \_ .

**Riproduzione inversa uniforme**

Lo strumento di spostamento DVD può ora eseguire una riproduzione inversa uniforme. Nella riproduzione inversa uniforme, lo strumento di spostamento DVD invia intere unità oggetto video (VOU) al decodificatore e il decodificatore emette i fotogrammi in ordine inverso. Questa funzionalità richiede che i decodificatori supportino la riproduzione inversa uniforme.

Quando l'applicazione imposta la velocità di riproduzione su un valore negativo, DVD Navigator esegue una query nei decodificatori per la proprietà [**AM \_ RATE \_ ReverseMaxFullDataRate.**](am-rate-reversemaxfulldatarate-property.md) Il valore di questa proprietà è il valore assoluto della velocità inversa massima x 10000. Ad esempio, se la velocità inversa massima è -2,0, il valore è 20000.

Se il decodificatore video supporta la proprietà , lo strumento di navigazione DVD usa la riproduzione inversa uniforme. Il flusso audio viene riprodotto in ordine inverso se il decodificatore audio supporta la proprietà . In caso contrario, il flusso audio viene disattivato. Se il decodificatore video non supporta la proprietà o se la velocità di riproduzione supera la velocità inversa massima del decodificatore video, lo strumento di navigazione DVD passa alla *modalità di analisi*. In modalità di analisi, lo strumento di navigazione DVD invia solo i fotogrammi I al decodificatore e rilascia tutti i fotogrammi B e P.

Durante la riproduzione inversa senza problemi, lo strumento di navigazione del DVD invia al decodificatore i VOBI completi. Lo strumento di navigazione dvd invia i VOBU in ordine inverso, ma invia i fotogrammi all'interno di ogni VOBU nel normale ordine di inoltro. All'inizio di ogni VOBU, lo strumento di navigazione DVD imposta il flag AM \_ ReverseBlockStart sull'esempio. Alla fine del VOBU, lo strumento di navigazione del DVD invia un esempio vuoto con il \_ flag AM ReverseBlockEnd. Per recuperare questi flag, chiamare [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) nell'esempio. I flag vengono impostati nel **membro dwTypeSpecificFlags** della [**struttura AM \_ SAMPLE2 \_**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) PROPERTIES.

Il decodificatore memorizza nella cache i dati video fino a quando non riceve l'esempio con il \_ flag AM ReverseBlockEnd. A questo punto, il decodificatore recapita i fotogrammi decodificati in ordine inverso. Ad esempio, se VOBU 1 contiene i fotogrammi 1-4 e VOBU 2 contiene i fotogrammi 5-8, lo strumento di navigazione DVD invierà i fotogrammi nell'ordine seguente:

(Avvio blocco) F5 F6 F7 F8 (fine blocco) (inizio blocco) F1 F2 F3 F4 (fine blocco)

Il decodificatore deve elaborare i fotogrammi come segue:

1.  Decodificare VOBU 2.
2.  Frame di output: F8 F7 F6 F5
3.  Decodificare VOBU 1.
4.  Frame di output: F4 F3 F2 F1

Lo strumento di spostamento DVD imposta il timestamp sul primo esempio nel VOBU (F1 e F5 in questo esempio), ma il timestamp contiene l'ora di presentazione dell'inizio del blocco, quindi il decodificatore deve applicare questa ora all'ultimo campione nel blocco (F4 e F8). I tempi di presentazione aumentano durante la riproduzione inversa.

In genere un VOBU contiene fino a 42 fotogrammi e può contenere più di un gruppo di immagini (GOP). Per consentire la decodifica dell'intero VOBU, il decodificatore deve memorizzare nella cache i fotogrammi I e P decodificati. Le VOBU nei DVD non sono GOP chiuse, quindi un frame B all'interno di un GOP potrebbe richiedere la decodifica di tutti i fotogrammi di riferimento nel GOP precedente. Se il decodificatore non dispone di superfici sufficienti per contenere tutti i fotogrammi decodificati, potrebbe essere necessario decodificare nuovamente i fotogrammi selezionati.

**Modifiche alla frequenza**

Per impostazione predefinita, lo strumento di navigazione DVD scarica il grafico tra le modifiche della frequenza. Se il decodificatore supporta la proprietà [**AM \_ RATE \_ ResetOnTimeDisc,**](am-rate-resetontimedisc-property.md) tuttavia, lo strumento di navigazione DVD non scarica il grafico, determinando una transizione più uniforme tra le velocità di riproduzione.

Lo strumento di spostamento DVD contrassegna sempre i campioni per la riproduzione a una velocità di 1x, indipendentemente dalla velocità di riproduzione effettiva. Il decodificatore deve ridimensionare i timestamp sui campioni decodificati in modo che corrispondano alla velocità di riproduzione effettiva. Per informazioni dettagliate, vedere [**Am \_ RATE \_ SimpleRateChange Property**](am-rate-simpleratechange-property.md). Di conseguenza, quando si riproduce a velocità diverse da 1x, i timestamp nei fotogrammi decodificati sono diversi da quelli dei fotogrammi codificati. Ogni volta che lo strumento di navigazione DVD imposta il flag AM \_ SAMPLE TIMEDISCONTINUITY su un campione, il decodificatore deve \_ risincronizzare i timestamp. In altre parole, il frame decodificato deve avere lo stesso timestamp del frame di input. Per recuperare il flag AM \_ SAMPLE \_ TIMEDISCONTINUITY, chiamare [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) nell'esempio. Il flag è impostato nel **membro dwSampleFlags** della [**struttura AM \_ SAMPLE2 \_**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) PROPERTIES.

**Risparmio energia**

In Windows Vista, lo strumento di spostamento DVD consente i miglioramenti seguenti per il risparmio energia:

-   Risoluzione del timer superiore
-   Cache dei dati più grande

**Risoluzione timer:** le applicazioni possono richiedere una risoluzione minima del timer chiamando la **funzione timeBeginPeriod.** Una risoluzione più elevata (periodo più breve) aumenta la velocità di risposta del sistema a eventi periodici, ad esempio i timeout, ma può anche aumentare la frequenza dei commutatori di contesto del thread.

Per impostazione predefinita, il clock di riferimento in DirectShow la risoluzione del timer su 1 millisecondo. A tale risoluzione, la CPU non entra in modalità di risparmio energia. A partire da Windows Vista, dvd Navigator esegue l'override del comportamento predefinito dell'orologio di riferimento chiamando [**IReferenceClockTimerControl::SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) sul clock di riferimento. In questo modo viene rimossa la richiesta dell'orologio per una risoluzione del timer di 1 millisecondo. Ciò potrebbe consentire alla CPU di accedere a una modalità di risparmio energia.

La risoluzione del timer è un'impostazione globale. Windows seleziona il valore più basso richiesto. I filtri del renderer di combinazione video (VMR-7 e VMR-9) impostano la risoluzione del timer su 1 millisecondo. L'EVR imposta in genere la risoluzione su un valore compreso tra 4 e 8 millisecondi, a seconda che la composizione del desktop sia abilitata o meno e che l'EVR sia in modalità schermo intero. La risoluzione potrebbe essere impostata anche da altre applicazioni.

**Dimensioni cache:** le applicazioni possono specificare la quantità di dati memorizzati nella cache da DVD Navigator impostando l'opzione CacheSizeInMB del DVD nel metodo \_ [**IDvdControl2::SetOption.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) Se l'applicazione imposta questo flag su un valore elevato (> 50 MB), l'unità DVD potrebbe essere scesa dopo il pre-recupero iniziale, a seconda dell'hardware, che può ridurre il consumo di energia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



