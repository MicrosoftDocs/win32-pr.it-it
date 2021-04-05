---
description: Altre informazioni su come funziona il componente Windows Imaging
ms.assetid: c233e25b-bec6-4e67-8fbf-2bf9b70c7522
title: Funzionamento del componente Windows Imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc9fe31ae4346f2c2d1f0b273e78ed10a0ec7e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757835"
---
# <a name="how-the-windows-imaging-component-works"></a>Funzionamento del componente Windows Imaging

In questo argomento sono incluse le sezioni seguenti:

-   [Individuazione e arbitraggio](#discovery-and-arbitration)
-   [Decodifica](#decoding)
-   [Encoding](#encoding)
-   [Durata di un codec](#the-lifetime-of-a-codec)
-   [Come abilitare con WIC un codec](#how-to-wic-enabled-a-codec)
-   [Supporto di Apartment multithread in WIC](#multi-threaded-apartment-support-in-wic)
-   [Argomenti correlati](#related-topics)

## <a name="discovery-and-arbitration"></a>Individuazione e arbitraggio

Prima di poter decodificare un'immagine, è necessario trovare un codec appropriato in grado di decodificare il formato di immagine. Nella maggior parte dei sistemi, poiché i formati di immagine supportati sono hardcoded, non è necessario alcun processo di individuazione. Poiché la piattaforma Windows Imaging Component (WIC) è estendibile, è necessario essere in grado di identificare il formato di un'immagine e di associarla a un codec appropriato.

Per supportare l'individuazione in fase di esecuzione, ogni formato di immagine deve avere un modello di identificazione che può essere usato per identificare il decodificatore appropriato per tale formato. Per i nuovi formati di file si consiglia di usare un GUID per il modello di identificazione, perché è garantito che sia univoco. Il modello di identificazione deve essere incorporato in ogni file di immagine conforme al formato di immagine. Ogni decodificatore include una voce del registro di sistema che specifica il modello di identificazione o i modelli dei formati di immagine che può decodificare. Quando un'applicazione deve aprire un'immagine, richiede un decodificatore da WIC. WIC Cerca i decodificatori disponibili nel registro di sistema e controlla ogni voce del registro di sistema per individuare un modello di identificazione corrispondente al modello incorporato nel file di immagine. Per altre informazioni sulle voci del registro di sistema decoder, vedere [voci del registro di sistema specifiche del codificatore](-wic-decoderregentries.md)

Quando WIC trova un singolo decodificatore che corrisponde al modello di identificazione nell'immagine, crea un'istanza del decodificatore e lo passa al file di immagine. Se WIC trova più di una corrispondenza, richiama un metodo denominato [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) in ogni decodificatore corrispondente per eseguire l'arbitrario tra di essi e trovare la migliore corrispondenza. Per ulteriori informazioni, vedere la sezione [QueryCapabilities](-wic-imp-iwicbitmapdecoder.md) nell' [implementazione di IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

## <a name="decoding"></a>Decodifica

Dopo che il decodificatore appropriato è stato selezionato e ne è stata creata un'istanza, l'applicazione comunica direttamente con il decodificatore. Il decodificatore ha diverse responsabilità, implementate tramite varie interfacce. Questi servizi possono essere classificati come:

-   Servizi a livello di contenitore
-   Servizi a livello di frame
-   Servizi di enumerazione dei metadati
-   Trasformazioni del decodificatore Native
-   Notifiche sullo stato di avanzamento e supporto per l'annullamento
-   Servizi di elaborazione non elaborati

I servizi a livello di contenitore includono il recupero dell'anteprima di primo livello (se supportata), l'anteprima, i contesti dei colori, la tavolozza (se applicabile) e il formato del contenitore, oltre a fornire l'accesso ai singoli fotogrammi dell'immagine all'interno del contenitore. Alcuni contenitori contengono solo un singolo frame, mentre altri, ad esempio Tagged Image File Format (TIFF), possono contenere più frame. Questo set di servizi include anche informazioni sul decodificatore stesso e sulle relative funzionalità rispetto a un file di immagine specifico.

I singoli frame hanno anteprime specifiche e possono avere anche contesti di colore, tavolozze e altre proprietà esposte a livello di frame. L'operazione più importante eseguita a livello di frame, tuttavia, è la decodifica effettiva dei bit dell'immagine per quel frame.

WIC fornisce lettori di metadati per i formati di metadati più comuni (IFD, EXIF, IPTC, XMP, APP0, APP1 e altri formati) e supporta anche l'estendibilità per i formati di metadati di terze parti. Questo consente di liberare il codec di responsabilità dell'analisi dei metadati. Tuttavia, il codec è responsabile dell'enumerazione dei blocchi di metadati e della richiesta di un lettore di metadati per ogni blocco. WIC esegue l'individuazione per i gestori di metadati nello stesso modo in cui avviene per i codec, in base a un modello nell'intestazione del blocco corrispondente a un modello nella voce del registro di sistema del gestore dei metadati. Per ulteriori informazioni, vedere le [voci del registro di sistema specifiche del codificatore](-wic-decoderregentries.md)

I decodificatori non sono obbligatori a supportare in modo nativo le operazioni di trasformazione, ma in questo modo vengono abilitate ottimizzazioni delle prestazioni significative che offrono una migliore esperienza dell'utente finale. Un'applicazione, ad esempio, può creare una pipeline di varie trasformazioni (ridimensionamento, ritaglio, rotazione e conversione del formato pixel) da eseguire su un'immagine prima che venga eseguito il rendering dell'immagine. Per ulteriori informazioni sulle pipeline di trasformazione, vedere [IWICBitmapSource](-wic-imp-iwicbitmapsource.md). Dopo la creazione di una pipeline di trasformazione, l'applicazione richiede la trasformazione finale nella pipeline per produrre la bitmap risultante dall'applicazione di tutte le trasformazioni all'origine dell'immagine. A questo punto, se il decodificatore stesso è in grado di eseguire operazioni di trasformazione, WIC chiede quale delle trasformazioni richieste è in grado di eseguire. Tutte le trasformazioni richieste che non possono essere eseguite dal decodificatore verranno eseguite da WIC sull'immagine decodificata prima di restituirla al chiamante. Questa pipeline di trasformazione ottimizzata offre prestazioni migliori rispetto all'esecuzione sequenziale di ogni trasformazione in memoria, in particolare quando è possibile eseguire alcune o tutte le trasformazioni durante il processo di decodifica.

Le notifiche di stato e il supporto per l'annullamento consentono a un'applicazione di richiedere notifiche sullo stato di avanzamento per operazioni di lunga durata e di consentire all'applicazione di fornire all'utente la possibilità di annullare un'operazione che richiede troppo tempo. Questo è importante perché se un utente non è in grado di annullare un'operazione, potrebbe sentire che il processo è bloccato e provare a annullarlo chiudendo l'applicazione.

Queste interfacce sono descritte in dettaglio nella sezione relativa all' [implementazione di un Decodificatore WIC-Enabled](-wic-implementingwicdecoder.md).

I servizi di elaborazione RAW includono la regolazione delle impostazioni della fotocamera, ad esempio l'esposizione, il contrasto e l'affilatura o la modifica dello spazio colore prima di elaborare i bit non elaborati.

## <a name="encoding"></a>Codifica

Come i decodificatori, i codificatori hanno responsabilità che implementano attraverso le interfacce. I servizi forniti dai codificatori sono complementari ai servizi forniti dai decodificatori, con la differenza che scrivono i dati dell'immagine anziché leggerli. I codificatori forniscono anche servizi nelle categorie seguenti:

-   Servizi a livello di contenitore
-   Servizi a livello di frame
-   Enumerazione dei metadati e servizi di aggiornamento
-   Supporto per notifiche di stato e annullamento

I servizi a livello di contenitore per un codificatore includono l'impostazione dell'anteprima di primo livello (se supportata), l'anteprima e la tavolozza (se applicabile) e l'iterazione nei singoli frame dell'immagine in modo che possano essere serializzati nel contenitore.

I servizi a livello di frame per un codificatore eseguono il mirroring di quelli per il decodificatore, ad eccezione del fatto che scrivono i dati dell'immagine, l'anteprima e qualsiasi tavolozza associato o altro componente, anziché leggerli.

Inoltre, i servizi di enumerazione dei metadati per un codificatore includono l'iterazione dei blocchi di metadati da scrivere e il richiamo dei writer di metadati appropriati per serializzare i metadati su disco.

Queste interfacce sono descritte in dettaglio nella sezione relativa all' [implementazione di un codificatore WIC-Enabled](-wic-implementingwicencoder.md).

## <a name="the-lifetime-of-a-codec"></a>Durata di un codec

Viene creata un'istanza di un codec WIC per gestire una singola immagine e in genere è presente una durata breve. Viene creato quando viene caricata un'immagine e viene rilasciata quando l'immagine viene chiusa. Un'applicazione può usare un numero elevato di codec contemporaneamente a una durata sovrapposta (si può pensare di scorrere una directory contenente centinaia di immagini) e più applicazioni possono eseguire questa operazione nello stesso momento.

Anche se alcuni codec hanno una durata che ha come ambito la durata del processo in cui si trovano, questo non avviene con i codec WIC. Raccolta foto di Windows Vista, Esplora risorse e Visualizzatore foto, nonché numerose altre applicazioni, sono basate su WIC e utilizzeranno il codec per visualizzare immagini e anteprime. Se la durata del codec è stata assegnata all'ambito della durata del processo, ogni volta che un'immagine o un'anteprima è stata visualizzata in Esplora risorse di Windows Vista, il codec di cui è stata creata un'istanza per decodificare l'immagine rimarrà in memoria fino al successivo riavvio del computer da parte dell'utente. Se il codec non viene mai scaricato, le relative risorse sono in effetti "perse" perché non possono essere usate da altri componenti nel sistema.

## <a name="how-to-wic-enabled-a-codec"></a>Come abilitare con WIC un codec

1.  Implementare una classe decoder a livello di contenitore e una classe decodificatore a livello di frame che espone le interfacce WIC necessarie per la decodifica delle immagini e l'iterazione nei blocchi di metadati. Ciò consente a tutte le applicazioni basate su WIC di interagire con il codec nello stesso modo in cui interagiscono con i formati di immagine standard.
2.  Implementare una classe del codificatore a livello di contenitore e una classe del codificatore a livello di frame che espone le interfacce WIC necessarie per la codifica di immagini e la serializzazione di blocchi di metadati in un file di immagine.
3.  Se il formato del contenitore non è basato su un contenitore TIFF o JPEG, potrebbe essere necessario scrivere gestori di metadati per i formati di metadati comuni (EXIF, XMP). Tuttavia, se si usa un formato di contenitore basato su TIFF o JPEG, questa operazione non è necessaria perché è possibile delegare ai gestori di metadati forniti dal sistema.
4.  Incorporare un modello di identificazione univoco (si consiglia un GUID) in tutti i file di immagine. In questo modo è possibile trovare una corrispondenza tra il formato dell'immagine e il codec durante l'individuazione. Se si scrive un wrapper WIC per un formato di immagine esistente, è necessario trovare un modello di bit che il codificatore scrive sempre nei propri file di immagine, che è univoco per tale formato di immagine, e utilizzarlo come modello di identificazione.
5.  Registrare il codec al momento dell'installazione. In questo modo, il codec viene individuato in fase di esecuzione associando il modello di identificazione nel registro di sistema al modello incorporato nel file di immagine.
6.  A partire da Windows 7, per WIC è necessario che i codec siano di tipo apartment COM "both". Ciò significa che è necessario eseguire il blocco appropriato per gestire i chiamanti e i chiamanti tra più Apartment negli scenari multithread. Per ulteriori informazioni, vedere la sezione successiva sul supporto di Apartment multithread.
7.  Supporto per piattaforme a 64 bit: per Windows 7, per WIC è necessario che i codec WIC di terze parti siano distribuiti sia come file binari nativi a 32 bit che a 64 bit. Il modulo a 32 bit, inoltre, deve essere installato ed eseguito nei sistemi a 64 bit e il programma di installazione del codec Windows 7 di terze parti deve installare sia i file binari 32 bit che 64 bit nei sistemi a 64 bit.

## <a name="multi-threaded-apartment-support-in-wic"></a>Supporto di Apartment multithread in WIC

Gli oggetti all'interno di un Apartment a thread multipli (MTA) possono essere chiamati simultaneamente da un numero qualsiasi di thread all'interno dell'MTA. In questo modo è possibile ottenere prestazioni migliori nei sistemi multicore e in alcuni scenari server. Inoltre, i codec WIC in un MTA possono chiamare altri oggetti nell'MTA senza il costo di marshalling associato alla chiamata tra thread in diversi apartment STA. In Windows 7, tutti i codec WIC inclusi sono stati aggiornati per supportare gli MTA, tra cui JPEG, TIFF, PNG, GIF, ICO e BMP. È consigliabile scrivere codec di terze parti per supportare gli MTA. I codec di terze parti che non supportano gli MTA causano costi significativi in termini di prestazioni nelle applicazioni multithread a causa del marshalling. Per abilitare il supporto MTA, è necessario implementare una sincronizzazione corretta nel codec di terze parti. L'implementazione esatta di queste tecniche di sincronizzazione esula dall'ambito di questo documento. Per ulteriori informazioni sulla sincronizzazione degli oggetti COM, vedere [Understanding and using com Threading Models](/previous-versions/ms809971(v=msdn.10)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Introduzione (come scrivere un CODEC WIC-Enabled)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Implementazione di un decodificatore WIC-Enabled](-wic-implementingwicdecoder.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Cenni preliminari sui metadati WIC](-wic-about-metadata.md)
</dt> </dl>

 

 



