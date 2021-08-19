---
description: 'Altre informazioni su: Funzionamento del componente Windows Imaging'
ms.assetid: c233e25b-bec6-4e67-8fbf-2bf9b70c7522
title: Funzionamento del Windows imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a63fe341bbb16afe78b159caa5c50c13fdb2cb8ee7a92f4c482dd03f8d9b8a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965110"
---
# <a name="how-the-windows-imaging-component-works"></a>Funzionamento del Windows imaging

In questo argomento sono incluse le sezioni seguenti:

-   [Individuazione e arbitraggio](#discovery-and-arbitration)
-   [Decodifica](#decoding)
-   [Encoding](#encoding)
-   [Durata di un codec](#the-lifetime-of-a-codec)
-   [Come abilitato per WIC un codec](#how-to-wic-enabled-a-codec)
-   [Supporto di apartment multi-thread in WIC](#multi-threaded-apartment-support-in-wic)
-   [Argomenti correlati](#related-topics)

## <a name="discovery-and-arbitration"></a>Individuazione e arbitraggio

Prima di poter decodificare un'immagine, è necessario trovare un codec appropriato in grado di decodificare il formato dell'immagine. Nella maggior parte dei sistemi, poiché i formati di immagine supportati sono hard-coded, non è necessario alcun processo di individuazione. Poiché la piattaforma Windows Imaging Component (WIC) è estendibile, è necessario essere in grado di identificare il formato di un'immagine e associarla a un codec appropriato.

Per supportare l'individuazione in fase di esecuzione, ogni formato di immagine deve avere un modello di identificazione che può essere usato per identificare il decodificatore appropriato per tale formato. Per i nuovi formati di file è consigliabile usare un GUID per il modello di identificazione, perché è garantito che sia univoco. Il modello di identificazione deve essere incorporato in ogni file di immagine conforme a tale formato di immagine. Ogni decodificatore dispone di una voce del Registro di sistema che specifica il modello o i modelli di identificazione dei formati di immagine che può decodificare. Quando un'applicazione deve aprire un'immagine, richiede un decodificatore da WIC. WIC cerca i decodificatori disponibili nel Registro di sistema e controlla ogni voce del Registro di sistema per individuare un modello di identificazione che corrisponda al modello incorporato nel file di immagine. Per altre informazioni sulle voci del Registro di sistema del decodificatore, vedere Voci del Registro di sistema [specifiche del codificatore](-wic-decoderregentries.md)

Quando WIC trova un singolo decodificatore che corrisponde al modello di identificazione nell'immagine, crea un'istanza del decodificatore e vi passa il file di immagine. Se WIC trova più di una corrispondenza, richiama un metodo denominato [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) in ogni decodificatore corrispondente per l'arbitrate tra di esse e trovare la corrispondenza migliore. Per altre informazioni, vedere la [sezione QueryCapabilities](-wic-imp-iwicbitmapdecoder.md) in [Implementing IWICBitmapDecoder (Implementazione di IWICBitmapDecoder).](-wic-imp-iwicbitmapdecoder.md)

## <a name="decoding"></a>Decodifica

Dopo aver selezionato e creato un'istanza del decodificatore appropriato, l'applicazione parla direttamente al decodificatore. Il decodificatore ha diverse responsabilità, che implementa tramite diverse interfacce. Questi servizi possono essere classificati come:

-   Servizi a livello di contenitore
-   Servizi a livello di frame
-   Servizi di enumerazione dei metadati
-   Trasformazioni del decodificatore nativo
-   Notifiche di stato e supporto per l'annullamento
-   Servizi di elaborazione non elaborati

I servizi a livello di contenitore includono il recupero dell'anteprima di primo livello (se supportata), l'anteprima, i contesti colori, la tavolozza (se applicabile) e il formato del contenitore, nonché l'accesso ai singoli fotogrammi di immagine all'interno del contenitore. Alcuni contenitori contengono un solo frame, mentre altri, ad esempio Tagged Image File Format (TIFF), possono contenere più frame. Questo set di servizi include anche informazioni sul decodificatore stesso e sulle relative funzionalità rispetto a un file di immagine specifico.

I singoli fotogrammi hanno le proprie anteprime e possono anche avere contesti di colore, tavolozze e altre proprietà, esposti a livello di frame. L'operazione più importante eseguita a livello di frame, tuttavia, è la decodifica effettiva dei bit di immagine per tale frame.

WIC fornisce lettori di metadati per i formati di metadati più comuni (IFD, EXIF, IPTC, XMP, APP0, APP1 e altri formati) e supporta anche l'estendibilità per i formati di metadati di terze parti. In questo modo il codec viene liberato dalla responsabilità di analizzare i metadati. Tuttavia, il codec è responsabile dell'enumerazione dei blocchi di metadati e della richiesta di un lettore di metadati per ogni blocco. WiC esegue l'individuazione per i gestori di metadati come per i codec, in base a un modello nell'intestazione del blocco corrispondente a un modello nella voce del Registro di sistema del gestore dei metadati. Per altre informazioni, vedere le voci del Registro di sistema [specifiche del codificatore](-wic-decoderregentries.md)

I decodificatori non sono necessari per supportare in modo nativo le operazioni di trasformazione, ma questa operazione consente ottimizzazioni significative delle prestazioni che offrono un'esperienza migliore per l'utente finale. Ad esempio, un'applicazione può creare una pipeline di varie trasformazioni (ridimensionamento, ritaglio, rotazione e conversione del formato pixel) da eseguire su un'immagine prima del rendering dell'immagine. Per altre informazioni sulle pipeline di trasformazione, vedere [IWICBitmapSource](-wic-imp-iwicbitmapsource.md). Dopo aver creato una pipeline di trasformazione, l'applicazione richiede la trasformazione finale nella pipeline per produrre la bitmap che risulta dall'applicazione di tutte le trasformazioni all'origine dell'immagine. A questo punto, se il decodificatore stesso è in grado di eseguire operazioni di trasformazione, WIC chiede quale delle trasformazioni richieste può eseguire. Tutte le trasformazioni richieste che il decodificatore non può eseguire verranno eseguite da WIC sull'immagine decodificata prima di restituirla al chiamante. Questa pipeline di trasformazione ottimizzata offre prestazioni migliori rispetto all'esecuzione sequenziale di ogni trasformazione in memoria, in particolare quando è possibile eseguire alcune o tutte le trasformazioni durante il processo di decodifica.

Le notifiche di stato e il supporto dell'annullamento consentono a un'applicazione di richiedere notifiche di stato per operazioni di lunga durata e di offrire all'utente la possibilità di annullare un'operazione che richiede troppo tempo. Questo è importante perché se un utente non riesce ad annullare un'operazione, può sembrare che il processo sia bloccato e provare ad annullarlo chiudendo l'applicazione.

Queste interfacce sono descritte in dettaglio nella sezione implementazione di [un decodificatore WIC-Enabled.](-wic-implementingwicdecoder.md)

I servizi di elaborazione non elaborati includono la regolazione delle impostazioni della fotocamera, ad esempio esposizione, contrasto e affilatura, o la modifica dello spazio colore prima di elaborare i bit non elaborati.

## <a name="encoding"></a>Codifica

Analogamente ai decodificatori, i codificatori hanno responsabilità che implementano tramite le interfacce. I servizi forniti dai codificatori sono complementari ai servizi forniti dai decodificatori, con la differenza che scrivono dati di immagine anziché leggerlo. I codificatori forniscono anche servizi nelle categorie seguenti:

-   Servizi a livello di contenitore
-   Servizi a livello di frame
-   Servizi di enumerazione e aggiornamento dei metadati
-   Supporto per notifica e annullamento dello stato

I servizi a livello di contenitore per un codificatore includono l'impostazione dell'anteprima di primo livello (se supportata), l'anteprima e la tavolozza (se applicabile) e l'iterazione dei singoli fotogrammi dell'immagine in modo che possano essere serializzati nel contenitore.

I servizi a livello di frame per un codificatore rispecchiano quelli per il decodificatore, ad eccezione del fatto che scrivono i dati dell'immagine, l'anteprima e qualsiasi tavolozza associata o altro componente, anziché leggerli.

Inoltre, i servizi di enumerazione dei metadati per un codificatore includono l'iterazione dei blocchi di metadati da scrivere e la chiamata dei writer di metadati appropriati per serializzare i metadati su disco.

Queste interfacce sono descritte in dettaglio nella sezione implementazione di [un codificatore WIC-Enabled.](-wic-implementingwicencoder.md)

## <a name="the-lifetime-of-a-codec"></a>Durata di un codec

Viene creata un'istanza di un codec WIC per gestire una singola immagine e in genere ha una breve durata. Viene creato quando un'immagine viene caricata e rilasciata quando l'immagine viene chiusa. Un'applicazione può usare un numero elevato di codec contemporaneamente con durate sovrapposte (si pensi a scorrere una directory contenente centinaia di immagini) e più applicazioni possono eseguire questa operazione contemporaneamente.

Anche se alcuni codec hanno una durata che ha come ambito la durata del processo in cui si trova, questo non è il caso dei codec WIC. I Windows Vista Raccolta foto, Windows Explorer e Visualizzatore foto, nonché numerose altre applicazioni, sono basati su WIC e usano il codec per visualizzare immagini e anteprime. Se l'ambito della durata del codec è stato esteso alla durata del processo, ogni volta che un'immagine o un'anteprima viene visualizzata in Windows Vista Explorer, viene creata un'istanza del codec per decodificare l'immagine che rimarrà in memoria fino al successivo riavvio del computer da parte dell'utente. Se il codec non viene mai scaricato, le relative risorse vengono di fatto "perse" perché non possono essere usate da altri componenti del sistema.

## <a name="how-to-wic-enabled-a-codec"></a>Come abilitato per WIC un codec

1.  Implementare una classe decodificatore a livello di contenitore e una classe decodificatore a livello di frame che espone le interfacce WIC necessarie per decodificare le immagini e scorrere blocchi di metadati. In questo modo tutte le applicazioni basate su WIC possono interagire con il codec nello stesso modo in cui interagiscono con i formati di immagine standard.
2.  Implementare una classe di codificatore a livello di contenitore e una classe di codificatore a livello di frame che espone le interfacce WIC necessarie per codificare le immagini e serializzare blocchi di metadati in un file di immagine.
3.  Se il formato del contenitore non è basato su un contenitore TIFF o JPEG, potrebbe essere necessario scrivere gestori di metadati per i formati di metadati comuni (EXIF, XMP). Tuttavia, se si usa un formato contenitore basato su TIFF o JPEG, questa operazione non è necessaria perché è possibile delegare ai gestori di metadati forniti dal sistema.
4.  Incorporare un modello di identificazione univoco (è consigliabile usare un GUID) in tutti i file di immagine. In questo modo il formato dell'immagine viene abbinato al codec durante l'individuazione. Se si scrive un wrapper WIC per un formato di immagine esistente, è necessario trovare un modello di bit che il codificatore scrive sempre nei relativi file di immagine univoci per tale formato di immagine e usarlo come modello di identificazione.
5.  Registrare il codec in fase di installazione. Ciò consente di individuare il codec in fase di esecuzione abbinando il modello di identificazione nel Registro di sistema al modello incorporato nel file di immagine.
6.  A Windows 7, WIC richiede che i codec siano di tipo apartment COM "Both". Ciò significa che è necessario eseguire il blocco appropriato per gestire i chiamanti e i chiamanti tra apartment in scenari multi-thread. Per altre informazioni, vedere la sezione successiva sul supporto di apartment multi-thread.
7.  Supporto per le piattaforme a 64 bit: per Windows 7, WIC richiede che i codec WIC di terze parti siano recapitati come file binari nativi a 32 bit e a 64 bit. Inoltre, il modulo a 32 bit deve installare ed eseguire in sistemi a 64 bit e il programma di installazione del codec Windows 7 di terze parti deve installare entrambi i file binari a 32 bit e a 64 bit nei sistemi a 64 bit.

## <a name="multi-threaded-apartment-support-in-wic"></a>Supporto di apartment multi-thread in WIC

Gli oggetti all'interno di un apartment multithread (MTA) possono essere chiamati contemporaneamente da qualsiasi numero di thread all'interno dell'MTA. Ciò consente prestazioni migliori nei sistemi multi-core e in determinati scenari server. Inoltre, i codec WIC in un MTA possono chiamare altri oggetti nell'agente di trasferimento messaggi senza il costo di marshalling associato alla chiamata tra thread in apartment STA diversi. Nella Windows 7, tutti i codec WIC predefiniti sono stati aggiornati per supportare gli MTA, tra cui JPEG, TIFF, PNG, GIF, ICO e BMP. È consigliabile scrivere codec di terze parti per supportare gli MTA. I codec di terze parti che non supportano gli MTA causano costi significativi per le prestazioni nelle applicazioni multi-thread a causa del marshalling. L'abilitazione del supporto MTA richiede l'implementazione della sincronizzazione appropriata nel codec di terze parti. L'implementazione esatta di queste tecniche di sincronizzazione non è nell'ambito di questo documento. Per altre informazioni sulla sincronizzazione degli oggetti COM, vedere [Understanding and Using COM Threading Models](/previous-versions/ms809971(v=msdn.10)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Introduzione (Come scrivere un codec WIC-Enabled)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Implementazione di un WIC-Enabled decodificatore](-wic-implementingwicdecoder.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Panoramica dei metadati WIC](-wic-about-metadata.md)
</dt> </dl>

 

 



